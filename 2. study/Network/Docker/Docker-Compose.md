

``` bash
docker-compose up

```


``` yaml

version: '3' #docker compose file version
services: 
  web:
    image: nginx
    ports:
      - "8080:80"
  app:
    build: .
    ports:
      - "8081:8080"
    depends_on: #creates after dependencies are created
      - db
  db:
    image: postgres 
     environment:
      POSTGRES_PASSWORD: example
      #MYSQL_ROOT_PASSWORD: root
      #TZ: Asia/Seoul
    #container_name: mysql-ramos
    #restart: always
    ports:
      - 3306:3306
    #volumes:
      #- ./mysql-init-files/:/docker-entrypoint-initdb.d
    #platform: linux/x86_64
```