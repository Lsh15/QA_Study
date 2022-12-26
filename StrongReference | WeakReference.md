# StrongReference | WeakReference
Reference는 메모리 누수를 막기 위해서 사용    
Reference의 종류는 StrongReference,SoftReference, WeakReference가 있다.   
StrongReference를 제외하고 Reference<T>를 상속받고 있다. Reference는 GC(Garbage Collection)와 연관이 있다.   

## StrongReference (강한 참조)
객체를 생성하게 되면 생기게 되는 참조   
StrongReference (강한 참조)를 통해 참조되고 있는 객체는 GC(Garbage Collection)의 대상에서 제외된다.   
GC(Garbage Collection)가 발생해도 객체가 해제되지 않기 때문에 OOM(Out of memory)이 발생할 수 있다.
 
## WeakReference


## Soft Reference



### 참고
https://dongsik93.github.io/til/2022/01/09/til-kotlin-weak-reference/    
https://developer.android.com/reference/kotlin/java/lang/ref/Reference    
https://d2.naver.com/helloworld/329631   
https://myseong.tistory.com/7   
https://jwsoft91.tistory.com/213    
