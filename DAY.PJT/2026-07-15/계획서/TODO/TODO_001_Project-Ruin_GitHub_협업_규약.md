# TODO

- 이름: Project Ruin GitHub 협업 규약 설계
- 유형: 작업
- 분류: 개발 협업 / GitHub / Unity
- 출처: Project Ruin
- 세부 정보: 현재 저장소와 개인 작업 습관을 분석하여 기획자와 개발자가 함께 사용할 Issue·PR 중심의 협업 규약을 작성한다.
- 완료 여부: 완료
- 긴급도: 4
- 가치: 5
- 예상 달성 시간: 2시간 이상
- 제한/유효 기간: 2026-07-15

## 세부 완료 요구 사항

- [x] 저장소 설정과 기존 Branch·Commit 패턴을 조사한다.
- [x] 개인 습관과 팀 규약의 차이를 설명한다.
- [x] 역할별 GitHub 사용 범위를 정한다.
- [x] Issue부터 Squash merge까지의 흐름을 정의한다.
- [x] Unity `.meta`, Scene, Prefab, LFS 위험을 기록한다.
- [x] 초보자도 따라 할 수 있는 협업 가이드를 작성한다.

## 실행 메모

- 핵심 산출물 `GITHUB_COLLABORATION_GUIDE.md`를 작성하고 Commit `a698db0`으로 반영했다.
- `.gitignore`가 약 15,871개의 `.meta`를 무시하는 중대한 위험을 발견했다.
- Commit 재검토 과정에서 문서 작업과 Unity 설정 변경이 한 Commit에 섞인 문제를 스스로 찾아냈다.

## 미완료 시 처리

- 처리 방식: 본 작업 완료, 후속 작업 분리
- 사유: 규약 설계와 문서화는 끝났지만 저장소 보호 설정과 `.meta` 복구는 별도 검증이 필요한 작업이다.
- 다음 행동: `.meta` 문제를 P0 작업으로 먼저 해결하고, Branch 보호와 Issue·PR Template을 실제 저장소에 적용한다.
