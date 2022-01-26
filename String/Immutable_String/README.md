# Java String
In Java, string is basically an object that represents sequence of char values. An array of characters works same as Java string. For example:

```java
char[] ch = {'j', 'a', 'v', 'a', 't', 'p', 'o', 'i', 'n', 't'};  
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

## 2. By new keyword

```java
String s = new String("Welcome");  //creates two objects and one reference variable  
```

In such case, JVM will create a new string object in normal (non-pool) heap memory, and the literal "Welcome" will be placed in the string constant pool. The variable s will refer to the object in a heap (non-pool).

# Immutable String in Java
A String is an unavoidable type of variable while writing any application program. String references are used to store various attributes like username, password, etc. In Java, String objects are immutable. Immutable simply means unmodifiable or unchangeable.

Once String object is created its data or state can't be changed but a new String object is created.

# Why String objects are immutable in Java?
As Java uses the concept of String literal. Suppose there are 5 reference variables, all refer to one object "Sachin". If one reference variable changes the value of the object, it will be affected by all the reference variables. That is why String objects are immutable in Java.

Following are some features of String which makes String objects immutable.

## ClassLoader
A ClassLoader in Java uses a String object as an argument. Consider, if the String object is modifiable, the value might be changed and the class that is supposed to be loaded might be different.

To avoid this kind of misinterpretation, String is immutable.

## Thread Safe
As the String object is immutable we don't have to take care of the synchronization that is required while sharing an object across multiple threads.

## Security
As we have seen in class loading, immutable String objects avoid further errors by loading the correct class. This leads to making the application program more secure. Consider an example of banking software. The username and password cannot be modified by any intruder because String objects are immutable. This can make the application program more secure.

## Heap Space
The immutability of String helps to minimize the usage in the heap memory. When we try to declare a new String object, the JVM checks whether the value already exists in the String pool or not. If it exists, the same value is assigned to the new object. This feature allows Java to use the heap space efficiently.

## Why String class is Final in Java?
The reason behind the String class being final is because no one can override the methods of the String class. So that it can provide the same features to the new String objects as well as to the old ones.

# Java String compare
We can compare String in Java on the basis of content and reference.

There are three ways to compare String in Java:

## 1. By Using equals() Method
The String class equals() method compares the original content of the string. It compares values of string for equality. String class provides the following two methods:
- public boolean equals(Object another) compares this string to the specified object.
- public boolean equalsIgnoreCase(String another) compares this string to another string, ignoring case.

## 2. By Using == operator
The == operator compares references not values.

## 3. By Using compareTo() method
The String class compareTo() method compares values lexicographically and returns an integer value that describes if first string is less than, equal to or greater than second string.

Suppose s1 and s2 are two String objects. If:

- s1 == s2 : The method returns 0.
- s1 > s2 : The method returns a positive value.
- s1 < s2 : The method returns a negative value.
