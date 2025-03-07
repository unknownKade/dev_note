## Config
``` java
@Configuration  
public class RedisConfig {  
   @Bean  
   public RedisTemplate<String, ItemDto> itemDtoRedisTemplate(  
      RedisConnectionFactory connectionFactory  
  
   ){  
      RedisTemplate<String, ItemDto> template = new RedisTemplate<>();  
      template.setConnectionFactory(connectionFactory);  
      template.setKeySerializer(RedisSerializer.string());  
      template.setValueSerializer(RedisSerializer.json());  
      //template.setValueSerializer(new GenericToStringSerializer<>(Integer.class));  
      return template;  
   }  
  
   @Bean  
   public RedisSerializer<Object> springSessionDefaultRedisSearializer(){  
      return RedisSerializer.java();  
   }  
  
}
```
### ZsetOperations


``` java
@Service  
public class RankService {  
   private final ZSetOperations<String, ItemDto> rankOps;  
  
   public RankService(RedisTemplate<String, ItemDto> redisTemplate) {  
      this.rankOps = redisTemplate.opsForZSet();  
   }  
  
   public void increase(ItemDto itemDto){  
      //incrementScore inits if there is no key while add does not  
      rankOps.incrementScore(  
         "soldRanking",  
         itemDto,  
         1  
      );  
   }  
  
}
```