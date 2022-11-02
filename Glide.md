# Glide
Glide는 안드로이드의 부드러운 스크롤링에 초점을 맞춘 빠르고 효율적인 이미지 로딩 라이브러리이다. Glide는 사용하기 쉬운 API와, 성능과 확장성이 좋은 디코딩 파이프라인 그리고 자동으로 리소스를 관리하는 기능을 제공한다. Glide는 비디오 스틸, 이미지 및 애니메이션 GIF를 가져오고, 디코딩하고, 디스플레이 하는 것을 지원한다.
## 라이브러리 등록
``` korlin
implementation 'com.github.bumptech.glide:glide:4.14.2'
```
## 이미지 출력
``` kotlin
Glide.with(Context)
     .load(이미지(URL, Resouce ID))
     .into(ImageView)
```
Glide는 3개의 파라미터를 필수적으로 요구하며, 파라미터를 전달하면 이미지를 가져와 출력한다.
* with() : Context
* load() : 이미지(URL 또는 Resouce ID) 
* into() : ImageView 

## 이미지 크기 조절
* override(width, height)함수를 이용하여 이미지의 크기를 조절한다.

## 이미지 변형
* CenterCrop   
이미지의 가로/세로의 길이 중 짧은 쪽을 ImageView의 레이아웃 크기에 맞춰서 출력한다. 원본 이미지 가로/세로의 비율은 유지되고 레이아웃에서 벗어난 이미지는 출력되지 않는다.

* FitCenter   
이미지의 가로/세로의 길이 중 긴 쪽을 ImageView의 레이아웃 크기에 맞춰서 출력한다. 원본 이미지 가로/세로의 비율은 유지되고 레이아웃에 이미지외 빈공간은 background 속성의 color로 채워진다.

* CircleCrop   
FitCenter와 유사하게 동작하지만 이미지를 원으로 변경한다.

## Placeholders
Glide를 통해 서로 다른 상황에서 사용되는 세 가지 placeholder를 지정할 수 있다.
* Placeholder   
Placeholder는 이미지 요청이 진행되는 동안 표시되는 Drawable이다. 요청이 성공적으로 완료되면 placeholder가 요청된 리소스로 바뀐다. 요청된 리소스가 메모리에서 로드되면 placeholder가 표시되지 않을 수 있다

* Error   
요청이 영구적으로 실패하면 Error Drawable이 표시된다. 요청된 URL / 모델이 null이고 Fallback Drawable이 설정되지 않은 경우 Error Drwable도 표시된다.

* Fallback   
Fallback Drawable은 요청된 URL 또는 모델이 null인 경우 표시된다. Fallback Drawables의 주요 목적은 사용자가 null이 예상되는지 여부를 표시 할 수 있도록 하는 것이다.

### 참고
https://velog.io/@ywown/kotlin-Glide-%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC   
https://www.charlezz.com/wordpress/wp-content/uploads/2020/10/www.charlezz.com-glide-v4-glide-v4--by-charlezz.pdf    
https://github.com/bumptech/glide     






