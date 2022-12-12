# Scope functions

## let
* 기본 정의
``` 
inline fun <T, R> T.let(block: (T) -> R): R
```
let은 it로 리시버에 접근하고, 람다함수의 마지막 결과를 리턴하고, 리시버의 여러 함수들을 호출할 때 사용할 수 있다.

Nullable 변수에 주로 많이 사용된다. 즉, 객체가 null이 아닌 코드를 실행하는 경우 사용한다. Null pointer 에러로 발생을 막을 때 꽤나 유용한 범위 함수이다.

### 예시
``` kotlin
fun main() {
//     var hello: String? = null
    var hello: String = "hello"
    val upperCase: String? = hello?.let { it.uppercase() }
    print(upperCase)
}

// 실행결과
HELLO
```
## with
* 기본 정의
```
inline fun <T, R> with(receiver: T, block: T.() -> R): R
```
with은 this로 리시버에 접근하고, 람다함수의 마지막 결과를 리턴한다.

let은 리시버 객체의 확장함수(extension function)로 쓰이지만, with는 그렇지 않다.

with는 리턴값을 사용하지 않는 경우에 쓸 것을 권장하고 있다. 이렇게 사용하면 코드가 간결해지고 가독성이 높아질 수 있습니다.

### 예시
``` kotlin
fun main() {
    val numbers = mutableListOf("one", "two", "three")
    val firstAndLast = with(numbers) {
        "The first element is ${first()}," +
        " the last element is ${last()}"
    }
    println(firstAndLast)
}

// 실행결과
The first element is one, the last element is three
```


## run
* 기본 정의
```
inline fun <T, R> T.run(block: T.() -> R): R
```
run은 this로 리시버에 접근하고, let과 with의 합체 버전으로 객체에 포함된 함수를 실행하고, 함수의 마지막 결과를 리턴한다.

run은 람다함수에서 여러 값을 초기화하고 리턴 값을 어떤 객체의 초기값으로 사용할 때 쓰면 좋다.

### 예시
``` kotlin
fun main() {
    val numbers = mutableListOf("one", "two", "three")
    val countEndsWithE = numbers.run {
        add("four")
        add("five")
        count { it.endsWith("e") }
    }
    println("numbers: $numbers")
    println("There are $countEndsWithE elements that end with e.")
}

// 실행결과
numbers: [one, two, three, four, five]
There are 3 elements that end with e.
```


## apply


### 예시
``` kotlin

```

## also

### 예시
``` kotlin

```

### 참고
https://kotlinlang.org/docs/scope-functions.html
