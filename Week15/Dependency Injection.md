# Dependency Injection(의존성 주입)
Dependency Injection(의존성 주입)이란 클래스간 의존성을 외부에서 주입하는것을 뜻한다.

## 의존성이란
클래스 간의 의존성(Dependency)이 있다는것은 한 클래스가 바뀔 때 다른 클래스가 영향을 받는다는 것을 뜻한다.    
코드에 변경이 있을 경우 변경에 의존성을 갖는 하나의 코드라도 수정하지 않은 곳이 있다면 오류가 발생할 수 있다.    
Interface를 이용하면 특정 클래스에 대한 의존성을 해결할 수 있다.   

## 주입이란
주입(Injection)은 외부에서 객체를 생성하여 해당 객체를 클래스 내부에 주입하는 것이다.       
주입에 필요한 인스턴스를 저장하는 공간을 Container라고 한다.

## 특징
* 클래스간의 결합도를 낮춘다.
* 인터페이스 기반으로 설계되어 코드를 유연하게 한다.
* 단위 테스트를 진행하기 쉬워진다.


### 참조
https://kotlinworld.com/64    
https://hyperconnect.github.io/2020/07/28/android-dagger-hilt.html    
https://developer.android.com/training/dependency-injection     




