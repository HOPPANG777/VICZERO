# 장기 프로젝트

- 이름: Project-Ruin
- 이전 이름: RuinConservator
- 프로젝트 성격: 팀 프로젝트 / Unity 게임 개발
- 목적 및 방향성: 기획자와 개발자가 안정적으로 콘텐츠를 제작·검증·공유할 수 있는 데이터 중심 Unity 게임 프로젝트를 완성한다.
- 달성 목표: 핵심 게임 시스템, CSV 제작 파이프라인, 팀 협업 규칙, 검증과 배포 기반을 단계적으로 완성한다.
- 진행 기간: 2026-07-15 ~ 진행 중
- 목표 기간: 장기 / 종료일 미정
- 상태: 진행 중
- 중단 조건: 팀 합의로 프로젝트 종료 또는 장기 보류가 결정될 때
- 다음 점검일: 2026-07-25

## 이름 변경 기록

- 기존 프로젝트 이름 `RuinConservator`가 `Project-Ruin`으로 변경됐다.
- 이전 이름으로 작성된 작업과 현재 `Project-Ruin` 작업은 같은 장기 프로젝트의 기록으로 취급한다.
- Unity 메뉴나 내부 도구에 남아 있는 `Ruin Conservator` 표기는 프로젝트명과 별개의 기존 제품·도구 표기일 수 있으므로, 실제 변경 범위를 확인한 뒤 수정한다.

## 마일스톤

| 순서 | 기간 | 완료 기준 | 상태 | 연결된 TODO 이름 | 연결된 TODO 데이터 |
|---|---|---|---|---|---|
| 1 | 2026-07 | GitHub 협업 가이드, Branch 보호, Issue·PR Template과 팀 연습 완료 | 진행 중 | GitHub 협업 규칙 실제 적용 | `DAY.PJT/2026-07-15`, 후속 설정 작업 |
| 2 | 2026-07 | Dialogue·Quest·Inventory CSV 제작 흐름과 Unity 회귀 검증 완료 | 진행 중 | Inventory CSV 전환 마감 | `DAY.PJT/2026-07-18`, `TODO.PJT/TODO_2026-07-18_Project-Ruin_Inventory_CSV_Unity_회귀검증.md` |
| 3 | 2026-07 ~ 미정 | 유적 재건 기반과 30% 복원 수직 슬라이스 완료 | 진행 중 | 유적 재건 Unity 검증 및 기획 확정 | `DAY.PJT/2026-07-22`, `TODO.PJT/TODO_2026-07-22_Project-Ruin_유적_재건_Unity_검증.md` |
| 4 | 미정 | 핵심 게임 루프와 저장·로드를 플레이 가능한 단위로 통합 | 미완료 | 핵심 시스템 통합 | 추후 생성 |
| 5 | 미정 | 팀원이 새 환경에서 Clone 후 실행·검증·콘텐츠 추가 가능 | 미완료 | 협업 및 배포 준비 | `.meta` 정책과 전체 참조 검증 |

## 현재 완료된 주요 작업

- GitHub 초보 기획자와 개발자를 위한 Issue·PR 중심 협업 규약 설계
- Inventory 원본 데이터를 `ItemDataSO`에서 CSV Definition 구조로 전환
- Item, Localization, Quest 사이의 교차 참조 검증 추가
- 비개발 직군용 Inventory CSV 작성 가이드 작성
- 런타임·Editor C# 빌드 및 실제 CSV 스모크 테스트 통과
- 기술 획득·반납, 재건도 계산, ES3 저장과 최소 제단 UI 기반 구현

## 현재 핵심 위험

- `.gitignore`의 `*.meta` 규칙으로 신규 Unity 참조 파일이 팀 저장소에 안전하게 전달되지 않을 수 있다.
- Inventory CSV 전환의 Unity Test Runner, Play Mode, 기존 세이브 복원 검증이 남아 있다.
- 구현 변경이 아직 목적별 Commit으로 정리되지 않았다.
- 유적·제단 콘텐츠 기획과 Unity Test Runner·Play Mode 검증이 남아 있다.

## 내려보낼 TODO

- [x] Unity `.meta` 추적 정책 정리 TODO 생성
- [x] Inventory CSV Unity 회귀 검증 TODO 생성
- [x] Inventory CSV 변경 Commit 분리 TODO 생성
- [x] 실제 아이콘 카탈로그 연결 TODO 생성

## 연결 기록

- GitHub 협업 규약: `DAY.PJT/2026-07-15`
- Inventory CSV 전환: `DAY.PJT/2026-07-18`
- 유적 재건 기반 구현: `DAY.PJT/2026-07-22`
- 지식 기록: `EXP.DATA/개발협업/GitHub`, `EXP.DATA/게임개발/Project-Ruin`
