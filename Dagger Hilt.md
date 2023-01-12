# Dagger Hilt
Hilt는 Dagger2 기반의 안드로이드 전용 의존성 주입 라이브러리이다.

## 특징
* 성능이 입증된 Dagger 기반으로 빌드 된다.
* ViewModel, Fragment, WorkManager 등과 같이 Jetpack에 통합된다.
* Android를 위해 정의된 Scope들이 있다.
* 안드로이드 스튜디오와 통합되기 때문에 오브젝트 그래프를 가시화할 수 있다.

## Gradle 설정
project-level의 build.gradle에 추가한다
``` kotlin
dependencies {
  // other plugins...
  classpath 'com.google.dagger:hilt-android-gradle-plugin:2.44.2'
}
```

app-level의 build.gradle 파일에 추가한다.
``` kotlin
apply plugin: 'com.android.application'
apply plugin: 'com.google.dagger.hilt.android'

dependencies {
  implementation 'com.google.dagger:hilt-android:2.44.2'
  kapt 'com.google.dagger:hilt-compiler:2.44.2'
}  
```
## 주요 Hilt Annotation
* @HiltAndroidApp
* @AndroidEntryPoint
* @InstallIn
* @EntryPoint

### @HiltAndroidApp
@HiltAndroidApp 은 Hilt 코드 생성시 시작, 반드시 Application 클래스에 추가해야 한다.   
Application 클래스 컴포넌트 코드를 생성 및 인스턴스화 하는 코드가 생성된다.

### @AndroidEntryPoint
@HiltAndroidApp 설정 후 Application 클래스 상단에 추가하어 사용가능 하다.     
Hilt는 Activity, Fragment, Service, View, BroadcastReceiver, ViewModel 컴포넌트들에 의존성 주입을 도와준다.     

### @InstallIn
Hilt가 생성하는 DI 컨테이너에 어떤 module을 사용할지 가르킨다.
Hilt에서 제공하는 기본적인 규칙은 모든 module에 @InstallIn 어노테이션을 사용하여 어떤 component에 install 할지 반드시 정해주어야 한다.

### @EntryPoint
Hilt가 지원하지 않는 클래스(Content Provider,DFM)에서 의존성이 필요한 경우 사용한다.
Interface 에서만 사용가능 하고,@InstallIn이 반드시 함께 있어야한다.


### 참고
https://hyperconnect.github.io/2020/07/28/android-dagger-hilt.html      
https://developer.android.com/training/dependency-injection/hilt-android     
https://www.charlezz.com/?p=44230    
https://www.youtube.com/watch?v=gkUCs6YWzEY
