### Implementations
- redis/redis-stack
- redis/redis-stack-server
- redis insight 
### docker-compose
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
``` bash
SET user:count 1  
GET user:count  
#increase/decrease
INCR user:count  
DECR user:count  
#set multiple  
MSET user:name me user:email asdf@asdf.com  
MGET user:name user:email
#list : implemented as linked list. push pop like stack, queue
LPUSH user:list alex
RPUSH user:list max
LPOP user:list
RPOP user:list
LLEN user:list #length of list
LRANGE user:list 0 1000 #range bigger than list size doesn't return error
LRANGE user:list 0 -2
LRANGE user:list 2 0 #null list
#error when type is wrong but returns null for null type
GET user:null

#flush entire db
flushdb
```