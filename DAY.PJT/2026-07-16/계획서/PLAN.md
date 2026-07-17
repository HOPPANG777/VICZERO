# 2026-07-16 계획서

- 날짜: 2026-07-16
- 오늘의 핵심 목표: Project-ZFC의 맵 생성 계약, 검증 책임, 결과 타입과 최종 소유권 정책을 확정한다.
- 실행 상태: 완료
- 원본 작업 문서: `D:/VicZero/Coding/Project-ZFC/ZFC-Documents/ZFC-Study/Project-ZFC_Map_Creation_Design_Study_2026-07-16.md`
- 선행 작업: 2026-07-13 Project-ZFC 맵 시스템 설계

## 오늘의 TODO

| 순서 | TODO | 완료 기준 | 상태 |
|---|---|---|---|
| 1 | Project-ZFC 맵 생성 계약과 소유권 설계 | 유효한 Map의 조건, 생성·검증 책임, 실패 결과와 소유권 전달 방식을 결정한다. | 완료 |

## 실행 순서

1. 7월 13일에 남긴 Map 생성 관련 질문을 다시 확인한다.
2. 빈 Map, 비정형 행, `TILE_NONE`에 대한 정책을 확정한다.
3. 구조 검증, 생성 품질 검증, 전투 배치 검증을 분리한다.
4. `TileGrid`, `TileLayout`, `Map`, `MapFactory`, `MapGenerator`의 책임을 정한다.
5. 생성 성공·실패 결과와 재시도 정책을 설계한다.
6. 완성된 Map의 최종 소유권과 읽기 참조 관계를 정한다.
7. 다음 구현 원칙과 순서를 별도 체크리스트로 연결한다.

## 완료 기준 확인

- [x] Map의 구조 불변 조건을 확정했다.
- [x] 유효하지 않은 Map이 생성되는 경로를 차단하도록 설계했다.
- [x] 예상 가능한 생성 실패와 구조적 오류를 구분했다.
- [x] `MapGenerationResult`와 `MapCreationResult`를 구분했다.
- [x] `CombatState`의 `unique_ptr<Map>` 단독 소유 정책을 정했다.
- [x] 구현 단계에서 지킬 원칙과 후속 체크리스트를 남겼다.
