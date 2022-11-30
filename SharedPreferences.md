# SharedPreferences
SharedPreferences를 이용하여 Integer, String과 같은 간단한 데이터를 저장할 수 있다. 숫자 몇개, 문자열 몇개 정도의 데이터를 저장해야 하는데 SQLite 같은 DB를 이용하기엔 번거로울 때 사용하면 좋다.  
SharedPreferences는 App의 개별 데이터 저장소에 xml파일을 만들고, 그 파일에 Integer, String 등의 데이터를 저장하거나 읽는다.데이터를 저장할 때는 key/value 형태로 저장한다.

## 특징
* SharedPreferences는 간단한 데이터를 앱의 개별 저장소에 xml파일로 저장
* SharedPreferences 객체를 생성할 때 파일 이름을 인자로 전달하며, 그 이름으로 xml파일이 생성됨
* 데이터를 저장할 때는 key/value 형태로 저장
* 데이터는 App의 개별 데이터 저장소에 저장되기 때문에 다른 App과 공유할 수 없음
* SharedPreferences는 put/get 메소드를 제공하여 데이터를 저장하거나 읽을 수 있음

## SharedPreferences 객체 생성

## SharedPreferences으로 데이터 저장

## SharedPreferences에서 데이터 읽기

### 참고
https://developer.android.com/training/data-storage/shared-preferences   
https://codechacha.com/ko/android-shared-preferences/   

