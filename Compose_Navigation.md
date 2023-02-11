# Compose_Navigation
Navigation은 특정 경로를 따라 앱 내의 한 대상에서 다른 대상으로 네비게이팅(= 탐색 or 이동) 할 수 있게 해주는 Jetpack 라이브러리이다.
Compose에서 Navigation을 사용할 때 NavController라는 컴포넌트를 이용한다.

컴포저블에서 rememberNavController() 메서드를 사용하여 NavController를 만들 수 있다.

## Gradle 설정
``` kotlin
dependencies {
  implementation "androidx.navigation:navigation-compose:$version"
}
```

### 참고
https://www.charlezz.com/?p=45742   
https://developer.android.com/jetpack/compose/navigation?hl=ko   



