# Garbage Collection
Garbage Collection(GC) 는 메모리 관리 방법 중에 하나로, 
시스템에서 사용하지 않는 동적 할당된 메모리 블럭을 찾아 자동으로 다시 사용 가능한 자원으로 회수하는것으로 시스템에서 Garbage Collection(GC)을 수행하는 부분을 Garbage Collector(가비지 컬렉터)라고 부른다.

## Garbage Collector(가비지 컬렉터)의 원리
1. 메모리 할당
2. 사용 중인 메모리 인식
3. 사용하지 않는 메모리 인식    

프로그램을 시작할 때 메모리를 관리하는 OS에 프로그램 실행에 필요한 메모리를 요청하게 된다. 이때 메모리를 어디에 저장할지 주소를 할당하는데 주소를 offset 주소라고 부른다.

할당된 메모리들은 프로그램이 돌아가면 Garbage(가비지)가 발생하게 된다. 그래서 Garbage Collector(가비지 컬렉터)는 가비지를 다른 용도로 사용할 수 있도록 메모리를 해체시킨다. 

JVM은 메모리를 부여받고 프로그램을 실행하다가 메모리가 부족해지는 순간이 오면 추가적으로 메모리를 요청한다. 이때  Garbage Collector(가비지 컬렉터)가 실행된다. 

## stop-the-world


## 참고
https://blog.metafor.kr/163     
https://d2.naver.com/helloworld/1329    
