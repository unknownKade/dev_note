
- Docker Compose + Kafka + Web Socket + Spring Vertex

- LLM : Large Language Model 대규모 언어 모델
	- 트랜스포머 모델
	- 장점 : 광범위한 지식 활용, 뛰어난 언어 이해 및 생성 능력, 다양한 테스크 수행 가능
	- 단점 : 편향성 문제, 사실 관계 오류 가능성, 맥락 이해의 한계, 일관성 문제, 유닐적 문제
	- RAG(Retrieval-Augmented Generation 검색 증강 생성) 으로 LLM의 사실 관계 오류 가능성과 맥락 이해 한계 보완하려고 외부 데이터 소스에서 실시간 활용하여 증거 기반 생성 )LaMDA, Preplexity)
		- 질의 인코더로 변환

Kafka
- 링크드인이 스칼라로 개발한 오픈소스 메시지 브로커 프로ㅔㅈㄱ트로 높은 처리량, 낮은 지연시간을 목표로 하고 있음 확장 가능한 Pub/Sub 형태의 메시지 큐 구성
- 프로듀서가 메시지 생성해서 크러스터로 보내고 컨슈머가 소비한다
- 