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


### 참고
https://developer.android.com/kotlin/coroutines?hl=ko   
https://www.devkuma.com/docs/kotlin/coroutine/   
