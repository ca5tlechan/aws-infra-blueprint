# Project Overview: AWS Infrastructure Blueprint

이 문서는 aws-infra-blueprint 레포의 목적/범위와 산출물 구성을 요약한다.
목표는 AWS에서 서비스를 “배포 가능한 상태”로 만드는 것에서 끝내지 않고, 운영(모니터링/롤백/장애 대응/비용·보안 통제)까지 포함한 형태로 정리하는 것이다.

## Goal
- 재현 가능한 배포 절차와 운영 절차를 문서화한다.
- 기본적인 가용성/보안/비용 통제를 포함한 인프라 구성을 정리한다.
- 장애를 재현하고 Postmortem(RCA + 재발 방지)을 남긴다.

## Scope (In)
- EC2 기반 애플리케이션 배포(샘플 앱 포함)
- (추후) ALB + HTTPS(ACM) 구성
- (가능하면) Route53 도메인 연결
- RDS 연동(학습 범위 내 최소 구성)
- VPC 분리(Public/Private), 보안그룹 최소권한
- 모니터링(CloudWatch) + 알람 1~2개 구성
- 장애 1건 재현 및 Postmortem 작성
- 비용 가드레일(태그/정리 절차) 적용

## Out of Scope (Not now)
- 상용 수준의 완전한 규정 준수/감사 대응 체계
- 대규모 트래픽 성능 튜닝(별도 실험으로 확장 가능)
- 멀티 리전 DR(재해복구) 구성

## Deliverables
- Architecture: `docs/architecture/`
- ADR (decisions): `docs/adr/`
- Runbooks (procedures): `docs/runbooks/`
- Postmortems (RCA): `docs/postmortems/`
- Security notes: `docs/security/`
- Cost guardrails: `docs/cost/guardrails.md`
- Scripts: `scripts/`
- Sample app: `app/`

## Working Agreement
- `main` 브랜치에는 직접 커밋하지 않는다. (`feature/*` → PR → merge)
- 민감정보(AWS 키/토큰, .env, 키 파일)는 레포에 커밋하지 않는다.
- 실습 리소스는 태그 규칙을 따르고, 종료 후 정리 절차를 수행한다.

## Notes
- 태그 규칙과 비용 정리 절차는 `docs/cost/guardrails.md`를 따른다.
- 문서는 “따라 할 수 있는 수준”으로 작성하고(절차/검증/롤백 포함), 변경 시 ADR로 근거를 남긴다.
