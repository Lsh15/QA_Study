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

## @Composable
Compose는 데이터를 UI 계층 구조로 변환하는 일련의 함수를 호출하여 UI를 구성하게 되는데, 이때 호출되는 함수는 @Composable이라는 애노테이션을 사용하여 선언하게 된다.    
@Composable을 사용하여 선언하는 함수를 Composable 함수라고 한다. Compose는 선언한 Composable 함수를 통해 시간이 지남에 따라 UI를 갱신하고 유지 관리할 수 있도록 한다.    
또한 @Composable 위에 @Preview(showBackground = true) 이라는 어노테이션을 추가하면 코드로 작성한 UI의 미리보기도 가능하다.

## Surface, Modifiers 
Surface 는 요소를 감싸는 컨테이너와 같은 역할을 하는 요소이다.      
Surface 를 사용해 텍스트의 컨테이너를 생성하고, 컨테이너에 색상을 부여하여 UI를 변동할 수 있다.

Modifier 파라미터를 사용하면 Surface, Text 와 같은 Compose UI 요소와 레이아웃, 색상 등의 스타일을 수정할 수 있게 해준다.    
Modifier는 스타일뿐만 아니라 클릭, 스크롤 여부 등의 동작을 제어하는 데에도 사용할 수 있다.

## Column Row Box
Compose에 표준 레이아웃 3요소는 Column, Row, Box 이다.

![image](https://user-images.githubusercontent.com/50148363/214518807-e2dad830-d57d-4325-bee8-813df63d2db2.png)

### Column
Column은 수직으로 배치되는 레이아웃이다.   
Column은 4가지 변수를 받는다.   
* modifier - composable의 크기, 동작, 모양을 변경하거나 사용자의 입력을 처리(클릭, 스크롤 등) 할 수 있도록 만드는 변수

* verticalArrangement - 수직 배치(Arrangment)를 설정하는 변수
* horizontalAlignment - 수평 정렬(Alignment)을 설정하는 변수
* content - Layout 안에 들어갈 위젯을 설정하는 변수

### Row
Row은 수평으로 배치되는 레이아웃이다.   
Column은 4가지 변수를 받는다.   
* modifier - composable의 크기, 동작, 모양을 변경하거나 사용자의 입력을 처리(클릭, 스크롤 등) 할 수 있도록 만드는 변수

* horizontalArrangement - 수평 배치(Arrangment)를 설정하는 변수
* verticalAlignment - 수직 정렬(Alignment)을 설정하는 변수
* content - Layout 안에 들어갈 위젯을 설정하는 변수

### Box
Box는 여러 위젯을 곂쳐서 놓을 수 있는 레이아웃이다.




### 참고
https://developer.android.com/jetpack/compose/documentation      
https://www.charlezz.com/?p=45448    

