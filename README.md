# aws-infra-blueprint

AWS에서 서비스 운영을 가정한 인프라 블루프린트와 운영 문서(ADR/Runbook/Postmortem), 비용·보안 가드레일을 포함합니다.

## What’s inside
- `docs/architecture/` : 아키텍처 다이어그램, 트래픽 흐름 정리
- `docs/adr/` : 설계/운영 의사결정 기록(ADR)
- `docs/runbooks/` : 배포/롤백/장애 대응 절차서
- `docs/postmortems/` : 장애 분석(RCA) 및 재발 방지 항목
- `docs/security/` : 보안 체크리스트 및 기본 원칙
- `docs/cost/guardrails.md` : 비용 가드레일(태그/정리 원칙)
- `scripts/` : 점검/정리 자동화 스크립트(예정)
- `app/` : 샘플 애플리케이션(예정)

## Working agreement
- `main` 브랜치에는 직접 커밋하지 않습니다. (`feature/*` → PR → merge)
- 민감정보(AWS Access Key/Secret, .env, 키 파일)는 절대 커밋하지 않습니다.
- 실습 리소스는 태그 규칙을 따르고, 작업 종료 후 정리 절차를 수행합니다.
