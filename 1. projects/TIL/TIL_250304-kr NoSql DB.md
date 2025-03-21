- 인메모리 데이터베이스 : RAM에 저장하는 인메모리는 **휘발성** 데이터고 영속성과 일관성보다 **확장성** **유연성**을 초점에 초점을 둔다

- NoSql DB 
	- 관계형 DB의 SQL를 사용하지 않고 **비정형 데이터**를 주로 다룬다
	- 관계형 DB가 일관성 때문에 확장성 유연성이 떨어지는 것을 보완
- NoSql DB types
	- Redis : key-value
	- MongoDB: Document
	- Cassandra : Column Family

- LSM(log-structured storage engine) Tree 사용으로 빠른 조회 성능 제공한다
	- append-only(끝에 데이터를 추가로 붙이는 것만 가능한) log file 기반으로 작동한다. 로그 파일이 append-only이므로 도중에 수정되지 않아 더 빠른 정리가 된다. 데이터의 추가 수정 삭제 등 변화를 기록한 이 로그파일을 취합해서 조회하여 빠른 조회가 가능하다
	- 