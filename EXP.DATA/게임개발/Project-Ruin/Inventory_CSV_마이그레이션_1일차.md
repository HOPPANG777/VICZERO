# Project-Ruin Inventory CSV 마이그레이션 학습 기록 - 1일차

- 제목: ScriptableObject 원본 데이터를 CSV Definition 구조로 전환하기
- 분류: 게임 개발 / Unity / 데이터 파이프라인
- 출처: `D:/VicZero/Coding/Project-Ruin/Assets/_Game/Docs/WORKLOG_2026-07-18_INVENTORY_CSV_MIGRATION.md`
- 작성일: 2026-07-18
- 프로젝트: Project-Ruin (이전 이름: RuinConservator)
- 학습 성취도: 93/100

## 빠른 요약

```text
items.csv
-> ItemCsvDefinitionLoader
-> ItemDefinition
-> GameDataRepository의 item_id 인덱스
-> InventoryController
-> Localization과 ItemVisualCatalog 결합
-> Inventory UI
```

기획자가 자주 수정하는 ID, 이름 Key, 설명 Key, 가격, 타입, 중첩 수는 CSV로 옮겼다. Unity 객체 참조가 필요한 Sprite만 ScriptableObject 카탈로그에 남겼다.

## 핵심 학습

### 데이터의 성격에 따라 저장 위치를 나눈다

- 기획 데이터: `items.csv`
- 다국어 문장: `localization.csv`
- Unity Sprite 참조: `ItemVisualCatalog.asset`
- 플레이어 보유 상태: `InventorySlotData`와 세이브 데이터

모든 데이터를 한 기술에 몰아넣지 않고 누가 자주 수정하는지와 어떤 참조가 필요한지를 기준으로 나눴다.

### 안정적인 ID가 시스템 사이의 계약이 된다

Quest, Inventory, 세이브는 객체 참조나 CSV 행 순서가 아니라 `item_id`로 연결한다. 따라서 출시 후 ID 변경은 단순 데이터 수정이 아니라 세이브 마이그레이션 문제로 취급해야 한다.

### 검증은 입력 지점과 통합 지점에 모두 필요하다

CSV Loader는 헤더, 형식, 숫자 범위, enum 값을 검사한다. Repository는 Localization과 Quest의 교차 참조를 검사한다. 각 계층이 자신이 알 수 있는 오류를 책임지므로 잘못된 데이터가 UI나 플레이 중에 늦게 발견되는 것을 줄인다.

### 레거시 경로를 남기면 이중 관리가 다시 생긴다

CSV 이관 후 `ItemDataSO`, 개별 아이템 에셋, Inspector 목록을 제거했다. 새 구조를 추가하는 것만큼 이전 제작 경로를 닫는 것이 중요하다.

### 빌드 성공과 Unity 동작 검증은 다르다

C# 런타임·Editor 빌드와 CSV 스모크 테스트는 통과했지만, Prefab 참조·UI 표시·세이브 복원은 Unity Test Runner와 Play Mode에서 별도로 확인해야 한다.

### `.meta`는 협업 가능한 결과물의 일부다

Unity 원본 파일만 Commit하고 `.meta`를 누락하면 다른 환경에서 GUID가 달라질 수 있다. 로컬 구현이 성공했더라도 팀원이 안전하게 Clone할 수 없다면 마이그레이션 마감은 완료되지 않은 것이다.

## 잘한 점

- Inventory만 바꾸지 않고 Quest, Localization, UI, 검증기, 테스트와 문서를 함께 갱신했다.
- 존재하지 않는 Quest Item ID를 실제 실패 사례로 확인했다.
- 레거시 타입과 에셋이 다시 추가되는 회귀까지 테스트 대상으로 만들었다.
- 비개발 직군이 처음부터 따라 할 수 있는 제작 가이드를 작성했다.
- `.meta` 위험을 발견하고 무리하게 Commit하지 않은 판단이 안전했다.

## 보완할 점

- Unity Test Runner와 Play Mode 검증을 완료해야 한다.
- 실제 기존 세이브 파일의 슬롯과 `new` 상태 복원을 확인해야 한다.
- `.meta` 정책을 해결한 뒤 다른 환경의 Clone 검증이 필요하다.
- 큰 변경 범위를 목적별 Commit으로 분리해 리뷰 가능하게 만들어야 한다.

## 다음 적용

1. `.meta` 추적 정책을 별도 작업으로 해결한다.
2. Unity 메뉴 검증기와 Edit Mode 테스트를 실행한다.
3. Coin 지급, RepairKit 소모, UI와 저장 복원을 Play Mode에서 확인한다.
4. 변경을 런타임·데이터·테스트·문서 Commit으로 분리한다.
5. 실제 아이콘이 준비되면 `icon_id`와 Sprite를 연결한다.
