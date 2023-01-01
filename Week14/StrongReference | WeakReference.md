# StrongReference | WeakReference
Reference는 메모리 누수를 막기 위해서 사용    
Reference의 종류는 StrongReference,SoftReference, WeakReference가 있다.   
StrongReference를 제외하고 Reference<T>를 상속받고 있다. Reference는 GC(Garbage Collection)와 연관이 있다.   

## StrongReference (강한 참조)
StrongReference (강한 참조)는 객체를 생성하게 되면 생기게 되는 참조   
StrongReference (강한 참조)를 통해 참조되고 있는 객체는 GC(Garbage Collection)의 대상에서 제외된다.   
GC(Garbage Collection)가 발생해도 객체가 해제되지 않기 때문에 OOM(Out of memory)이 발생할 수 있다.
 
## WeakReference (약한 참조)
WeakReference (약한 참조)는 짧은 주기에 자주 사용되는 객체를 캐시 할 때 유용한 참조      
WeakReference (약한 참조)는 GC(Garbage Collection)가 발생하면 무조건 수거되며 WeakReference (약한 참조)가 사라지는 시점이 GC(Garbage Collection)의 실행 주기와 일치한다.
 
## SoftReference
StrongReference (강한 참조)와는 다르게 GC(Garbage Collection)에 의해 수거될 수도 있고, 수거되지 않을 수도 있다.    
메모리에 충분한 여유가 있다면 GC(Garbage Collection)가 수행되고 있다 하더라도 수거되지 않는다.   
GC(Garbage Collection)가 발생하면 수거되므로 OOM(Out of memory)의 위험성을 줄일 수 있다.      
메모리가 적은 모바일 기기 특성상 WeakReference (약한 참조)와 동작하는게 크게 다르지 않다.     

### 참고
https://dongsik93.github.io/til/2022/01/09/til-kotlin-weak-reference/    
https://developer.android.com/reference/kotlin/java/lang/ref/Reference    
https://d2.naver.com/helloworld/329631   
https://myseong.tistory.com/7   
https://jwsoft91.tistory.com/213    
