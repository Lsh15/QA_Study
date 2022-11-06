# Material Design
Material Design 은 모바일과 데스크톱 그리고 그 밖에 다양한 장치를 아우르는 디자인이다.

## 라이브러리 등록
``` kotlin
dependencies {
    implementation 'com.google.android.material:material:<version>'
}
```
## AppBarLayout
App Bar는 액티비티의 제목과 탐색(navigation)을 위한 액션 버튼 또는 여러 종류의 위젯으로 구성된 액티비티의 기본 도구모음(Toolbar)을 말한다.   
<img src = "https://user-images.githubusercontent.com/50148363/199925229-9cc3ae01-d595-4a68-8757-a49292552e77.png" width="900" height="300"/> 
1. Container
2. Navigation icon 
3. Title 
4. Action items 
5. Overflow menu 

### CoordinatorLayout
CoordinatorLayout은 FrameLayout에 기반을 둔 Layout이다. CoordinatorLayout은 스크롤 이벤트에 따라 상단의 앱바 혹은 이미지를 변화시켜줄때 사용한다.

### CollapsingToolbarLayout
AppBarLayout의 안에 작성하는데 AppBarLayout에 포함된 ImageView, Toolbar등을 어떻게 축소할지 설정하는 곳이다.
 
## TabLayout
TabLayout은 Tab 버튼을 눌렀을 때 다른 페이지를 보여주는 레이아웃입니다. 상단에 Tab 버튼이 보이며, 이 버튼을 누르면 가운데 페이지가 변경됩니다.   
TabLayout과 ViewPager2를 이용하면, Tab 버튼을 눌렀을 때 다른 페이지가 보이는 기능을 쉽게 구현할 수 있다. ViewPager2는 Swipe하여 페이지를 넘기는 UI를 구현하는데 사용되는 클래스이다.      
<img src = "https://user-images.githubusercontent.com/50148363/199925801-ee37cef4-f706-41a1-8721-463135364067.png" width="700" height="300"/> 
1. Container
2. Active icon 
3. Active text label 
4. Active tab indicator
5. Inactive icon 
6. Inactive text label 
7. Tab item

## NavigationView
NavigationView는 앱의 최상위 기본 탐색 메뉴로 동작하는 인터페이스 화면을 의미한다.
<img src = "https://user-images.githubusercontent.com/50148363/199932833-27980100-0cd3-4474-92a7-e7969c8c2426.png" width="600" height="600"/>
1. Container
2. Header 
3. Divider 
4. Active text overlay
5. Active text
6. Inactive text
7. Subtitle 
8. Scrim 

## ExtendedFloatingActionButton
FloatingActionButton은 화면 레이어 최상단에 떠있는 버튼을 의미한다.   
<img src = "https://user-images.githubusercontent.com/50148363/199936348-a8bc200d-5e4e-4316-8d94-76c0f17caab8.png" width="500" height="300"/>
1. Container
2. Icon
3. Text label

### 참고
https://velog.io/@changhee09/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-AppBarLayout   
https://recipes4dev.tistory.com/141   
https://m2.material.io/components?platform=android   


