# MVC | MVP | MVVM
## MVC (Model - View - Controller)
![image](https://user-images.githubusercontent.com/50148363/196627224-11c5bbb2-182e-46b8-b56d-42bbbeec1048.png)

### 구조
* Model   
독립적인 영역으로 앱에서 사용되는 실제 데이터 및 데이터 조작 로직을 처리하는 부분

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
![image](https://user-images.githubusercontent.com/50148363/196639035-f055f047-f346-424b-9863-700dfaf3fe33.png)

### 구조
* Model   
독립적인 영역으로 앱에서 사용되는 실제 데이터 및 데이터 조작 로직을 처리하는 부분

* View   
사용자에게 보여지는 UI부분

* Presenter   
Model과 View사이의 매개체   
View에서 요청한 정보를 Model로부터 가공하여 View로 전달하는 부분

### 동작
1. Action들은 View를 통해 들어온다.   
2. View는 데이터를 Presenter에게 요청한다.   
3. Presenter는 Model에게 데이터를 요청한다.   
4. Model은 Presenter에서 요청받은 데이터를 응답한다.   
5. Presenter는 View에게 데이터를 응답한다.   
6. View는 Presenter가 응답한 데이터를 이용하여 화면을 나타낸다.

### 장점
* Presentor를 통해서 데이터를 전달받기 때문에 View와 Model의 의존성 없음
* MVC 단점을 해결

### 단점
* View와 Presenter 사이의 높은 의존성
* View마다 Presenter가 존재하게 되고 코드량이 많아져 유지 보수의 어려움 

## MVVM (Model - View – ViewModel)
![image](https://user-images.githubusercontent.com/50148363/196659211-017b9418-662e-4908-a686-903f64dfda73.png)

### 구조
* Model   
독립적인 영역으로 앱에서 사용되는 실제 데이터 및 데이터 조작 로직을 처리하는 부분

* View   
사용자에게 보여지는 UI부분

* ViewModel   
View를 표현하기 위해 만들어진 View를 위한 Model   
View를 나타내 주기 위한 Model이자 View를 나타내기 위한 데이터 처리를 하는 부분

### 동작
1.
2.


### 장점
*
*

### 단점
*
*


