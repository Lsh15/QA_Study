# Seven Testing Principles (테스팅의 7 가지 원리)
![image](https://user-images.githubusercontent.com/50148363/227133596-b0b863ab-1c6c-4f26-b4b6-3f16afed34e5.png)

## 1. 테스팅은 결함이 존재함을 밝히는 활동이지, 결함이 없음을 밝히는 활동이 아니다 (Testing shows the presence of defects, not their absence)
Testing은 결함이 존재한다는 것을 보여줄 수 있지만, 결함이 없다는 것을 증명할 수 없다.   
Testing은 소프트웨어에 발견되지 않은 결함의 존재 가능성을 줄일 수는 있지만, 결함이 전혀 발견되지 않았다 하더라도 소프트웨어가 완벽하다는 뜻은 아니다.

## 2. 완벽한 테스팅은 불가능하다 (Exhaustive testing is impossible)
모든 것을 Testing 한다는 것은 간단한 소프트웨어를 제외하고는 불가능하다.   
완벽하게 테스트하고자 하기보다는 리스크 분석과 우선순위를 토대로한 테스트에 노력을 집중하는 것이 좋다.

## 3. 조기 테스팅으로 시간과 비용을 절약할 수 있다 (Early testing saves time and money)
초기에 결함을 찾기 위해서는 정적 및 동적 테스트 모두 소프트웨어 개발 수명주기 중 가능한 이른 시점에 시작해야 한다.   
초기부터 시작하는 테스팅을 시프트 레프트(shift left)라고도 부른다.     
소프트웨어 수명주기 초기부터 테스팅을 함으로써 나중에 큰 비용이 동반되는 수정을 줄이거나 없앨 수 있다. 

## 4. 결함은 집중된다 (Defects cluster together)
출시 전 Testing에서 발견하는 결함은 소수의 모듈에 집중되어 발생하는 경향을 보이며, 운영상 장애의 대부분은 소수의 모듈에서 발생한다.   
예상 결함 집중 영역과 테스트와 운영 중 실제로 관측한 결함 집중 영역은 리스크 분석의 주요 입력값으로 사용된다.     
리스크 분석은 테스트 노력을 집중시키는 데 필요하다.

## 5. 살충제 패러독스에 유의하라 (Beware of the pesticide paradox)
만일 같은 테스트를 계속해서 반복 실행한다면, 해당 테스트로는 결함을 더 이상 발견할 수 없게 된다.   
새로운 결함을 발견하기 위해서는 기존 테스트와 테스트 데이터를 바꾸고 새로운 테스트를 작성할 필요가 있다.   
하지만 살충제 패러독스가 좋은 것을 의미하는 경우도 있다. 자동 리그레션 테스팅의 경우 리그레션 결함이 적다는 것을 의미할 수도 있다. 

## 6. 테스팅은 정황에 의존적이다 (Testing is context dependent)
Testing은 context에 따라 다르게 진행된다.   
애자일에서의 Testing은 순차적 소프트웨어 개발 수명주기에서의 Testing과는 다르게 진행된다.

## 7. 오류 부재는 궤변이다 (Absence-of-errors is a fallacy)
테스터가 모든 테스트를 실행하고 존재하는 모든 결함을 발견하기를 기대하는 경우도 있지만, 이것은 불가능하다.   
단순히 많은 결함을 발견하고 고쳤다고 해서 시스템의 성공이 보장된다고 생각하는 것은 궤변이다. 

### 참고
http://www.kstqb.org/board_skin/board_list.asp?page=1&bbs_code=4&key=0&word=&etc=ISTQB    
https://velog.io/@rae_gi/%ED%85%8C%EC%8A%A4%ED%8C%85%EC%9D%98-7%EA%B0%80%EC%A7%80-%EC%9B%90%EB%A6%AC   




