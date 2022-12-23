# SOLID 원칙
SOLID란 2000년대 초반 로버트 마틴이 객체 지향 프로그래밍 및 설계에 대한 5가지 원칙을 소개 한 것인데, 유지보수와 확장이 쉬운 소프트웨어를 만들고자 할 때 이 원칙을 적용할 수 있다.
코드의 가독성을 높이고 확장이 쉬운 구조를 만들기 위한 지침이다.

## Single Responsibility Principle (단일 책임 원칙)
Single Responsibility Principle (단일 책임 원칙) 이란 모든 클래스는 하나의 책임만 가지며, 클래스가 제공하는 모든 서비스는 하나의 책임을 수행하는데 집중한다는 원칙이다.

### 예시 
로그인(signIn), 로그아웃(signOut) 기능을 만들고 싶은 유저에 대한 정보를 담고 있는 User 클래스가 있다는 가정
* Wrong Ex
``` kotlin
data class User(
    var id: Long,
    var name: String,
    var password: String
){
    fun signIn(){
        // Authetication 을 통한 로그인...
    }

    fun signOut(){
        // Authetication 을 통한 로그아웃...
    }
}
```

User 클래스는 유저에 대한 정보만 가지고 있는 것으로 구현되어야하고, 만약 로그인(signIn)/로그아웃(signOut) 같은 유저 인증 관련 프로세스를 다루고 싶다면 인증 관련 프로세스를 다루는 새로운 클래스는 추가하여 해결한다.
* Right Ex
``` kotlin
data class User(
    var id: Long,
    var name: String,
    var password: String
)

class AuthenticationService(){
    fun signIn(){
        // 로그인 관련 구현...
    }

    fun signOut(){
        // 로그아웃 관련 구현...
    }
}
```

## Open-Closed Principle (개방-폐쇄 원칙)
Open-Closed Principle (개방-폐쇄 원칙) 이란 소프트웨어의 구성요소(컴포넌트, 클래스, 모듈, 함수)는 확장에 열려있고, 변경에 닫혀있어야 한다는 원칙이다.

### 예시 
스마트폰 그리고 스마트폰 서비스 정보를 담고 있는 MobilePhoneUser 클래스가 있고, 스마트폰 서비스에는 HMS, GMS 라고 불리는 2개의 다른 서비스가 있다고 가정
* Wrong Ex
``` kotlin
class MobilePhone {
    lateinit var brandName: String
}

class MobilePhoneUser {
    fun runMobileDevice(mobileServices: Any, mobilePhone: MobilePhone) {
        if (mobileServices is HuaweiMobileServices) {
            println("This device is running with Huawei Mobile Services")
        }
    }
}

class HuaweiMobileServices {
    fun addMobileServiceToPhone(mobilePhone: MobilePhone) { 
    	println("Huawei Mobile Services") 
    }
}
```

새로운 스마트폰 서비스 타입이 나오면,  잊고 추가하지 않을 수도 있고, 코드량도 정량적으로 늘게 되어 그 때마다 하나하나 if-else 문을 통해 추가해야하는 문제 발생된다.
모든 스마트폰 서비스를 위한 하나의 인터페이스를 가지게하고, 각각의 스마트폰 서비스 타입은 인터페이스를 구현하고, 고유한 특성을 가지고 있게 만들어 문제를 해결한다.
* Right Ex
``` kotlin
class MobilePhone {
    lateinit var brandName: String
}

class MobilePhoneUser {
    fun runMobileDevice(mobileServices: IMobileServices, mobilePhone: MobilePhone) {
        mobileServices.addMobileServiceToPhone(mobilePhone)
    }
}

interface IMobileServices {
    fun addMobileServiceToPhone(mobilePhone: MobilePhone)
}

class HuaweiMobileServices: IMobileServices {
    override fun addMobileServiceToPhone(mobilePhone: MobilePhone) { 
    	mobilePhone.brandName = "Huawei"
    	println("Huawei Mobile Services")
    }
}

class GoogleMobileServices: IMobileServices {
    override fun addMobileServiceToPhone(mobilePhone: MobilePhone) { 
    	mobilePhone.brandName = "Google"
    	println("Google Mobile Services") 
    }
}
```

## Liskov Substitution Priciple (리스코프의 치환 원칙)
Liskov Substitution Priciple (리스코프의 치환 원칙) 이란 자식 클래스는 언제나 부모클래스를 대체할 수 있어야 한다는 원칙이다.

