# Java String
In Java, string is basically an object that represents sequence of char values. An array of characters works same as Java string. For example:

```java
char[] ch={'j', 'a', 'v', 'a', 't', 'p', 'o', 'i', 'n', 't'};  
String s = new String(ch);  
```
is same as:
```java
String s = "javatpoint";  
```

Java String class provides a lot of methods to perform operations on strings such as compare(), concat(), equals(), split(), length(), replace(), compareTo(), intern(), substring() etc.

The *java.lang.String* class implements *Serializable, Comparable* and *CharSequence* interfaces.

# CharSequence Interface
The CharSequence interface is used to represent the sequence of characters. String, StringBuffer and StringBuilder classes implement it. It means, we can create strings in Java by using *String, StringBuilder* and *StringBuffer* classes.

The Java String is immutable which means it cannot be changed. Whenever we change any string, a new instance is created. For mutable strings, you can use StringBuffer and StringBuilder classes.

# How to create a string object?

## 1. String Literal
Java String literal is created by using double quotes. For Example:

```java
String s = "welcome";  
```

Each time you create a string literal, the JVM checks the "string constant pool" first. If the string already exists in the pool, a reference to the pooled instance is returned. If the string doesn't exist in the pool, a new string instance is created and placed in the pool. For example:

```java
String s1 = "Welcome";  
String s2 = "Welcome";  //It doesn't create a new instance  
```

### Note
  - String objects are stored in a special memory area known as the "string constant pool".

## Why Java uses the concept of String literal?
To make Java more memory efficient (because no new objects are created if it exists already in the string constant pool).
