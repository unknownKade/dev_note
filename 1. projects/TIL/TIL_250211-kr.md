## Cross-Origin Resources Sharing
클라이언트와 서버의 url이 다른 경우를 방지하는 것이  CORS 정책이다. 요즘 대부분 웹 서비스들은 서버와 클라이언트가 같은 오리진이 아니기 때문에 서버측에서 CORS 설정이 별도로 필요하다.

CORS 흐름
-  요청 헤더에는 해당 요청이 어디에서 왔는지 정보를 담은 Origin 값이 퐇마되어있다.
- 만약 서버와 클라이언트의 Origin url이 다른 경우를 cross-origin request으로 분류되어 CORS 정책에서 요청을 막는다. 보안상의 이유 때문에 구체적인 원인은 알려주지 않는다.
- 서버 측에서 허용해주는 url을 설정하여 그 정보를 헤더에 담을 수 있다.
	- ``Access-Control-Allow-Origin``: 허용되는 Origin. 와일드 카드(\*)인 경우 모든 Origin이 허용된다.
	- ``Access-Control-Allow-Methods``: 기본 허용 통신은 GET이며 추가적으로 허용하는 HTTP 메소드를 설정한다. 
	- ``Access-Control-Max-Age``:  클라이언트는 GET 외 메소드에 대해서는 서버에게 해당 요청에 대한 허가를 받는 preflight 요청을 보낸다. 받은 허가의 유효기간을 설정하는 헤더.