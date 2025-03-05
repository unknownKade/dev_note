
### 인메모리 데이터베이스
- RAM에 저장하는 인메모리는 **휘발성** 데이터고 영속성과 일관성보다 **확장성** **유연성**을 초점에 초점을 둔다
- NoSql DB 
	- 관계형 DB의 SQL를 사용하지 않고 **비정형 데이터**를 주로 다룬다
	- 관계형 DB가 일관성 때문에 확장성 유연성이 떨어지는 것을 보완
	- 다양한 종류가 있음
		- Redis : key-value
		- MongoDB: Document
		- Cassandra : Column Family

## Redis
- redis/redis-stack
- redis/redis-stack-server
- redis insight 
- docker-compose
``` yaml
services:  
  redis-stack:  
    image: redis/redis-stack  
    container_name: sparta-redis  
    restart: always  
    #set redis default user deafult's password as systempass
    command: ["redis-server","--requirepass", "systempass"]
    ports:  
      - 6379:6379  
      - 8001:8001
 
```

- redis cli
``` redis
set some-key:1234 value1
get some-key:1234
```