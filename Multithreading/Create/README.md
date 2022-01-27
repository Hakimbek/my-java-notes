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
