# Compose 
Jetpack Compose는 네이티브 Android UI를 빌드하기 위한 최신 도구 키트이다.

## Compose를 사용해야 하는 이유
* 코드 감소   
작성하는 코드를 Kotlin과 XML로 나누지 않고 Kotlin으로만 작성하기 때문에 테스트와 디버그 작업과 버그 발생 가능성이 줄어들게 된다.   
Compose로 코드를 작성하면 빌드 중인 대상을 쉽고 간단하게 유지관리할 수 있다. Compose의 레이아웃 시스템은 개념적으로 더 단순하기 때문에 추론하기 쉬어 복잡한 구성요소의 코드도 쉽게 읽을 수 있다.

* 직관적   
Compose는 선언적 API를 사용하기 때문에 Compose가 나머지를 처리하므로 UI를 설명하기만 하면 된다. API는 직관적이므로 찾아서 사용하기가 쉽다.   
Compose를 사용하면 특정 활동이나 프래그먼트에 종속되지 않는 작은 스테이트리스(Stateless) 구성요소를 빌드한다. 이를 통해 재사용하고 테스트하기가 쉬워진다. 

* 빠른 개발 과정   
Compose는 기존의 모든 코드와 호환되고 Navigation, ViewModel, Kotlin 코루틴과 같은 대부분의 일반적인 라이브러리도 Compose와 함께 작동하므로 언제 어디서든 원하는 대로 채택할 수 있다.    
실시간 미리보기와 같은 기능을 포함해 전체 Android 스튜디오 지원을 사용하면 코드를 더 빠르게 반복하고 제공할 수 있다.

* 강력한 성능   
Material 디자인으로 빌드하든 자체 디자인 시스템으로 빌드하든, Compose를 사용하면 원하는 디자인을 유연하게 구현할 수 있다.
Compose를 사용하면 애니메이션을 통해 쉽고 빠르게 앱에 움직임과 생명을 불어넣을 수 있다. 

## @Composable Surface @Preview Modifiers Row Column Box


### 참고
https://developer.android.com/jetpack/compose/documentation      
