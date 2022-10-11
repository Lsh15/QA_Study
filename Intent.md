# Intent (인텐트)
Intent는 메시징 객체로, 다른 앱 구성 요소로부터 작업을 요청하는 데 사용할 수 있다. 
## Use Cases of Intents (인텐트 사용 사례)
* Starting an activity (Activity 시작)   
Intent를 startActivity() 메서드에 실행하여 새 Activity를 실행할 수 있다. Intent는 Activity의 수행 동작을 정의하고 새 Activity에서 사용해야 하는 데이터를 전달한다.

* Starting a service (Service 시작)  
Intent를 startService() 메서드에 전달하여 새 Service를 실행할 수 있다. Intent는 Service의 동작을 정의하고 새로운 Service에서 사용해야 하는 데이터를 전달한다.

* Delivering a broadcast (Broadcast Receiver 메시지 전달)   
sendBroadcast() 또는 sendOrderedBroadcast() 메서드에 Intent를 전달하여 Broadcast Receiver에 메시지를 전달할 수 있다. 다른 컴포넌트 또는 다른 앱에서 broadcast 메시지로 Intent를 전달할 수 있다.

## Intent Type (인텐트 유형)
* Explicit Intents (명시적 인텐트)   
Explicit Intents (명시적 인텐트)는 앱 내의 특정 액티비티나 서비스 등 특정한 앱 구성 요소를 시작하는 데 사용하는 Intent이다. Explicit Intents (명시적 인텐트)에는 애플리케이션의 패키지 이름 또는 컴포넌트의 클래스 이름과 같이 명시적인 정보가 포함되어야 한다.

* Implicit Intents (암시적 인텐트)    
Implicit Intents (암시적 인텐트)는 작업을 지정하여 기기에서 해당 작업을 수행할 수 있는 모든 앱을 호출할 수 있도록 한다. Implicit Intents (암시적 인텐트)를 사용하면 Android 시스템에서 시작할 적절한 구성 요소를 찾고, 해당 Intent와 일치하는 인텐트 필터가 있으면 시스템에서 해당 구성 요소를 시작하고 이를 Intent 객체를 전달한다. 호환되는 인텐트 필터가 여러 개인 경우, 시스템에서 대화상자를 표시하여 사용자가 어느 앱을 사용할지 직접 선택할 수 있게 한다.
 
* Intent Filters (인텐트 필터)   


### 참고
https://developer.android.com/guide/components/intents-filters   
https://velog.io/@skydoves/2022-android-developer-roadmap-part2   
