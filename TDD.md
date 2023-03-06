# TDD
TDD란 Test Driven Development의 약자로 테스트 주도 개발이다.
TDD(테스트 주도 개발)는 설계 이후 코드 개발 및 테스트케이스를 작성하는 기존의 개발 프로세스와 다르게 테스트케이스를 작성 한 후 실제 코드를 개발하여 리펙토링하는 절차로 개발한다. 

## TDD 매인 프로세스 
* RED - 테스트 실패
* GREEN - 테스트 성공
* REFACTOR - 리팩토링

![image](https://user-images.githubusercontent.com/50148363/223036500-568c4894-691e-400c-815c-293d716d8417.png)

## TDD 세부 프로세스 
단위 테스트 작성 → 단위 테스트 실행 → 운영 코드 작성 → 단위 테스트 실행 → 설계 개선(리팩토링) → 단위 테스트 → …  실행을 반복한다.

![image](https://user-images.githubusercontent.com/50148363/223001534-70b7d734-2f38-4c3d-a716-8bf092c779e2.png)

## 장단점
### 장점
* 튼튼한 객체 지향적인 코드 생산
* 재설계 시간의 단축
* 디버깅 시간의 단축
* 테스트 문서의 대체 가능
* 추가 구현의 용이함

### 단점
* 생산성의 저하

### 참고
https://en.wikipedia.org/wiki/Test-driven_development    
https://media.fastcampus.co.kr/knowledge/dev/tdd/    
http://clipsoft.co.kr/wp/blog/tddtest-driven-development-%EB%B0%A9%EB%B2%95%EB%A1%A0/   
