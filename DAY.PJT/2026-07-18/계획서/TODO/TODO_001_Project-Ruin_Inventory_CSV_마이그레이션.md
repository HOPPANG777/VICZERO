# TODO

- 이름: Project-Ruin Inventory CSV 마이그레이션
- 유형: 작업
- 분류: 게임 개발 / Unity / 데이터 파이프라인
- 출처: `LNG.PJT/Project-Ruin.md`
- 세부 정보: Inventory의 기획 데이터를 CSV로 통합하고 Unity 참조, 런타임 조회, Quest, UI, 검증과 문서를 함께 전환한다.
- 완료 여부: 부분 완료
- 긴급도: 5
- 가치: 5
- 예상 달성 시간: 2시간 이상
- 제한/유효 기간: 2026-07-18 ~ 후속 검증 완료 시

## 세부 완료 요구 사항

- [x] 런타임 코드와 데이터 이관
- [x] GameRoot Prefab과 ItemVisualCatalog 연결
- [x] Editor 검증기와 회귀 테스트 코드 갱신
- [x] C# 빌드 및 CSV 스모크 테스트
- [x] 기획자용 Inventory CSV 작성 가이드
- [ ] Unity Test Runner 실행
- [ ] Play Mode 지급·소모·UI·저장 복원 확인
- [ ] `.meta` 추적 정책 해결
- [ ] 목적별 Commit 생성

## 실행 메모

- 구현 단계의 완성도는 높지만 팀 저장소 반영과 실제 Unity 동작 확인이 남아 있어 전체 완료로 처리하지 않는다.

## 미완료 시 처리

- 처리 방식: 재분해
- 사유: `.meta`, Unity 회귀 검증, Commit, 아이콘은 서로 다른 완료 조건과 위험을 가진다.
- 다음 행동: TODO.PJT의 네 후속 작업으로 각각 처리한다.
