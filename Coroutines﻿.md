# Coroutines
Coroutine은 비동기적으로 실행되는 코드를 간소화하기 위해 Android에서 사용할 수 있는 동시 실행 설계 패턴이다. Android에서 Coroutine은 기본 스레드를 차단하여 앱이 응답하지 않게 만들 수도 있는 장기 실행 작업을 관리하는 데 도움이 된다.

## 기능
* 경량: Coroutine을 실행 중인 스레드를 차단하지 않는 정지를 지원하므로 단일 스레드에서 많은 Coroutine을 실행할 수 있다. 
* 메모리 누수 감소: 구조화된 동시 실행을 사용하여 범위 내에서 작업을 실행합니다.
* 기본으로 제공되는 취소 지원: 실행 중인 Coroutine 계층 구조를 통해 자동으로 취소가 전달됩니다.
* Jetpack 통합: 많은 Jetpack 라이브러리에 Coroutine을 완전히 지원하는 확장 프로그램이 포함되어 있습니다.

## Gradle dependency 설정
Android 프로젝트에서 Coroutine을 사용하려면 앱의 build.gradle 파일에 다음 종속 항목을 추가해야 한다.
``` kotlin
dependencies {
    implementation("org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.9")
}
```

## Coroutines 기초
Coroutine에서는 thread를 block(점유)하는 대신 처리를 suspend(중단)한다. 
* block   
block은 스레드를 점유한다. 점유를 하게 되면 thread로 처리를 진행할 수 없게 된다.
* suspend   
suspend는 coroutine 처리를 중단하고 thread를 해제한다. 해제하는 동안 다른 처리에 리소스를 활용할 수 있다.

Coroutine에서 만들어진 thread을 직접 제어하지 않고 Dispatchers를 통해서 제어한다. Dispatchers에 coroutine을 보내기만 하면 Dispatchers는 thread에 coroutine을 분산 시킨다.
* Dispatchers.Main   
메인 스레드로서 화면 UI와 상호작용 작업 등을 하는 Dispatchers
* Dispatchers.IO   
네트워크, DB 등 백그라운드에서 필요한 작업을 하는 Dispatchers
* Dispatchers.Default   
CPU를 많이 사용하는 정렬이나 무거운 계산 작업 등을 하는 Dispatchers

Dispatchers에 coroutine을 붙이는 메서드는 2가지가 있다.
* lanuch   
즉시 실행되고, 실행결과는 반환하지 않는다.   
관리를 위한 Job객체를 반환한다.   
join을 통해서 완료를 대기할 수 있다.
* async   
결과나 예외를 반환한다.   
실행결과는 Deferred<T>를 통해서 반환하며 await을 통해서 받을 수 있다.   
await은 작업이 완료될때까지 기다린다.
    
### 참고
https://developer.android.com/kotlin/coroutines?hl=ko   
https://www.devkuma.com/docs/kotlin/coroutine/   
https://todaycode.tistory.com/23    
https://kotlinworld.tistory.com/155?category=973476
