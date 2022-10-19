# MVC | MVP | MVVM
## MVC (Model - View - Controller)
![image](https://user-images.githubusercontent.com/50148363/196627224-11c5bbb2-182e-46b8-b56d-42bbbeec1048.png)

### 구조
* Model   
앱에서 사용되는 실제 데이터 및 데이터 조작 로직을 처리하는 부분

* View   
사용자에게 보여지는 UI부분

* Controller   
사용자의 입력을 받고 처리하는 부분   
모델의 데이터 변화에 따라 뷰를 선택

### 동작
1. Action들은 Controller에 들어온다.
2. Controller는 Action를 확인하고, Model을 업데이트한다.
3. Controller는 Model을 나타내 줄 View를 선택한다.
4. View는 Model을 이용하여 화면을 나타내게 된다.

### 장점
* 가장 단순한 패턴이기도 하고 널리 사용되고 있는 패턴
* Model은 View와 완전히 분리되기 때문에 쉽게 테스트가 가능

### 단점
* View와 Model 사이의 높은 의존성으로 인한 유지보수의 어려움
* Controller에 많은 코드가 모이게 되어 Activity의 비대화

## MVP (Model - View - Presenter)
### 구조
* Model

* View

* Presenter

### 동작
1.
2.


### 장점
*
*


### 단점
*
*


## MVVM (Model - View – ViewModel)
### 구조
* Model

* View

* ViewModel

### 동작
1.
2.


### 장점
*
*

### 단점
*
*



