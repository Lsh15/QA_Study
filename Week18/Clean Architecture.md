#  Clean Architecture(클린 아키텍처)
Clean Architecture(클린 아키텍처)는 Robert C. Martin에 의해 만들어졌으며 그의 블로그 Uncle Bob에서 소개되었으며, 관심사를 계층별로 분리하는 소프트웨어 디자인 철학이다. Clean Architecture(클린 아키텍처)의 주요 원칙은 코드 종속성이 외부로부터 내부로 의존한다는 것이다.  내부 계층의 코드는 외부 계층의 기능을 알 수 없다. 

## 장점
* 프레임워크 독립성 : 프레임워크가 라이브러리에 의존하지 않음
* 테스트 용이성 : 비즈니스 규칙은 UI, DB, 백엔드 서버등 외부와 무관하게 테스팅 가능
* UI 독립성 : UI 변경이 시스템의 나머지 부분에 영향을 미치지 않음
* DB 독립성 : DB 를 어떤 시스템으로 갈아끼우든 상관없음
* 외부 기능 독립성 : 비즈니스 규칙은 외부 기능에 대해 알지 못함

<img src="https://user-images.githubusercontent.com/50148363/217189299-5be25664-b257-4517-aa05-31a4335c118e.png" width="700" height="500">

## Entities
* 핵심 업무 규칙을 캡슐화한다.
* 메서드를 가지는 객체, 일련의 데이터 구조와 함수의 집합이다.
* 가장 변하지 않으며 외부로부터 영향을 받지 않는 영역이다.

## Use Cases
* 애플리케이션의 특화된 업무 규칙을 포함한다.
* 시스템의 모든 Use Cases(유즈 케이스)를 캡슐화하고 구현한다.
* 엔티티로 들어오고 나가는 데이터 흐름을 조정하고 조작한다.
* 안드로이드로 따지면 Model, Repository, Executor 등과 관련된 내용이 해당 계층에 속한다.

## Interface Adapter
* Entity 나 Use Case 로부터 얻은 데이터를 가공하는 계층이다.
* 외부 인터페이스에서 들어오는 데이터를 유즈 케이스와 엔티티에서 처리하기 편한 방식으로 변환하며, 유즈 케이스와 엔티티에서 나가는 데이터를 외부 인터페이스에서 처리하기 편한 방식으로 변환한다.
* 안드로이드로 따지면 ViewModel(MVVM), Presenter(MVP), View(MVVM, MVP), Controller(MVC) 등이 포함된다.

## Frameworks & Drivers
* 시스템의 핵심 업무와는 관련 없는 세부 사항이다.
* 프레임워크나, 데이터베이스, 웹 서버 등이 여기에 해당한다.
* 안드로이드에서는 UI 와 관련된 액티비티 (혹은 프래그먼트), Intent 전달, Room 과 같은 DB, Retrofit 과 같은 네트워킹 관련 프레임워크 코드들이 속한다

### 참고
https://meetup.nhncloud.com/posts/345   
https://www.charlezz.com/?p=1461   
https://velog.io/@haero_kim/Android-Clean-Architecture-%EB%A7%9B%EB%B3%B4%EA%B8%B0

