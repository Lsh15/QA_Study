# Glide
Glide는 안드로이드의 부드러운 스크롤링에 초점을 맞춘 빠르고 효율적인 이미지 로딩 라이브러리이다. Glide는 사용하기 쉬운 API와, 성능과 확장성이 좋은 디코딩 파이프라인 그리고 자동으로 리소스를 관리하는 기능을 제공한다. Glide는 비디오 스틸, 이미지 및 애니메이션 GIF를 가져오고, 디코딩하고, 디스플레이 하는 것을 지원한다
## 라이브러리 등록
``` korlin
implementation 'com.github.bumptech.glide:glide:4.14.2'
```
## 이미지 출력
``` kotlin
Glide.with(Context)
     .load(이미지(URL, Resouce ID))
     .into(imageView)
```
with()함수에 Context를 전달하고, load()함수에 이미지(URL 또는 Resouce ID)를 전달하고, into() 함수에 imageView 객체 전달하면 이미지를 가져와 출력한다.

## 크기 조절
* override(width, height)함수를 이용하여 이미지의 크기를 조절할 수 있다.

## placeholder


### 참고
https://velog.io/@ywown/kotlin-Glide-%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC   
https://www.charlezz.com/wordpress/wp-content/uploads/2020/10/www.charlezz.com-glide-v4-glide-v4--by-charlezz.pdf    
https://github.com/bumptech/glide     






