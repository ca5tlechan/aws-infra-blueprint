# Cost Guardrails (비용 가드레일)

## 원칙
1) 실습 리소스는 반드시 태그를 단다.
2) 매 실습 종료 시 "정리 체크리스트"를 수행한다.
3) 과금 위험 리소스(ALB/RDS/NAT 등)는 사용 시간을 짧게 가져간다.
4) AWS Access Key를 레포에 절대 저장하지 않는다.

## 태그 규칙(필수)
- Project=aws-infra-blueprint
- Owner=<your-name>
- Env=dev
- Expiry=YYYY-MM-DD

## 과금 위험 리소스(주의)
- ALB, RDS, NAT Gateway, EIP, CloudWatch(로그/메트릭 과다), 데이터 전송

## 매일/실습 종료 후 정리 체크리스트
- [ ] 사용하지 않는 EC2 인스턴스 중지/종료
- [ ] 사용하지 않는 ALB/Target Group 삭제
- [ ] RDS 인스턴스 중지/삭제(학습 후 즉시 정리)
- [ ] NAT Gateway/EIP 생성 여부 확인 후 삭제
- [ ] 스냅샷/AMI 불필요하면 삭제
- [ ] CloudWatch 로그 그룹/알람 과다 생성 여부 확인
- [ ] Route53 레코드 정리(테스트용)

## (예정) 자동 정리 스크립트
- scripts/cleanup.md 또는 scripts/cleanup.sh에 Project 태그 기반 정리 절차를 고정한다.
