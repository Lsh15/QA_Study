# Activity LifeCycle
![image](https://user-images.githubusercontent.com/50148363/192918805-48e158df-98f5-4dee-9d19-fef0f8b3d838.png)
## onCreate()
Activity를 생성할 때 실행되는 메소드로 전체 LifeCycle 동안 한 번 호출되게 되며 필수적으로 구현해야 한다. 메서드는 savedInstanceState 매개변수를 수신하는데, 이는 Activity의 이전 저장 상태가 포함된 Bundle 객체이다. 이번에 처음 생성된 Activity인 경우 Bundle 객체의 값은 null이다. XML 파일을 정의하고 setContentView()에 전달하는 대신, Activity 코드에 새로운 View 객체를 생성하고 새로운 View를 ViewGroup에 넣어서 뷰 계층 구조를 빌드할 수 있다.

## onStart()	
Activity가 사용자에게 보이기 직전에 호출된다. onStart() 메서드가 호출되면 Activity가 사용자에게 표시되고, 앱은 활동을 포그라운드에 보내 상호작용할 수 있도록 준비한다. onStart() 메서드는 매우 빠르게 완료되고, 생성됨 상태와 마찬가지로 활동은 시작됨 상태에 머무르지 않고, 시스템이 onResume() 메서드를 호출한다. 

## onResume()	
Activity가 포그라운드 상태가 되었고 사용자와 상호작용을 할 수 있는 곳이다. 이벤트(예를 들어 전화가 오거나, 사용자가 다른 활동으로 이동하거나, 기기 화면이 꺼지는 이벤트)가 발생하여 앱에서 포커스가 떠날 때까지 앱이 이 상태에 머무른다. 방해되는 이벤트가 발생하면 onPause() 가 호출되고 다시 재개가 되면 onResume() 콜백이 호출하게 된다. onResume() 은 onPause() 에서 해제했던 리소스들을 다시 초기화 하는 코드가 있어야한다. 즉, onResume과 onPause는 대칭적으로 리소스/데이터 초기화와 해제를 해야 한다.

## onPause()	
사용자가 Activity를 떠나는 것을 나타내는 첫 번째 신호로 이 메서드를 호출한다 (하지만 해당 활동이 항상 소멸되는 것은 아님). Activity가 포그라운드에 있지 않게 되었다는 것을 나타낸다 (다만 사용자가 멀티 윈도우 모드에 있을 경우에는 여전히 표시 될 수도 있음). 새로운 Acitvity가 포그라운드로 나오기전까지는 onPause() 상태에 있다가 포그라운드로 나오는 순간 모든 화면이 가려지면 onStop() 콜백을 호출하게 된다. Dialog Activity나 투명 Acitivty가 위에 뜰 경우에도 onPause() 상태에 머물게 된다. onPause()를 사용하여 애플리케이션 또는 사용자의 데이터를 저장하거나, 네트워크 호출을 하거나, 데이터베이스 트랜잭션을 실행해서는 안 된다. 부하가 큰 종료 작업은 onStop() 상태일 때 실행해야 한다. onPause() 메서드의 실행이 완료되더라도 Activity는 일시중지됨 상태로 남아 있으며 Activity는 다시 시작되거나 사용자에게 완전히 보이지 않게 될 때까지 이 상태에 머무른다. Activity가 다시 시작되면 시스템은 다시 한번 onResume() 콜백을 호출한다. 

## onStop()
Activity가 사용자에게 더 이상 표시되지 않으면 중단됨 상태에 들어가고, 시스템은 onStop() 콜백을 호출한다. 시스템은 Activity의 실행이 완료되어 종료될 시점에 onStop()을 호출할 수도 있다. onStop() 메서드에서는 앱이 사용자에게 보이지 않는 동안 앱은 필요하지 않은 리소스를 해제하거나 조정해야 한다. onStop()을 사용하여 CPU를 비교적 많이 소모하는 종료 작업을 실행해야 한다. onStop() 메서드에 들어가면 Activity 객체는 메모리 안에 머무르게 된다. Activity가 다시 시작되면 시스템은 onRestart()를 호출하고, Activity가 실행을 종료하면 시스템은 onDestroy()를 호출한다. onPause() 는 포그라운드에서 백그라운드로 전환되는 시점으로 화면의 일부가 가려진 상태에 호출되고, onStop() 은 완전히 화면이 가려지면 호출된다.

## onDestroy()	
onDestroy()는 활동이 소멸되기 전에 호출된다. 사용자가 Activity를 완전히 닫거나 Activity에서 finish()가 호출되어 종료되는 경우, 구성 변경(기기 회전 또는 멀티 윈도우 모드)으로 인해 시스템이 일시적으로 활동을 소멸시키는 경우에도 호출된다. 이와 같은 두 가지 시나리오는 isFinishing() 메서드로 구분할 수 있다. Activity가 종료되는 경우 onDestroy()는 Activity가 수신하는 마지막 수명 주기 콜백이 된다. 구성 변경으로 인해 onDestroy()가 호출되는 경우 시스템이 즉시 새 활동 인스턴스를 생성한 다음, 새로운 구성에서 그 새로운 인스턴스에 관해 onCreate()를 호출한다.

## onRestart()	
Activity가 중단되었다가 다시 시작되기 직전에 호출된다. onRestart() 뒤에는 항상 onStart() 가 호출된다.

# Fragment LifeCycle
![image](https://user-images.githubusercontent.com/50148363/193259090-e60443b3-30a8-420b-99b5-7e7658ef9f5f.png)
## onAttach()
Fragment가 Activity와 연결될 때 호출된다. Fragment가 완벽하게 생성된 상태는 아니다.

## onCreate()
Fragment를 생성할 때 시스템에서 이것을 호출한다. Fragment의 기본 구성 요소 중 Fragment가 일시 정지되거나 중단되었다가 재개되었을 때 유지하고자 하는 것을 초기화해야 한다. Activity와는 달리 Fragment의 onCreate()에서는 view와 관련된 UI작업을 할 수 없다.

## onCreateVIew()
Fragment가 사용자 인터페이스를 처음으로 그릴 시간이 되면 호출한다. Layout을 inflate해서 반환해주고, View 객체를 얻을 수 있으므로 UI와 관련된 바인딩 작업을 실행하면 된다. onCreateVIew() 메서드는 Fragment Layout의 루트이다. Fragment가 UI를 제공하지 않는 경우 null을 반환하면 된다.
 
## onViewCreated()
Fragment의 View(위젯, 레이아웃)가 생성되면 호출된다. View의 초기값을 설정할 수 있다.

## onViewStateRestored()
onViewStateRestored()은 저장해둔 모든 State 값이 Fragment의 View 계층구조에 복원되었을 때 호출되며, 각 View의 상태 값(체크박스가 현재 체크되어 있는지)을 체크할 수 있다 .

## onStart()
Fragment가 화면에 보여지기 직전에 실행된다. child FragmentManager를 통해 FragmentTransaction을 안전하게 수행할 수 있다.
 
## onResume()
Fagment가 화면에 보여 지며 사용자와 상호작용이 가능한 상태이다. Activity와 마찬가지로 이벤트가 발생하여 Fragment가 가려지기 전까지 이 상태가 유지된다.

## onPause()
사용자가 Fragment를 떠나기 시작했지만 Fragment는 여전히 보일때부터 onPause()가 호출된다. UI 관련 처리를 정지하고, 중요한 데이터를 저장한다.

## onStop()
Fragment가 완전히 가려져 더 이상 화면에 보이지 않는 경우, 실행된다. onStop()은 API 28 버전을 기점으로 onSaveInstanceState() 함수와 onStop() 함수 호출 순서가 달라졌다.  onStop()이 onSaveInstanceState() 함수보다 먼저 호출되어 onStop()이 FragmentTransaction을 안전하게 수행할 수 있는 마지막 지점이 되었다.

## onDestroyView()
Fragment와 관련된 view가 제거될 때 실행된다. Activity에서 Fragment 생성 시 addToBackStack()를 요청했을 경우 onDestroy()를 호출하지 않고 인스턴스가 저장되어 있다가 Fragment를 다시 부를 때 onCreateView()를 실행하여 다시 화면에 보여 지게 한다. Fragment가 아직 메모리에 남아있으므로, Fragment에 대한 모든 참조를 제거해야 메모리 누수를 방지할 수 있다.

## onDestory()
View가 제거된 후 Fragment가 완전히 소멸되기 전에 호출된다.

## onDetach() 
Fragment가 완전히 소멸되고, Activity와의 연결도 끊어질 때 실행된다. onAttach() 가 onCreate() 이전에 호출 됐던 것처럼 onDetach() 또한 onDestroy() 이후에 호출된다.


### 참고 자료
https://math-coding.tistory.com/238    
https://developer.android.com/guide/components/activities/activity-lifecycle?hl=ko   
https://developer.android.com/guide/fragments/lifecycle   
https://jinee0717.tistory.com/44   
https://zibro.tistory.com/13   
