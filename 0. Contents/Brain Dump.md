- make TCP checksum MD5

- 제 과제에서는 index :: fragment가 정상적으로 안되는데 결국 원인을 못 찾았습니다.
- AWS에 배포할 때 보안 그룹에 설정한 규칙에 대해 자세히 알고 싶습니다. (왜 해당 규칙들인지)
- JWT를 쿠키로 주고 헤더로 받는 것이 안전한가요? (헤더/쿠키 혼용의 이유 혹은 어떤 쪽이 더 나은지)
- 일전 면접에서 코드에 대한 피드백으로 JWT은 매번 사용자 정보 조회하는 트랜잭션이 발생하면 의미가 없다고 들었는데, 이번에 구현한 과제에서 JwtAuthorizationFilter에서 매번 트랜잭션이 발생하게 되는 것을 보이는데 해당 부분에 대한 의견이 궁금합니다.