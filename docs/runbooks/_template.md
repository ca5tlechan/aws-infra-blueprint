# Runbook: <Title>

## 1) Purpose
- 이 런북이 다루는 작업(배포/설정 변경/복구 등)의 목적과 기대 결과를 적는다.

## 2) Scope
- 대상 환경: (예: dev)
- 대상 컴포넌트: (예: EC2, ALB, RDS)
- 포함/제외 범위:
  - In:
  - Out:

## 3) Preconditions
- 사전 조건(권한/계정/네트워크/도구 설치 상태)을 적는다.
- 필요 권한:
- 필요 도구:
- 필요한 값(도메인/리전/인스턴스 ID 등):

## 4) Safety & Guardrails
- 비용/보안 관점에서 반드시 지켜야 하는 안전장치를 적는다.
- 태그 규칙(Project/Owner/Env/Expiry) 적용 여부 확인
- 민감정보(키/토큰/.env) 취급 원칙
- 실습 종료 후 정리(삭제/중지) 대상

## 5) Procedure (Step-by-step)
> 각 단계는 “무엇을 한다 → 왜 한다(한 줄) → 어떻게 확인한다”를 포함한다.

1. Step 1: <what>
   - Why:
   - Command / Console path:
   - Expected result:

2. Step 2: <what>
   - Why:
   - Command / Console path:
   - Expected result:

## 6) Verification (How to validate)
- 성공 여부를 판단할 “검증 방법”을 적는다.
- 기능 검증:
- 인프라 검증:
- 관측 지표(예: ALB 헬스체크, HTTP 200, CPU/Mem, 5xx 비율):

## 7) Rollback (If it fails)
- 실패 시 되돌리는 절차를 “최소 단계”로 적는다.
- 롤백 트리거 조건:
- 롤백 절차:
- 롤백 후 검증:

## 8) Observability / Logging
- 어디에서 로그/지표를 확인하는지 적는다.
- 로그 위치:
- 지표/알람:
- 확인해야 할 에러 패턴:

## 9) Common Issues & Fixes
- 자주 발생하는 문제와 1차 해결책을 적는다.
- Issue 1:
  - Symptom:
  - Cause:
  - Fix:
- Issue 2:
  - Symptom:
  - Cause:
  - Fix:

## 10) References
- 관련 문서/ADR/링크(레포 내부 경로)를 적는다.
- Related ADR:
- Related Postmortem:
- Related docs:
