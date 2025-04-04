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
	- Composition(has-a) over Inheritence 컴포지션을 통한 기능 확장을 하면 상속의 강한 커플링 없음 ``
	- 상태, 전략 패턴