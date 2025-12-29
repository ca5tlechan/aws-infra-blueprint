# Postmortem: <Incident ID> (<YYYY-MM-DD>)

## 1) Summary
- 한 줄 요약:
- 심각도(예: Sev-3/Sev-2):
- 상태: Resolved / Monitoring / Open

## 2) Impact
- 사용자 영향: (예: 로그인 불가, 5xx 증가 등)
- 영향 범위: (예: 전체/일부 API/특정 AZ)
- 지속 시간: (시작~종료)
- 고객/비즈니스 영향: (가능하면 수치: 실패율, 지연시간, 요청수)

## 3) Timeline (KST)
> “관측/조치/복구” 중심으로 적는다.

| Time | Event |
|---|---|
| HH:MM | 감지(알람/사용자 제보/로그) |
| HH:MM | 1차 확인(지표/로그/헬스체크) |
| HH:MM | 원인 후보 좁힘 |
| HH:MM | 임시 조치(완화) |
| HH:MM | 근본 조치(수정) |
| HH:MM | 정상화 확인 |

## 4) Detection
- 어떻게 감지했나? (알람/대시보드/사용자 제보)
- 어떤 지표/로그가 신호였나?
- 감지까지 걸린 시간(MTTD): <분>

## 5) Root Cause (RCA)
- 직접 원인(Direct cause):
- 근본 원인(Root cause):
- 왜 이런 일이 가능했나? (구성/절차/검증 누락 등)

## 6) Resolution & Recovery
- 즉시 완화 조치(Mitigation):
- 근본 해결(Fix):
- 복구까지 걸린 시간(MTTR): <분>

## 7) What went well / What went wrong
### Went well
- 
### Went wrong
- 

## 8) Action Items (Prevention)
> “재발 방지”는 반드시 소유자/기한/상태를 둔다.

| Action Item | Owner | Due | Status |
|---|---|---|---|
| 예: SG 오픈 포트 점검 스크립트 실행을 배포 체크리스트에 추가 | <name> | YYYY-MM-DD | TODO |
| 예: CloudWatch 알람(5xx, target unhealthy) 추가 | <name> | YYYY-MM-DD | TODO |
| 예: 배포 런북에 검증 단계(health check) 강화 | <name> | YYYY-MM-DD | TODO |

## 9) Supporting Evidence
- 관련 대시보드/알람 스냅샷 경로:
- 관련 로그 위치(CloudWatch log group 등):
- 관련 PR/커밋:
- 관련 Runbook:
- 관련 ADR:
