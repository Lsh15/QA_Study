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

## 얼굴 인식기 구성
* setPerformanceMode   
PERFORMANCE_MODE_FAST(기본값) | PERFORMANCE_MODE_ACCURATE - 얼굴을 인식할 때 속도 또는 정확도를 우선시 한다.

* setLandmarkMode   
LANDMARK_MODE_NONE(기본값) | LANDMARK_MODE_ALL - 눈, 귀, 코, 콧볼, 입과 같은 얼굴의 랜드마크를 파악할 것인지 여부이다.

* setContourMode
CONTOUR_MODE_NONE(기본값) | CONTOUR_MODE_ALL - 얼굴 특징의 윤곽을 감지할지 나타낸다. 윤곽은 이미지 속 가장 뚜렷한 얼굴에 대해서만 인식된다.

* setClassificationMode   
CLASSIFICATION_MODE_NONE(기본값) | CLASSIFICATION_MODE_ALL - 얼굴을 '웃고 있음'이나 '눈을 뜸'과 같은 카테고리로 분류할 것인지 여부이다.

#### 예시
``` kotlin
// 높은 정확도를 가진 랜드마크 탐지와 얼굴 분류를 위한 설정
val highAccuracyOpts = FaceDetectorOptions.Builder()
        .setPerformanceMode(FaceDetectorOptions.PERFORMANCE_MODE_ACCURATE)
        .setLandmarkMode(FaceDetectorOptions.LANDMARK_MODE_ALL)
        .setClassificationMode(FaceDetectorOptions.CLASSIFICATION_MODE_ALL)
        .build()

// 실시간 contour 탐지를 위한 설정
val realTimeOpts = FaceDetectorOptions.Builder()
        .setContourMode(FaceDetectorOptions.CONTOUR_MODE_ALL)
        .build()
```

## 입력 이미지 준비
이미지 속 얼굴을 인식하려면 Bitmap, media.Image, ByteBuffer, 기기의 파일에서 InputImage 객체를 만들어야 한다. 그런 다음 InputImage 객체를 FaceDetector의 process 메서드에 전달해야한다.   
얼굴 인식의 경우 크기가 480x360 픽셀 이상인 이미지를 사용해야 한다. 실시간으로 얼굴을 인식하는 경우 이 최소 해상도로 프레임을 캡처하면 지연 시간을 줄일 수 있다.

### Bitmap 사용
Bitmap 객체에서 InputImage 객체를 생성하는 예시 코드
``` kotlin
val image = InputImage.fromBitmap(bitmap, 0)
```

### URI 사용
URI에서 InputImage 객체를 생성하는 예시 코드
``` kotlin
val image: InputImage
try {
    image = InputImage.fromFilePath(context, uri)
} catch (e: IOException) {
    e.printStackTrace()
}
```

## FaceDetector 인스턴스 가져오기
FaceDetector 객체를 생성한다. 아무 옵션도 지정해주지 않으면 기본 설정값으로 세팅된다.
``` kotlin
// Or, to use the default option:
val detector = FaceDetection.getClient(options)
```

## 이미지 처리
생성한 FaceDetector 객체를 이용해 생성한 Input Image를 처리해주는 코드이다. 탐지한 결과는 result에 담기게 된다.
``` kotlin
val result = detector.process(image)
        .addOnSuccessListener { faces ->
            // Task completed successfully
        }
        .addOnFailureListener { e ->
            // Task failed with an exception
        }
```

### 참고
https://developers.google.com/ml-kit/vision/face-detection   
https://developers.google.com/ml-kit/vision/face-detection/android   
