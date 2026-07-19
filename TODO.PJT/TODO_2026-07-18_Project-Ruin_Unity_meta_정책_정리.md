# TODO

- 이름: Project-Ruin Unity `.meta` 추적 정책 정리
- 유형: 작업
- 분류: Project-Ruin / Unity / Git
- 출처: `LNG.PJT/Project-Ruin.md`, Inventory CSV 마이그레이션
- 세부 정보: `.gitignore`의 `*.meta` 규칙을 안전하게 정리하고 신규 Inventory 파일의 GUID 참조를 팀 저장소에서 보존한다.
- 완료 여부: 미완료
- 긴급도: 5
- 가치: 5
- 예상 달성 시간: 2시간 이상
- 제한/유효 기간: Inventory CSV Commit 전

## 세부 완료 요구 사항

- [ ] 별도 Issue와 Branch에서 작업한다.
- [ ] `*.meta` 제거 시 나타나는 전체 변경량을 검토한다.
- [ ] 신규 Inventory 파일과 Prefab 참조 GUID를 확인한다.
- [ ] `.meta` 변경을 기능 Commit과 분리한다.
- [ ] 다른 환경 또는 새 Clone에서 참조가 유지되는지 확인한다.

## 실행 메모

- 현재 Inventory 변경을 안전하게 Commit하기 위한 P0 선행 작업이다.

## 미완료 시 처리

- 처리 방식: 이월
- 사유: 미완료 상태에서는 신규 Unity 참조 파일의 팀 공유가 안전하지 않다.
- 다음 행동: 저장소 전체 `.meta` 현황을 먼저 목록화한다.
