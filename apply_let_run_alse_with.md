## let

```kotlin
inline fun <T, R> T.let(block: (T) -> R) : R = block(this)
```

## run

```kotlin
inline fun <T, R> T.run(block: T.() -> R): R = block()
```

## apply

```kotlin
inline fun <T> T.apply(block: T.() -> Unit) : T {
  block()
  return this
}
```

## also

```kotlin
inline fun <T> T.alse(block : (T) -> Unit) : T {
  block(this)
  return this
}
```

## with

```kotlin
inline fun <T,R> with(receiver: T, block: T.() -> R): R = receiver.block()
```

