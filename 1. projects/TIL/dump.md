
- 직렬화는 언제 쓰는가
- 엔티티에서 원시타입 vs Wrapper 클래스
- VM options -Dserver.port=8081

https://github.com/dannyseo9202/second-project-example/blob/main/hub-service/src/main/java/sparta/project/logistics/hub/route/domain/model/RouteId.java

https://github.com/jinho-yoo-jack/wanted-preonboarding-challenge-backend-16/blob/master/src/main/java/com/wanted/preonboarding/hexagonal/account/adapter/out/web/persistence/entity/PerformanceEntity.java
- 도메인 서비스에서 밸류는 상태를 가지면 안된다
- 잘 설계된 MSA면 컨텍스트간 모놀리식처럼 데이터 일관성 보장 로깅,트레이싱, kafka 큐로 트랜잭션 순차적으로 처리 -> 통합이벤트 추천

- 담당과 공통 책임
- 통일성
- 품질 관심
- 일정 보수적
- 도메인간 소통


- 모노 레포 멀티 모듈
- 메시징으로 update 하는 경우 -> kafka 브로커에서 멱등성 키로 비교를 해서 보장한다, 멱등적 소비적 패턴으로 구현
- SAGA 패턴, Outbox Pattern
- @ElementCollection
- 외부에 공개하는건 build/resources/main/static/ 아래로