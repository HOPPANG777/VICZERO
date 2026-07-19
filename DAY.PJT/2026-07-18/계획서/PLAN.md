# 2026-07-18 계획서

- 날짜: 2026-07-18
- 기록 작성일: 2026-07-19
- 연결 장기 프로젝트: `../../../LNG.PJT/Project-Ruin.md`
- 오늘의 핵심 목표: Inventory 아이템 원본을 ScriptableObject에서 CSV 기반 Definition 구조로 전환하고 제작·검증 흐름을 통합한다.
- 실행 상태: 핵심 구현 완료, Unity 최종 검증 및 Commit 대기
- 원본 작업 로그: `D:/VicZero/Coding/Project-Ruin/Assets/_Game/Docs/WORKLOG_2026-07-18_INVENTORY_CSV_MIGRATION.md`

## 오늘의 TODO

| 순서 | TODO | 완료 기준 | 상태 |
|---|---|---|---|
| 1 | Inventory CSV 마이그레이션 | 코드·데이터·Prefab·검증기·회귀 테스트·기획 문서를 CSV 구조로 전환한다. | 핵심 구현 완료 |

## 완료 기준 확인

- [x] `items.csv`와 순수 C# `ItemDefinition`을 추가했다.
- [x] Localization과 Quest Item ID 교차 검증을 연결했다.
- [x] InventoryController와 UI를 Definition 기반으로 전환했다.
- [x] Sprite 참조를 `ItemVisualCatalogSO`로 분리했다.
- [x] 레거시 `ItemDataSO`와 개별 아이템 에셋을 제거했다.
- [x] 런타임·Editor C# 빌드를 통과했다.
- [x] 실제 CSV 13개 스모크 테스트와 잘못된 Item ID 거부를 확인했다.
- [x] 비개발 직군용 작성 가이드를 완성했다.
- [ ] Unity Test Runner와 Play Mode 회귀 검증을 완료한다.
- [ ] `.meta` 추적 정책을 해결하고 목적별 Commit을 생성한다.
