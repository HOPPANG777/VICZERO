# 2026-07-13 계획서

- 날짜: 2026-07-13
- 오늘의 핵심 목표: Project-ZFC의 맵 시스템 책임과 자료 구조를 설계하고, 배운 내용을 다시 볼 수 있는 문서로 정리한다.
- 실행 상태: 완료
- 원본 작업 문서: `C:/Users/a0106/Documents/Project-ZFC_Map_Design_Study_2026-07-13.md`

## 오늘의 TODO

| 순서 | TODO | 완료 기준 | 상태 |
|---|---|---|---|
| 1 | Project-ZFC 맵 시스템 설계 학습 | Point, Map, TileType의 책임과 경계를 설명하고 다음 구현 순서를 정한다. | 완료 |

## 실행 순서

1. Map, Unit, CombatSystem, Renderer의 책임을 분리한다.
2. Point와 TileGrid의 자료형 및 접근 규칙을 정리한다.
3. Map의 질의 함수 계약과 불변 조건을 정의한다.
4. 작은 입력 사례로 경계 조건을 검토한다.
5. 결정하지 못한 문제와 다음 구현 순서를 남긴다.

## 완료 기준 확인

- [x] `Map`이 소유하는 데이터와 소유하지 않는 데이터를 구분했다.
- [x] `tiles[y][x]`, signed 좌표, `size_t`의 차이를 설명했다.
- [x] `GetSize`, `Contains`, `TileAt`, `IsWalkable`의 계약을 정리했다.
- [x] 정상 좌표와 범위 밖 좌표의 예상 결과를 작성했다.
- [x] 다음에 결정할 문제와 구현 순서를 작성했다.
