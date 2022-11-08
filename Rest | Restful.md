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

* Stateless (무 상태)

* Cacheable (캐시 처리 가능)

* 계층화

* Uniform Interface (인터페이스 일관성) 

* Self-descriptiveness (자체 표현 구조)

# Restful

### 참고
https://hckcksrl.medium.com/rest란-c602c3324196   
https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html   
https://velog.io/@ellyheetov/REST-API   
https://yuricoding.tistory.com/79   
