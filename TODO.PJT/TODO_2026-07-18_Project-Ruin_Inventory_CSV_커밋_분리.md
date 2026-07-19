# TODO

- 이름: Project-Ruin Inventory CSV 변경 Commit 분리
- 유형: 작업
- 분류: Project-Ruin / Git / 리뷰
- 출처: Inventory CSV 마이그레이션
- 세부 정보: 검증이 끝난 변경을 런타임, 데이터·Prefab, 테스트, 문서 목적별 Commit으로 분리한다.
- 완료 여부: 미완료
- 긴급도: 4
- 가치: 4
- 예상 달성 시간: 1시간
- 제한/유효 기간: `.meta` 정책과 Unity 회귀 검증 후

## 세부 완료 요구 사항

- [ ] 포함 파일과 삭제 파일 전체를 다시 확인한다.
- [ ] 런타임 전환 Commit을 만든다.
- [ ] 데이터와 Prefab 이관 Commit을 만든다.
- [ ] 검증기와 회귀 테스트 Commit을 만든다.
- [ ] 제작 문서와 작업일지 Commit을 만든다.
- [ ] 각 Commit 제목과 실제 변경 범위를 일치시킨다.

## 실행 메모

- `.meta` 정책 변경은 Inventory 기능 Commit과 섞지 않는다.

## 미완료 시 처리

- 처리 방식: 보류
- 사유: 선행 `.meta` 정책과 Unity 검증이 끝나야 안전하게 범위를 확정할 수 있다.
- 다음 행동: 두 선행 TODO의 완료 여부를 확인한다.
