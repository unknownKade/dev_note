
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


```