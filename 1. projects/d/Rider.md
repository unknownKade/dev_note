개념 모델
context, aggregate
2차 SA

websocket Kafka 실시간 통신

[# DSM(Dependency Structure Matrix)](https://v0o0v.tistory.com/4)
[표현 계층 & 응용 계층의 DTO 네이밍 규칙](https://substantial-visage-888.notion.site/DTO-1ba861c68fb18092898dcc7f609da167)
[MSA에서 JWT 인증 및 인가 설계 가이드](https://substantial-visage-888.notion.site/MSA-JWT-1b9861c68fb18094addcde9ab5f8c782)

[대략적인 프로젝트 구조(모노 리포) 및 DDD 5대 개념 구현 예시](https://github.com/dannyseo9202/second-project-example)
[프로젝트2 가이드](https://substantial-visage-888.notion.site/2-1b2861c68fb180cc9a72d85aaaf2f4ba)


localhost:9093 : ui for apache kafka

```
server:

  port: 18081

  

jwt:
  secret: 3ce7f1ea6fa22a731c49f6e3b312bba19b07138faf89f2b8f3943da2c894e383
  access-token-expiration: 60000
  refresh-token-expiration: 600000
```