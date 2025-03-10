- API Gateway는 클라이언트와 서버 사이 단일 진입지점으로 요청을 백엔드로 라우팅하고 인증,인가, 로드 밸런싱, 모니터링 로깅, 요청 응답 변환 등 처리를 담당한다.
- Spring Cloud Gateway는 Spring CLoud Netflix 패키지의 일부이며 MSA에 많이 사용되고 동적 라우팅, 필터링, 모니터링, 보안 등을 제공한다. 전체 필터링 Global Filter와 서비스별로 필터링하는 Gateway Filter가 있다.

### 필터

- Mono : 비동기적 처리 객체. Mono\<Void\>는 아무것도 반환하지 않음
- SeverWebExchange : HTTP 요청과 응답을 캡슐화한 객체 exchange.getRequest() 
- 