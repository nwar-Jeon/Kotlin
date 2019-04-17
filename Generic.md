# Generic

#### 클래스 제네릭 선언

```kotlin
class ClassName<T>(param : T){
  
}
```

#### 함수 제네릭 선언

```kotlin
fun <T> methodName(param : T) : T {
  
}
```

#### out (가변 어노테이션, 선언 위치 가변)

```kotlin
interface Source<out T>{
  fun method() : T
}
```

제네릭이 자기 자신을 반환하기만 할때 사용.

#### in()

```kotlin
interface Consumer<in T>{
  fun consume(item : T)
}
```

제네릭이 파라미터로 들어갈 때 사용.