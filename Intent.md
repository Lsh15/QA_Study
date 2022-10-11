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


* Implicit Intents (암시적 인텐트)


### 참고
https://developer.android.com/guide/components/intents-filters   
https://velog.io/@skydoves/2022-android-developer-roadmap-part2   
