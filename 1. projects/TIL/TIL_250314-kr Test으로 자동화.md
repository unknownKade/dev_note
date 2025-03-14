
## API 테스트

``` java
@SpringBootTest //실제 애플리케이션 다 갖고와서 느림.부분설정가능
@AutoConfigureMockMVC // 환경 모킹으로 HTTP 요청/응답 모의 검증 가능
@Transactional //각 메서드마다 롤백
@ActiveProfiles("dev") //application-dev.yml
public class AuthControllerApiV1TestTemp{
	
	@Test
	public void testArticleGetByIdSuccessByNoAuth() throws Exception{	
		mockMvc.perfom(
			MockMvcRequestBuilders.get("/v1/{id}", 2L);
		)
		.andExpectAll(
			MockMvcResultMatchers.status.isOk(),
			//MockMvcResultMatchers.status.isBadRequest(),
			//MockMvcResultMatchers.jsonPath("$.message).value("smth went wrong")
		)
	}
	

	//test마다 로그인을 객체로 전달
	private MvcResult login()
	
	@Test
	public void somePostTest() throws Exception{
		RestDTO<ResAuthPostLoginDTOApiV1> resLoginDto = objectMapper.readValue(
		login().getResposne().getRContentAsString(), new RypeReference<>(){}
		);
		mcokMvc.perform(MockMvcRequestBuilder.post("/v1/auth"))
	
	}
}
```
- 더미 데이터 data.sql이나 코드로 추가
``` java
@Configuration
@Profile("dev") //dev일때만 빈 등록
public class DataLoader{
	@Bean
	public CommandLineRunner laodData(UserRepository userRepository){

	}
```


## Swagger


## RestDoc


## 문서 보안

## 