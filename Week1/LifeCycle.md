# Activity LifeCycle
![image](https://user-images.githubusercontent.com/50148363/192918805-48e158df-98f5-4dee-9d19-fef0f8b3d838.png)
## onCreate()
Activity를 생성할 때 실행되는 메소드로 전체 LifeCycle 동안 한 번 호출되게되며 필수적으로 구현해야한다. 메서드는 savedInstanceState 매개변수를 수신하는데, 이는 활동의 이전 저장 상태가 포함된 Bundle 객체이다. 이번에 처음 생성된 활동인 경우 Bundle 객체의 값은 null이다. XML 파일을 정의하고 setContentView()에 전달하는 대신, Activity 코드에 새로운 View 객체를 생성하고 새로운 View를 ViewGroup에 넣어서 뷰 계층 구조를 빌드할 수 있습니다

## onStart()	
Activity가 사용자에게 보이기 직전에 호출된다. onStart() 가 호출되면 Activity가 사용자에게 표시되고, 앱은 활동을 포그라운드에 보내 상호작용할 수 있도록 준비한다. onStart() 메서드는 매우 빠르게 완료되고, 생성됨 상태와 마찬가지로 활동은 시작됨 상태에 머무르지 않고, 시스템이 onResume() 메서드를 호출한다. 

## onResume()	
Activity가 포그라운드 상태가 되었고 사용자와 상호작용을 할 수 있는 곳이다. 이벤트(예를 들어 전화가 오거나, 사용자가 다른 활동으로 이동하거나, 기기 화면이 꺼지는 이벤트)가 발생하여 앱에서 포커스가 떠날 때까지 앱이 이 상태에 머무른다. 방해되는 이벤트가 발생하면 onPause() 가 호출되고 다시 재개가 되면 onResume() 콜백이 호출하게된다. onResume() 은 onPause() 에서 해제했던 리소스들을 다시 초기화 하는 코드가 있어야한다. 즉, onResume과 onPause는 대칭적으로 리소스/데이터 초기화와 해제를 해야 한다.
## onPause()	

## onStop()	
## onDestroy()	
## onRestart()	
# Fragment LifeCycle
![image](https://user-images.githubusercontent.com/50148363/192920677-243e67d6-8003-4737-84c7-b1ba0fc5862a.png)


### 참고 자료
https://math-coding.tistory.com/238
https://www.charlezz.com/?p=834
https://developer.android.com/guide/components/activities/activity-lifecycle?hl=ko
