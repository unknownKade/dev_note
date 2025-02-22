1. 전역설정은 같이
constants
config
util
yml - h2 in memory 활용
2.dto + controller push
1. entity + repo 진도 안나가면 도움
2. 각각 service 구현

빠르게 개발 후 리팩토링(최소 두번 추천)


도메인 기준을 명확할 것

entity에 dto 메소드 넣지 말것(계층 간 의존성 위반)
dto에 toEntty() , from(Entity entity) 추천
따로 Mapper 클래스 고려

객체 생성 시 빌더패턴 활용

클래스 내부  정적 팩토리 패턴 활용

stream / for

userdetails의 유저 정보
- 유저 조회한 이후에 UserDetails 에 정보 넣는 경우
- JWT 토큰에서 추출한 정보 UserDetails에 넣는 경우
- 실제 비즈니스로직이 작동되는 서비스단에서
- 활용 용도는 본인확인 등
- insert 할떄 등에는 다시 유저 조회해서 써야함


page 결과 리턴시 PageModel 사용

service가 다른 service 참조하지 않도록 강제 추천


dto 이름 