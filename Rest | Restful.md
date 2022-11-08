# Rest 와 Restful
## Rest
“Representational State Transfer” 의 약자이다.   
분산시스템 설계를 위한 소프트웨어 아키텍처의 하나로서 
웹에 존재하는 모든 자원(이미지, 동영상, DB 자원)에 고유한 URI를 부여해 활용하는 것으로, 자원을 정의하고 자원에 대한 주소를 지정하는 방법론을 의미한다고 한다.

## Rest 구성요소
* Resource (자원), URL   
모든 자원은 고유한 ID를 가지고 ID는 서버에 존재하고 클라이언트는 각 자원의 상태를 조작하기 위해 요청을 보낸다. HTTP에서 이러한 자원을 구별하는 ID는 ‘Students/1’ 같은 HTTP URI 이다.

* Verb (행위), Method   
클라이언트는 URI를 이용해 자원을 지정하고 자원을 조작하기 위해 Method를 사용한다. HTTP 프로토콜에서는 GET , POST , PUT , DELETE 같은 Method를 제공한다.

* Representation (표현)   
클라이언트가 서버로 요청을 보냈을 때 서버가 응답으로 보내주는 자원의 상태를 Representation이라고 한다. REST에서 하나의 자원은 JSON , XML , TEXT , RSS 등 여러 형태의 Representation으로 나타낼 수 있다.

## Rest 특징
* Server-Client (서버-클라이언트 구조)   
자원이 있는 쪽이 Server, 자원을 요청하는 쪽이 Client가 되어 서로 간 의존성이 줄어든다.   
REST Server : API를 제공하고 비즈니스 로직 처리 및 저장을 책임진다.   
Client: 사용자 인증이나 context(세션, 로그인 정보) 등을 직접 관리하고 책임진다.   

* Stateless (무 상태)   
REST는 무상태성 성격을 갖는다. 작업을 위한 상태정보를 따로 저장하고 관리하지 않는다. 
세션 정보나 쿠키정보를 별도로 저장하고 관리하지 않기 때문에 API 서버는 들어오는 요청만을 단순히 처리하면 되기 때문에 서비스의 자유도가 높아지고 서버에서 불필요한 정보를 관리하지 않음으로써 구현이 단순해 진다.

* Cacheable (캐시 처리 가능)   
HTTP라는 기존 웹표준을 그대로 사용하기 때문에, 웹에서 사용하는 기존 인프라를 그대로 활용이 가능하다. HTTP가 가진 캐싱 기능이 적용 가능하다. 
HTTP 프로토콜 표준에서 사용하는 Last-Modified 태그나 E-Tag를 이용하면 캐싱 구현이 가능하다.

* 계층화   
REST 서버는 다중 계층으로 구성될 수 있으며 보안, 로드 밸런싱, 암호화 계층을 추가해 구조상의 유연성을 둘 수 있고 PROXY, 게이트웨이 같은 네트워크 기반의 중간매체를 사용할 수 있게 한다.

* Uniform Interface (인터페이스 일관성)   
URI로 지정한 자원에 대한 조작을 통일되고 한정적인 인터페이스로 수행한다. HTTP 표준에만 따른다면 모든 플랫폼에 사용이 가능하다.

* Self-descriptiveness (자체 표현 구조)   
동사(Method) + 명사(URI) 로 이루어져 있어 어떤 메서드에 무슨 행위를 하는지 알 수 있으며 REST API 자체가 매우 쉬워서 API 메시지 자체만 보고도 API를 이해할 수 있다.

## Rest API
REST 기반으로 서비스 API를 구현한 것으로 최근 대부분의 OpenAPI(누구나 사용할 수 있도록 공개된 API)는 REST API이다

# Restful

### 참고
https://hckcksrl.medium.com/rest란-c602c3324196   
https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html   
https://velog.io/@ellyheetov/REST-API   
https://yuricoding.tistory.com/79   
