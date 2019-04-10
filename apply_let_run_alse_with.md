## let

```kotlin
inline fun <T, R> T.let(block: (T) -> R) : R = block(this)
```



### ex)

```kotlin

```

## run

```kotlin
inline fun <T, R> T.run(block: T.() -> R): R = block()
```

지역변수 범위제한, 명시적 매개변수를 암시적 수신객체로 변환

### ex)

```kotlin

```

## apply

```kotlin
inline fun <T> T.apply(block: T.() -> Unit) : T {
  block()
  return this
}
```

객체의 프로퍼티를 초기화하고, 객체 자신을 반환함. (it 사용 x.)

### ex)

```kotlin

```

## also

```kotlin
inline fun <T> T.alse(block : (T) -> Unit) : T {
  block(this)
  return this
}
```

수신 객체의 프로퍼티 데이터의 유효성을 검사할 때. (it 사용.)

### ex)

```kotlin

```

## with

```kotlin
inline fun <T,R> with(receiver: T, block: T.() -> R): R = receiver.block()
```

수신 객체가 non-nullable이고, 결과가 필요하지 않은 경우에 사용.

### ex)

```kotlin

```

