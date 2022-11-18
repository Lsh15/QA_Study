# Face Detection API
## 라이브러리 등록
``` kotlin 
dependencies {
  implementation 'com.google.mlkit:face-detection:16.1.5'
}
```
## 주요 기능
* Recognize and locate facial features (얼굴 특징 인식 및 위치 찾기) : 감지된 모든 얼굴의 눈, 귀, 볼, 코, 입의 좌표를 확인한다.   
*	Get the contours of facial features (얼굴 특징의 윤곽 가져오기) : 감지된 얼굴과 눈, 눈썹, 입술, 코의 윤곽을 가져온다.   
*	Recognize facial expressions (표정 인식) : 사람이 웃고 있는지 아니면 눈을 감고 있는지 판단한다.   
*	Track faces across video frames (동영상 프레임에서 얼굴 추적) : 감지된 고유한 얼굴의 식별자를 가져온다. 식별자는 호출 전체에서 일관되므로 동영상 스트림의 특정인에 대해 이미지 조작을 할 수 있다.   
*	Process video frames in real time (동영상 프레임을 실시간으로 처리) : 얼굴 인식은 기기에서 실행되며, 동영상 조작과 같은 실시간 애플리케이션에서 사용하기에 빠르다.

### 참고
https://developers.google.com/ml-kit/vision/face-detection   
https://developers.google.com/ml-kit/vision/face-detection/android   
