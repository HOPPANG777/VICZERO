# TODO

- 이름: Project-Ruin Inventory CSV Unity 회귀 검증
- 유형: 작업
- 분류: Project-Ruin / Unity / 테스트
- 출처: Inventory CSV 마이그레이션
- 세부 정보: 컴파일과 스모크 테스트 이후 남은 Unity Editor, Play Mode, 세이브 호환성을 검증한다.
- 완료 여부: 미완료
- 긴급도: 4
- 가치: 5
- 예상 달성 시간: 1시간
- 제한/유효 기간: Inventory CSV Commit 전

## 세부 완료 요구 사항

- [ ] CSV 데이터 검증기 Error 0개를 확인한다.
- [ ] Edit Mode `GameDataCsvRegressionTests`를 실행한다.
- [ ] Coin 100개 보상 지급과 RepairKit 1개 소모를 확인한다.
- [ ] 이름, 설명, 수량, `new` 표시와 탭 노출을 확인한다.
- [ ] 저장 후 재실행하여 기존 슬롯 복원을 확인한다.
- [ ] 삭제되거나 잘못된 Item ID의 처리 결과를 기록한다.

## 실행 메모

- Unity Editor가 열려 있어 Batch Mode 테스트를 실행하지 못한 항목을 마감한다.

## 미완료 시 처리

- 처리 방식: 이월
- 사유: 실제 Unity 동작 확인 전에는 마이그레이션 완료로 판정할 수 없다.
- 다음 행동: 열린 Unity 프로젝트에서 메뉴 검증기부터 실행한다.
