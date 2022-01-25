# Object
Any entity that has state and behavior is known as an object. For example, a chair, pen, table, keyboard, bike, etc.

An Object can be defined as an instance of a class. An object contains an address and takes up some space in memory. Objects can communicate without knowing the details of each other's data or code. The only necessary thing is the type of message accepted and the type of response returned by the objects.

An object in Java is the physical as well as a logical entity, whereas, a class in Java is a logical entity only.

An object has three characteristics:

## State
  - represents the data (value) of an object.
## Behavior
  - represents the behavior (functionality) of an object.
## Identity
  - An object identity is typically implemented via a unique ID. The value of the ID is not visible to the external user. However, it is used internally by the JVM to identify each object uniquely.

## new keyword in Java
The new keyword is used to allocate memory at runtime. All objects get memory in Heap memory area.

There are many ways to create an object in java. They are:

- By new keyword
- By newInstance() method
- By clone() method
- By deserialization
- By factory method etc.

## Anonymous object
Anonymous simply means nameless. An object which has no reference is known as an anonymous object. It can be used at the time of object creation only.

```java
new Calculation(); //anonymous object  
```
