# Object class in Java
The Object class is the parent class of all the classes in java by default. In other words, it is the topmost class of java.

The Object class is beneficial if you want to refer any object whose type you don't know. Notice that parent class reference variable can refer the child class object, know as upcasting.

The Object class provides some common behaviors to all the objects such as object can be compared, object can be cloned, object can be notified etc.

## Methods of Object class

| Method |	Description |
| ------ | ----------- |
| public final Class getClass() |	returns the Class class object of this object. The Class class can further be used to get the metadata of this class. |
| public int hashCode() |	returns the hashcode number for this object. |
| public boolean equals(Object obj) |	compares the given object to this object. |
| protected Object clone() throws CloneNotSupportedException |	creates and returns the exact copy (clone) of this object. |
| public String toString() |	returns the string representation of this object. |
| public final void notify() |	wakes up single thread, waiting on this object's monitor. |
| public final void notifyAll() |	wakes up all the threads, waiting on this object's monitor. |
| public final void wait(long timeout) throws InterruptedException	| causes the current thread to wait for the specified milliseconds, until another thread notifies (invokes notify() or notifyAll() method). |
| public final void wait(long timeout, int nanos) throws InterruptedException |	causes the current thread to wait for the specified milliseconds and nanoseconds, until another thread notifies (invokes notify() or notifyAll() method). |
| public final void wait() throws InterruptedException |	causes the current thread to wait, until another thread notifies (invokes notify() or notifyAll() method). |
| protected void finalize() throws Throwable |	is invoked by the garbage collector before object is being garbage collected.

# Object Cloning in Java
The object cloning is a way to create exact copy of an object. The clone() method of Object class is used to clone an object.

The java.lang.Cloneable interface must be implemented by the class whose object clone we want to create. If we don't implement Cloneable interface, clone() method generates CloneNotSupportedException.

The clone() method is defined in the Object class. Syntax of the clone() method is as follows:

```java
protected Object clone() throws CloneNotSupportedException  
```

## Why use clone() method ?
The clone() method saves the extra processing task for creating the exact copy of an object. If we perform it by using the new keyword, it will take a lot of processing time to be performed that is why we use object cloning.

## Advantage of Object cloning

- You don't need to write lengthy and repetitive codes. Just use an abstract class with a 4- or 5-line long clone() method.
- It is the easiest and most efficient way for copying objects, especially if we are applying it to an already developed or an old project. Just define a parent class, implement Cloneable in it, provide the definition of the clone() method and the task will be done.
- Clone() is the fastest way to copy array.

## Disadvantage of Object cloning

- To use the Object.clone() method, we have to change a lot of syntaxes to our code, like implementing a Cloneable interface, defining the clone() method and handling CloneNotSupportedException, and finally, calling Object.clone() etc.
- We have to implement cloneable interface while it doesn't have any methods in it. We just have to use it to tell the JVM that we can perform clone() on our object.
- Object.clone() is protected, so we have to provide our own clone() and indirectly call Object.clone() from it.
- Object.clone() doesn't invoke any constructor so we don't have any control over object construction.
- If you want to write a clone method in a child class then all of its superclasses should define the clone() method in them or inherit it from another parent class. Otherwise, the super.clone() chain will fail.
- Object.clone() supports only shallow copying but we will need to override it if we need deep cloning.
