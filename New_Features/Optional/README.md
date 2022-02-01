# Optional Class
Optional is a container object used to contain not-null objects. Optional object is used to represent null with absent value. This class has various utility methods to facilitate code to handle values as ‘available’ or ‘not available’ instead of checking null values.

| Method | Description |
| ------ | ----------- |
| static <T> Optional<T> empty() | Returns an empty Optional instance. |
| boolean equals(Object obj) | Indicates whether some other object is "equal to" this Optional. |
| Optional<T> filter(Predicate<? super <T> predicate) | If a value is present and the value matches a given predicate, it returns an Optional describing the value, otherwise returns an empty Optional. |
| <U> Optional<U> flatMap(Function<? super T,Optional<U>> mapper) | If a value is present, it applies the provided Optional-bearing mapping function to it, returns that result, otherwise returns an empty Optional. |
| T get() | If a value is present in this Optional, returns the value, otherwise throws NoSuchElementException. |
| int hashCode() | Returns the hash code value of the present value, if any, or 0 (zero) if no value is present. |
| void ifPresent(Consumer<? super T> consumer) | If a value is present, it invokes the specified consumer with the value, otherwise does nothing. |
| boolean isPresent() | Returns true if there is a value present, otherwise false. | 
| <U>Optional<U> map(Function<? super T,? extends U> mapper) | If a value is present, applies the provided mapping function to it, and if the result is non-null, returns an Optional describing the result. |
| static <T> Optional<T> of(T value) | Returns an Optional with the specified present non-null value. |
| static <T> Optional<T> ofNullable(T value) | Returns an Optional describing the specified value, if non-null, otherwise returns an empty Optional. |
| T orElse(T other) | Returns the value if present, otherwise returns other. |
| T orElseGet(Supplier<? extends T> other) | Returns the value if present, otherwise invokes other and returns the result of that invocation. |
| <X extends Throwable> T orElseThrow(Supplier<? extends X> exceptionSupplier) | Returns the contained value, if present, otherwise throws an exception to be created by the provided supplier. |
| String toString() | Returns a non-empty string representation of this Optional suitable for debugging. |

Java 11 introduced new method to Optional class as isEmpty() to check if value is present. isEmpty() returns false if value is present otherwise true.

It can be used as an alternative of isPresent() method which often needs to negate to check if value is not present.