### 예시 
Vehicle 추상 클래스가 있고,  Vehicle 클래스는 엔진 상태에 대한 정보와 앞으로 이동 메서드를 가지고 있다는 가정
* Wrong Ex
``` kotlin
abstract class Vehicle {
    protected var isEngineWorking = false
    abstract fun startEngine()
    abstract fun moveForward()
    }

class Car: Vehicle() {
    override fun startEngine() {
        println("Engine started")
        isEngineWorking = true
    }

    override fun moveForward() {
        println("Moving forward")
    }
}

class Bicycle: Vehicle() {
    override fun startEngine() {
        // 필요없는 메서드
    }
    
    override fun moveForward() {
        println("Moving forward")
    }
}
```
Bicycle 클래스를 자식 클래스로 만들 때, Bicycle 은 엔진이 없기 때문에(성급한 추상화의 결과), startEngine 메서드는 필요 없어진다.
Vehicle 을 상속받는 새로운 자식 클래스를 만들어 해결할 수 있다.
* Right Ex
``` kotlin
interface Vehicle {
    fun moveForward()
}

abstract class VehicleWithEngine: Vehicle {    
    private var isEngineWorking = false
    
    open fun startEngine() { 
    	isEngineWorking = true 
    }
}

class Car: VehicleWithEngine() {
    override fun startEngine() {
        super.startEngine()
        println("Engine started")
    }

    override fun moveForward() {
        println("Moving forward")
    }
}

class Bicycle: Vehicle {

    override fun moveForward() {
        println("Moving forward")
    }
}
```

## Interface Segregation Principle (인터페이스 분리 원칙)
Interface Segregation Principle (인터페이스 분리 원칙) 이란 클래스가 다른 클래스에 종속될때에는 가능한 최소한의 인터페이스만을 사용해야 한다는 원칙이다.

### 예시 
Animal 인터페이스를 구현했고, 인터페이스는 동물이 할 수 있는 행동들에 대한 메서드를 가지고 있다는 가정
* Wrong Ex
``` kotlin
interface Animal {
    fun eat()
    fun sleep()
    fun fly() // 의미 없는 예시용
}

class Cat: Animal {
    override fun eat() {
        println("Cat is eating fish")
    }

    override fun sleep() {
        println("Cat is sleeping on its owner's bed")
    }

    override fun fly() {
        TODO("Not yet implemented") // Cats can't fly
    }
}

class Bird: Animal {
    override fun eat() {
        println("Bird is eating forage")
    }

    override fun sleep() {
        println("Bird is sleeping in the nest")
    }

    override fun fly() {
        println("Bird is flying so high")
    }
}
```
Cat 같은 클래스가 추가된다면, Fly 메서드는 불필요하게 된다.
Animal 클래스에서 fly 메서드를 제거하고, FlyingAnimal 같이 새로운 인터페이스를 추가하여 해결한다.
* Right Ex
``` kotlin
interface Animal {
    fun eat()
    fun sleep()
}

interface FlyingAnimal {
    fun fly()
}

class Cat: Animal {
    override fun eat() {
        println("Cat is eating fish")
    }

    override fun sleep() {
        println("Cat is sleeping on its owner's bed")
    }
}

class Bird: Animal, FlyingAnimal {
    override fun eat() {
        println("Bird is eating forage")
    }

    override fun sleep() {
        println("Bird is sleeping in the nest")
    }

    override fun fly() {
        println("Bird is flying so high")
    }
}
```
## Dependency Inversion Principle (의존성 역전 원칙)
Dependency Inversion Principle (의존성 역전 원칙) 이란 상위와 하위 객체 모두가 동일한 추상화에 의존해야 한다는 원칙이다.


### 예시 
* Wrong Ex
``` kotlin
data class User(
    var id: Long,
    var name: String,
    var password: String
){
    fun signIn(){
        // Authetication 을 통한 로그인...
    }

    fun signOut(){
        // Authetication 을 통한 로그아웃...
    }
}
```

* Right Ex
``` kotlin
data class User(
    var id: Long,
    var name: String,
    var password: String
)

class AuthenticationService(){
    fun signIn(){
        // 로그인 관련 구현...
    }

    fun signOut(){
        // 로그아웃 관련 구현...
    }
}
```

### 참고
https://www.nextree.co.kr/p6960/     
https://nanamare.tistory.com/174      
https://www.charlezz.com/?p=1452      


