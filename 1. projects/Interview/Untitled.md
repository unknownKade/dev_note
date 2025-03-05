 ## Java
- Java Bean/ Spring Bean
	- 자바 빈은 
- SOLID
	- Single Responsibility - 단일 책임 원칙은 각 객체는 한 가지 책임만을 가져야하는 원칙
	- Open Close - 변화에는 닫혀있고 확장에는 열려 있어야한다
	- Liskov Substitution Principle - 자식 객체를 부모 객체로 교환해도 정상적으로 작동해야한다
	- Interface Seperation - 쓰지 않는 외부 메소드에 의존해선 안된다. 필요한 단위로 인터페이스로 쪼개야한다
	- Dependency Inversion - 자기보다 구체적인 것에 의존해선 안된다. 구현 클래스에 의존하지 않고 인터페이스를 통해야한다
- Serialize
## Spring

- IoC/ DI/ IoC Container
  
- Spring Bean 등록, Scope, lifecycle
	- 스프링 빈은 기본적으로 Component 어노테이션으로 등록할 수 있고 어떤 컴포넌트인지에따라 @Controller, @Service, @Repository 같이 구체적인 용도의 빈은 따로 어노테이션이 마련되어 있기도하다.
	- 그 외에 스프링 설정을 할 수 있는 @Configuration어노테이션을 붙인 클래스에서는 @Bean 어노테이션으로 메소드만으로도 빈을 등록 할 수 있다.
	- 스프링을 올릴때 componentScan을 통해 어노테이션이 붙은 설정과 빈을 찾아 빈을 만들어 스프링 컨테이너에 등록한다.
	- @postContruct @PreDestroy를 통해 빈의 생명주기를 임의로 변경 할 수 있다
	- 빈의 생명중기  IoC 컨테이너 생성 -> 스프링 빈 생성 -> 의존성 주입 ->초기화 콜백 메소드 호출  -> 사용 -> 소멸 콜백 메소드 호출 -> 스프링 종료
	- 빈이 존재할 수 있는 범위(scope)를 singletone, porotoype, request, session, applicaiton으로 설정할 수 있다.
- Dispatcher Servlet/ HandlerMapping/ Handler Adapter/ View Resolver
	- 
- Spring filter/ Interceptor
	- 
- 스프링 의존성 생성자 주입/ 필드 주입/ 수정자 주입
	- 생성자를 통해 주입하는 경우 해당 빈의 생성자에 의존성을 변수로 줘서 final 멤버로 주입한다.
	- 필드 주입은 @Autowired 어노테이션을 사용해서 주입하는 것인데

- MVC pattern
	- 
- Layered architecture

## JPA
- 트랜잭션 격리
- 지연로딩 프록시
- 영속성 컨텍스트/flush/dirty checking
	- 엔티티를 트랜잭션 단위로 저장하고있는 단위 
	-  flush는 영속성 컨텍스트 상의 엔티티 데이터와 DB의 데이터를  맞추는데 사용. 트랜잭션을 커밋하는 경우나 JPQL 쿼리가 실행되는 경우 호출된다 
	- empty로 영속성 컨텍스트 비울 수 있다
	- dirty checking은 트랜잭션이 종료되는 시점에서 변화를 감지해서 DB에 반영하는 기능
- 
## DB
- Index [link](https://www.youtube.com/watch?v=iNvYsGKelYs)
	- 데이터베이스 지정한컬럼들의 데이터를 정렬해서 물리적 주소와 함께 따로 보관해서  검색 속도를 향상 시키는 자료구조로 주로 B+트리가 사용된다.
	- PK는 자동 인덱싱되고 클러스터드 인덱스라고한다
	- 쓰기/업데이트가 
- paritioning/sharding/replication  [link](https://www.youtube.com/watch?v=P7LqaEO-nGU)
	- partitioning 
		- vertical : 테이블의 가로(컬럼)을 기준으로 테이블을 나누는 것으로 정규화 같은 걸 말함 
		- horizontal : 테이블 row를 기준으로 테이블을 나누는 것으로 테이블 자체가 커지는 것을 막는것. 테이블이 커지면 인덱스 크기가 커져 느려진다. 데이터가 균등하게 나눠지게 hash/range등으로 parition key를 정하여 파티셔닝한다
- sharding
	-
[link](https://github.com/ksundong/backend-interview-question)