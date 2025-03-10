

``` bash
docker run -d --name rabbitmq -p5672:5672 -p 15672:15672 --restart=unless-stopped rabbitmq:management

spring.application.name=order

message.exchange=market
message.queue.product=market.product
message.queue.payment=market.payment

spring.rabbitmq.host=localhost
spring.rabbitmq.port=5672
spring.rabbitmq.username=guest
```
