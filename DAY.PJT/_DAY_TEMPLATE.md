# DAY.PJT 날짜별 구조

```text
DAY.PJT/
  YYYY-MM-DD/
    계획서/
      PLAN.md
      TODO/
        TODO_001_이름.md
    보고서/
      REPORT.md
      REPORT-(TODO이름).md
```

## PLAN.md 역할

- 오늘 처리할 일정과 TODO를 배치한다.
- RE.PJT, LNG.PJT, TODO.PJT에서 오늘 실행할 것만 가져온다.
- 너무 많이 넣지 않고 실제 실행 가능한 양으로 제한한다.

## REPORT.md 역할

- 실행 결과, 미완료 사유, 다음 행동을 기록한다.
- 특정 TODO에 별도 분석이 필요하면 REPORT-(TODO이름).md를 추가한다.
