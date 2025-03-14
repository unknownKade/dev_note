
## API 테스트

``` java
@SpringBootTest //실제 애플리케이션 다 갖고와서 느림.부분설정가능
@AutoConfigureRestApi
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
- 코드 가독성 보완 SomethingController implements SomethingControllerDocs 
- Spring RESTDocs
	- 언제나 API 일치
	- 문서 양식 작성 필요
	- TDD적합
	- 테스트 결과 출력 화면은 제공되지 않음
- RestDocs + Swagger = com.epages.restdocs-api-spec 0.19.2 

## 문서 보안

## 