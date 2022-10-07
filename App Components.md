# App Components (앱 구성 요소)
## Activity (액티비티)
Activity는 사용자가 앱과 상호 작용하는 진입점이며 단일화면을 의미한다. Activity는 Life Cycle 관련 메서드들을 이용하여 원하는 기능들을 구현할 수 있다. 2개 이상의 Activity를 동시에 Display 할 수 없으며 1개 이상의 View 또는 ViewGroup을 포함한다.

## Service (서비스)
Service는 백그라운드에서 앱을 계속 실행하기 위한 다목적 진입점이며 백그라운드에서 실행되는 구성 요소로, 오랫동안 실행되는 작업을 수행하거나 원격 프로세스를 위한 작업을 수행한다. Service는 사용자 인터페이스를 제공하지 않는다. 앱이 종료되어도 이미 시작이 된 Service는 백그라운드에서 계속 동작한다.

## Broadcast Receiver (방송 수신자)
Broadcast Receiver는 시스템이 정기적인 사용자 플로우 밖에서 이벤트를 앱에 전달하도록 지원하는 구성 요소로, 앱이 시스템 전체의 브로드캐스트 알림에 응답할 수 있게 한다.  Broadcast Receiver도 앱으로 들어갈 수 있는 진입점이기 때문에 현재 실행되지 않은 앱에도 시스템이 브로드캐스트를 전달할 수 있다. Broadcast Receiver는 사용자 인터페이스를 표시하지 않지만, 상태 표시줄 알림을 생성하여 사용자에게 브로드캐스트 이벤트가 발생했다고 알릴 수 있다. 다만 Broadcast Receiver는 극소량의 작업만 수행하도록 만들어진 경우가 많다.

## Content Provider (콘텐츠 제공자)



### 참고
https://developer.android.com/guide/components/fundamentals   
https://velog.io/@jojo_devstory/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-Android-4%EB%8C%80-%EC%BB%B4%ED%8F%AC%EB%84%8C%ED%8A%B8
