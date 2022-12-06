# Kotlinx Serialization
kotlinx Serialization은 JetBrains에서 만든, Kotlin을 위한 JSON 라이브러리이다.   
Serialization는 응용 프로그램에서 사용하는 데이터를 네트워크를 통해 전송하거나 데이터베이스 또는 파일에 저장할 수 있는 형식으로 변환하는 프로세스이다.


## 특징
*	빠른 JSON 인코딩 & 디코딩을 지원   
Kotlinx Serialization의 새로운 버전이 출시하게 되면서 JSON 디코더를 다시 작성하고 JSON 인코더를 크게 최적화했기 때문에 이전 버전보다 직렬화 속도가 빨라졌다.

* 멀티플랫폼을 지원   
자주 사용되는 Gson과 Moshi는 모두 자바 라이브러리이므로, 자바를 지원하는 플랫폼(ex 안드로이드, Spring FrameWork 등)에서만 사용할 수 있습니다.   
Kotlinx Serialization 라이브러리는 자바, 자바스크립트, 네이티브(Kotlin/Native) 등 다양한 플랫폼을 지원하기떄문에 공용 라이브러리에 구현해서 사용할 수 있다.

* 코틀린을 지향    
Gson 라이브러리의 경우 타입이 없는 프로퍼티를 파싱할 경우 null 로 처리되어 null 이 아닌 프로퍼티가 null 값을 가지게 될 뿐 아니라, 프로퍼티의 기본값 조차 반영되지 않는 문제가 발생한다.   
kotlinx.serialization 라이브러리를 사용하면 JSON 문자열이 프로퍼티를 포함하고 있지 않음을 확인하고, null 대신 기본값을 대입한다. 따라서 개발자가 의도한 대로 파싱이 수행되는 것을 확인할 수 있다.

* 컴파일 안전을 보장   
kotlinx.serialization 라이브러리는 @Serializable 어노테이션이 있는 클래스만 직렬화(serialization)를 지원합니다.
직렬화를 수행할 수 없는 경우 런타임 에러 대신 컴파일 에러가 발생하므로 버그를 사전에 방지할 수 있다.

### 참고
https://kotlinlang.org/docs/serialization.html   
https://mashup-android.vercel.app/mashup-12th/jieun/kotlinx-serialization/   
https://tourspace.tistory.com/357   


