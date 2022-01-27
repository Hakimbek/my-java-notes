# Java Threads | How to create a thread in Java
There are two ways to create a thread:

# Thread class
Thread class provide constructors and methods to create and perform operations on a thread.Thread class extends Object class and implements Runnable interface.

## Commonly used Constructors of Thread class:
- Thread()
- Thread(String name)
- Thread(Runnable r)
- Thread(Runnable r,String name)

```java
class Multi extends Thread {  
  public void run() {  
    System.out.println("thread is running...");  
  } 
  
  public static void main(String args[]) {  
     Multi t = new Multi();  
     t.start();  
  }  
}  
```

### Output:
```
thread is running...
```

# Runnable interface:
The Runnable interface should be implemented by any class whose instances are intended to be executed by a thread. Runnable interface have only one method named run().

```java
public void run(): // is used to perform action for a thread.
```

```java
class Multi implements Runnable {  
  public void run() {  
     System.out.println("thread is running...");  
  }  
  
  public static void main(String args[]){  
     Multi m = new Multi();  
     Thread t = new Thread(m);   // Using the constructor Thread(Runnable r)  
     t.start();  
  }  
}  
```

### Output:
```
thread is running...
```

# Starting a thread:
The start() method of Thread class is used to start a newly created thread. It performs the following tasks:

- A new thread starts(with new callstack).
- The thread moves from New state to the Runnable state.
- When the thread gets a chance to execute, its target run() method will run.

# Thread Scheduler in Java
A component of Java that decides which thread to run or execute and which thread to wait is called a thread scheduler in Java. In Java, a thread is only chosen by a thread scheduler if it is in the runnable state. However, if there is more than one thread in the runnable state, it is up to the thread scheduler to pick one of the threads and ignore the other ones. There are some criteria that decide which thread will execute first. There are two factors for scheduling a thread i.e. Priority and Time of arrival.

## Priority
Priority of each thread lies between 1 to 10. If a thread has a higher priority, it means that thread has got a better chance of getting picked up by the thread scheduler.

## Time of Arrival
Suppose two threads of the same priority enter the runnable state, then priority cannot be the factor to pick a thread from these two threads. In such a case, arrival time of thread is considered by the thread scheduler. A thread that arrived first gets the preference over the other threads.

# Can we start a thread twice
No. After starting a thread, it can never be started again. If you does so, an IllegalThreadStateException is thrown. In such case, thread will run once but for second time, it will throw exception.

```java
public class TestThreadTwice extends Thread {  
  public void run() {  
    System.out.println("running...");  
  }  
  
  public static void main(String args[]) {  
    TestThreadTwice t = new TestThreadTwice1();  
    t.start();  
    t.start();  
  }  
}  
```

### Output:
```
running
Exception in thread "main" java.lang.IllegalThreadStateException
```
