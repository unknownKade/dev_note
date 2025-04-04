- Entropy(무질서한 정도)에 대응하기 위해 디자인 패턴 사용
- 변화에 유연하게 대처하기 위해 기준을 정의하는 것 = 변화를 고려한 설계
- 로직 한데 뭉쳐 있거나, 책임이 분리되지 않는 구조
	- 유닛테스트하기 쉬워짐
- 공통 구조는 재사용
- 프레임워크에 위임된 한계를 깨기 위해-> 스프링에 이미 수많은 디자인패턴 내장됨

### 핵심 개념
- 추상화(Abstraction)
	- 추상 팩토리,
- 관심사의 분리(Seperation of Concerns)
	- mvc, 전략패턴, aop, spring transaction
- 느슨한 결합(Loose Coupling)
	- observer pattern, 중재자 패턴
- 코드 재사용
- 개방 ㅍㅖ쇄
- 행동 위임(Delegation)
	- Composition(has-a) over Inheritence 컴포지션을 통한 기능 확장을 하면 상속의 강한 커플링 없음 ``class Order extends
	- 상태, 전략 패턴
- 변경 격리(Isolating Changes)
	- 특정 컴포넌트로 격리(인프라)
- 상태 관리(State management)


### SOLID
- 단일 책임(SRP) : 
- 개방-폐쇄(OCP): 확장에는 열려 있고
- 리스코프 치환 원칙(LSP)
- 인터페이스 분리 원칙(ISP)
- 의존성 역전 원칙(DIP)

## 생성 패턴


## 구조 패턴
- Facade : 복잡한 서브 시스템에 단순화된 인터페이스 제공
- Proxy : 

## 행위 패턴(Behaviorial Pattern)
- Strategy Pattern(전략 패턴)
	- 행동(알고리즘)을 캡슐화하여 동적으로 바뀌는 디자인 패턴
	- refactoring 기법 중 extract method ->extract class 고려 
- 전략 패턴 잦은 실수
	- 전략을 너무 세부화
	- 분리의 목적이 뚜렷해지기 전에 굳이 분리 하지 말자(don't overengineer)
``` java
interface PaymentStrategy{
	void processPayment(int amount);
}

class NaverPayStrategy implements PaymentStrategy{
	@Override
	void processPyament(){
	}
}

class BankingStrategy implements PaymentStrategy{
	@Override
	void processPyament(){
	}
}
```

## Template Method Pattern
- 구조를 정의하고 세부 구현은 서브 클래스에 위임
	- 변경 가능한 메소드는  추상 메소드
	- 알고르짐의 제어 흐름은 부모 클래스가 담당
	- primitiveOperations 은 무조건 구체 구현, hook Methods은 선택 구현