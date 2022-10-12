# Intent (인텐트)
Intent는 메시징 객체로, 다른 앱 구성 요소로부터 작업을 요청하는 데 사용할 수 있다. 
## Use Cases of Intents (인텐트 사용 사례)
#### * Starting an activity (Activity 시작)
Intent를 startActivity() 메서드에 실행하여 새 Activity를 실행할 수 있다. Intent는 Activity의 수행 동작을 정의하고 새 Activity에서 사용해야 하는 데이터를 전달한다.

#### * Starting a service (Service 시작)  
Intent를 startService() 메서드에 전달하여 새 Service를 실행할 수 있다. Intent는 Service의 동작을 정의하고 새로운 Service에서 사용해야 하는 데이터를 전달한다.

#### * Delivering a broadcast (Broadcast Receiver 메시지 전달)   
sendBroadcast() 또는 sendOrderedBroadcast() 메서드에 Intent를 전달하여 Broadcast Receiver에 메시지를 전달할 수 있다. 다른 컴포넌트 또는 다른 앱에서 broadcast 메시지로 Intent를 전달할 수 있다.

## Intent Type (인텐트 유형)
#### * Explicit Intents (명시적 인텐트)   
Explicit Intents (명시적 인텐트)는 앱 내의 특정 액티비티나 서비스 등 특정한 앱 구성 요소를 시작하는 데 사용하는 Intent이다. Explicit Intents (명시적 인텐트)에는 앱의 패키지 이름 또는 컴포넌트의 클래스 이름과 같이 명시적인 정보가 포함되어야 한다.

#### * Implicit Intents (암시적 인텐트)    
Implicit Intents (암시적 인텐트)는 작업을 지정하여 기기에서 해당 작업을 수행할 수 있는 모든 앱을 호출할 수 있도록 한다. Implicit Intents (암시적 인텐트)를 사용하면 Android 시스템에서 시작할 적절한 구성 요소를 찾고, 해당 Intent와 일치하는 인텐트 필터가 있으면 시스템에서 해당 구성 요소를 시작하고 이를 Intent 객체를 전달한다. 호환되는 인텐트 필터가 여러 개인 경우, 시스템에서 대화상자를 표시하여 사용자가 어느 앱을 사용할지 직접 선택할 수 있게 한다.
 
#### * Intent Filters (인텐트 필터)   
Intent Filters (인텐트 필터)는 Intent의 작업, 데이터 및 카테고리를 기반으로 어느 유형의 Intent를 수락하는지 지정한다. 시스템은 Intent가 Intent Filters (인텐트 필터) 중 하나를 통과한 경우에만 Implicit Intents (암시적 인텐트)를 앱 구성 요소에 전달한다. 여러 가지 종류의 Intent를 처리하고자 하되 특정 조합의 작업, 데이터, 카테고리 유형으로만 한정하고자 할 때는 여러 Intent Filters (인텐트 필터)를 생성해야 한다.

## Pending Intent (보류 인텐트)   
PendingIntent는 Intent를 가지고 있는 클래스로, 기본 목적은 다른 앱(다른 프로세스)의 권한을 허가하여 가지고 있는 Intent를 본인 앱의 프로세스에서 실행하는 것처럼 사용하게 하는 것이다.

### * Pending Intent (보류 인텐트)의 사용 사례
* Notification으로 작업을 수행할 때 Pending Intent (보류 인텐트)를 사용한다. 
* 바탕화면의 위젯으로 Intent 작업을 수행할 때 Pending Intent (보류 인텐트)를 사용한다.
* AlarmManager를 통해 지정된 시간에 Intent가 시작되도록 할때 Pending Intent (보류 인텐트)를 사용힌다.



### 참고
https://developer.android.com/guide/components/intents-filters   
https://velog.io/@skydoves/2022-android-developer-roadmap-part2   
