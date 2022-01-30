# Java Annotations
Java Annotation is a tag that represents the metadata i.e. attached with class, interface, methods or fields to indicate some additional information which can be used by java compiler and JVM.

Annotations in Java are used to provide additional information, so it is an alternative option for XML and Java marker interfaces.

## Built-In Java Annotations used in Java code
- @Override
- @SuppressWarnings
- @Deprecated
## Built-In Java Annotations used in other annotations
- @Target
- @Retention
- @Inherited
- @Documented

## @Override
@Override annotation assures that the subclass method is overriding the parent class method. If it is not so, compile time error occurs.

## @SuppressWarnings
@SuppressWarnings annotation: is used to suppress warnings issued by the compiler.

## @Deprecated
@Deprecated annoation marks that this method is deprecated so compiler prints warning. It informs user that it may be removed in the future versions. So, it is better not to use such methods.

# Java Custom Annotations
Java Custom annotations or Java User-defined annotations are easy to create and use. The @interface element is used to declare an annotation. For example:
```java
@interface MyAnnotation{}  
```

## Points to remember for java custom annotation signature

1. Method should not have any throws clauses
2. Method should return one of the following: primitive data types, String, Class, enum or array of these data types.
3. Method should not have any parameter.
4. We should attach @ just before interface keyword to define annotation.
5. It may assign a default value to the method.

# Types of Annotation
There are three types of annotations.

## Marker Annotation
An annotation that has no method, is called marker annotation.
```java
@interface MyAnnotation{}  
```

## Single-Value Annotation
An annotation that has one method, is called single-value annotation.
```java
@interface MyAnnotation{  
int value();  
}  
```

We can provide the default value also. For example:
```java
@interface MyAnnotation{  
int value() default 0;  
}  
```

### How to apply Single-Value Annotation
Let's see the code to apply the single value annotation.
```java
@MyAnnotation(value=10)  
```

## Multi-Value Annotation
An annotation that has more than one method, is called Multi-Value annotation. For example:
```java
@interface MyAnnotation {  
  int value1();  
  String value2();  
  String value3();  
}  
```
