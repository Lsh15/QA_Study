# Compose_Navigation
Navigation은 특정 경로를 따라 앱 내의 한 대상에서 다른 대상으로 네비게이팅(= 탐색 or 이동) 할 수 있게 해주는 Jetpack 라이브러리이다.
Compose에서 Navigation을 사용할 때 NavController라는 컴포넌트를 이용한다.

컴포저블에서 rememberNavController() 메서드를 사용하여 NavController를 만들 수 있다.

``` kotlin
val navController = rememberNavController()
```
## Gradle 설정
``` kotlin
dependencies {
  implementation "androidx.navigation:navigation-compose:$version"
}
```

## NavHost 생성하기
NavHost는 구성 가능한 대상을 지정하는 탐색 그래프와 NavController를 연결한다. 구성 가능한 대상은 컴포저블 간에 이동할 수 있어야 한다. 
여러 컴포저블 간에 이동하는 과정에서 NavHost의 콘텐츠가 자동으로 재구성되고, 탐색 그래프의 구성 가능한 대상은 각각 경로와 연결된다.

컴포즈내에서 네비게이션을 사용할 때, 경로(루트)는 문자열로 표현된다

## 컴포저블로 화면 이동
구성 가능한 대상으로 이동하려면 navigate 메서드를 사용해야 한다. navigate는 대상의 경로를 나타내는 단일 String 매개변수를 사용한다. 
``` kotlin
navController.navigate("Composable Name")
```
navigate는 새 대상을 백 스택에 추가한다. 추가 탐색 옵션을 navigate() 호출에 연결하여 navigate 동작을 수정할 수 있다.
``` kotlin
navController.navigate("Composable Name") {
    popUpTo("home")
}
```

### 참고
https://www.charlezz.com/?p=45742   
https://developer.android.com/jetpack/compose/navigation?hl=ko   



