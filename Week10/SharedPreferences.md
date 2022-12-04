# SharedPreferences
SharedPreferences를 이용하여 Integer, String과 같은 간단한 데이터를 저장할 수 있다. 숫자 몇개, 문자열 몇개 정도의 데이터를 저장해야 하는데 SQLite 같은 DB를 이용하기엔 번거로울 때 사용하면 좋다.  
SharedPreferences는 App의 개별 데이터 저장소에 xml파일을 만들고, 그 파일에 Integer, String 등의 데이터를 저장하거나 읽는다.데이터를 저장할 때는 Key/Value 형태로 저장한다.

## 특징
* SharedPreferences는 간단한 데이터를 앱의 개별 저장소에 xml파일로 저장
* SharedPreferences 객체를 생성할 때 파일 이름을 인자로 전달하며, 그 이름으로 xml파일이 생성됨
* 데이터를 저장할 때는 Key/Value 형태로 저장
* 데이터는 App의 개별 데이터 저장소에 저장되기 때문에 다른 App과 공유할 수 없음
* SharedPreferences는 Put/Get 메소드를 제공하여 데이터를 저장하거나 읽을 수 있음

## SharedPreferences 객체 생성
getSharedPreferences(String name, int mode) 를 호출하여 SharedPreferences 객체를 생성할 수 있다.   
name은 앱에 고유하게 식별할 수 있는 파일 이름을 사용해야 한다. mode는 MODE_PRIVATE(자기 앱 내에서 사용. 외부 앱에서 접근 불가)를 사용해야 한다.

## SharedPreferences으로 데이터 저장
SharedPreferences에서 데이터를 저장할 때는 edit()을 호출하여 SharedPreferences.Editor를 만들어서 할 수 있다.  
putInt() 및 putString()과 같은 메서드를 사용하여 쓰려고 하는 키와 값을 전달한다. 그런 다음 apply()를 호출하여 변경사항을 저장한다. 첫번째 인자는 Key이고, 두번째 인자는 Value이다.   
apply()는 비동기적으로(asynchronously) 동작하기 때문에 처리 중인 Thread가 Blocking되지 않는다.

## SharedPreferences에서 데이터 읽기
SharedPreferences에서 데이터를 읽어올 때는 Edit 객체가 필요없다.   
getInt() 및 getString()과 같은 메서드를 사용하여 저장되어 있는 키를 받는다. 첫번째 인자는 Key이고, 두번째 인자는 Key에 대한 데이터가 없을 때 값이다.   

### 참고
https://developer.android.com/training/data-storage/shared-preferences   
https://codechacha.com/ko/android-shared-preferences/   

