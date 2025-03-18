- 주문
	- 주문 생성  -> 배송 생성 이벤트
	- 주문 수정
	- 주문 취소
	- 
- map struct
- generationtype identity
- request를 커맨드로 바꿔주는건 컨트롤러에서(WebAdaptor)
- @Builder
@Mapper(componentModel = "spring")
- @EqualsAndHashCode @NoArgsConstructor(access = AccessLevel.Protected)
- request -> command -> entity -> domain -> web response
- persistence -> entity -> domain -> command -> out
- db replication
	- application-port-in 에 command 외에 query
- in.web.response - responsedto
- service 계층에서만 예외 던지기

- 모듈 간 통신
	- 보내는 모듈에선 Request/ResponseDTO
	- 받는 모듈에선 DomainInfo
``` java
// adaptor.out.client.<Domain>FeignClient.java //adaptor.out.client.<Domain>.<Domain>FeignClient.java (클라이언트가 많아지면 패키지 분리가능)
@FeignClient(name = "product-service")
public interface ProductFeignClient extends ProductInternalClient{ 
// 공통모듈에서 ProductInternalClient를 상속하므로 메서드를 정의하지 않아도 됨 
}

```

https://www.bucketplace.com/post/2021-12-30-msa-phase-1-api-gateway/
https://blog.logto.io/ko/rbac-in-practice

``` java
@FeignClient(name = "hub-service")
public interface HubFeignClient{
	@GetMapping("/internal/v1/hubs/{hubId}")
	HubResponse findById(@PathVariable("hubId") Long hubId);
}
```

![[Pasted image 20250318005749.png]]