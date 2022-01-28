# Synchronization in Java
Synchronization in Java is the capability to control the access of multiple threads to any shared resource.

Java Synchronization is better option where we want to allow only one thread to access the shared resource.

## Why use Synchronization?
1. To prevent thread interference.
2. To prevent consistency problem.

# Types of Synchronization
1. Process Synchronization
2. Thread Synchronization

Here, we will discuss only thread synchronization.

# Thread Synchronization
There are two types of thread synchronization mutual exclusive and inter-thread communication.

## Mutual Exclusive
 - ### Synchronized method.
 - ### Synchronized block.
 - ### Static synchronization.
## Cooperation (Inter-thread communication in java)

# Mutual Exclusive
Mutual Exclusive helps keep threads from interfering with one another while sharing data. It can be achieved by using the following three ways:

- By Using Synchronized Method
- By Using Synchronized Block
- By Using Static Synchronization

## Understanding the problem without Synchronization

```java
class Table {  
   void printTable(int n) { //method not synchronized  
      for(int i = 1; i <= 5; i++){  
         System.out.println(n * i);  
         try {  
            Thread.sleep(400);  
         } catch(Exception e){
            System.out.println(e);
         }  
      }  
  
   }  
}  
  
class MyThread1 extends Thread {  
   Table t;  

   MyThread1(Table t) {  
      this.t = t;  
   }  
   
   public void run() {  
      t.printTable(5);  
   }   
  
}  

class MyThread2 extends Thread{  
   Table t;  

   MyThread2(Table t){  
      this.t = t;  
   }  
   
   public void run() {  
      t.printTable(100);  
   }  
}  
  
class TestSynchronization {  
   public static void main(String args[]){  
      Table obj = new Table(); //only one object  
      MyThread1 t1=new MyThread1(obj);  
      MyThread2 t2=new MyThread2(obj);  
      t1.start();  
      t2.start();  
   }  
}  
```

### Output:

```
 5
 100
 10
 200
 15
 300
 20
 400
 25
 500
```

# Java Synchronized Method
If you declare any method as synchronized, it is known as synchronized method.

Synchronized method is used to lock an object for any shared resource.

When a thread invokes a synchronized method, it automatically acquires the lock for that object and releases it when the thread completes its task.

```java
```java
class Table {  
   synchronized void printTable(int n) { //method not synchronized  
      for(int i = 1; i <= 5; i++){  
         System.out.println(n * i);  
         try {  
            Thread.sleep(400);  
         } catch(Exception e){
            System.out.println(e);
         }  
      }  
  
   }  
}  
  
class MyThread1 extends Thread {  
   Table t;  

   MyThread1(Table t) {  
      this.t = t;  
   }  
   
   public void run() {  
      t.printTable(5);  
   }   
  
}  

class MyThread2 extends Thread{  
   Table t;  

   MyThread2(Table t){  
      this.t = t;  
   }  
   
   public void run() {  
      t.printTable(100);  
   }  
}  
  
class TestSynchronization {  
   public static void main(String args[]){  
      Table obj = new Table(); //only one object  
      MyThread1 t1=new MyThread1(obj);  
      MyThread2 t2=new MyThread2(obj);  
      t1.start();  
      t2.start();  
   }  
}  
```
### Output:
```
5
10
15
20
25
100
200
300
400
500
```

# Synchronized Block in Java
Synchronized block can be used to perform synchronization on any specific resource of the method. Suppose we have 50 lines of code in our method, but we want to synchronize only 5 lines, in such cases, we can use synchronized block. If we put all the codes of the method in the synchronized block, it will work same as the synchronized method.

## Points to Remember
- Synchronized block is used to lock an object for any shared resource.
- Scope of synchronized block is smaller than the method.
- A Java synchronized block doesn't allow more than one JVM, to provide access control to a shared resource.
- The system performance may degrade because of the slower working of synchronized keyword.
- Java synchronized block is more efficient than Java synchronized method.

```java
class Sender   
{   
  public void SenderMsg(String msg)  
  {   
    System.out.println("\nSending a Message: "  + msg);  
    try  
    {   
      Thread.sleep(800);   
    }   
    catch (Exception e)   
    {   
      System.out.println("Thread interrupted.");   
    }   
    System.out.println("\n" +msg+ "Sent");  
  }  
}   
// A Sender class for sending a message using Threads   
class SenderWThreads extends Thread   
{   
  private String msg;   
  Sender sd;   
  
  // Receiver method to receive a message object and a message to be sent   
  SenderWThreads(String m, Sender obj)  
  {   
    msg = m;  
    sd = obj;   
  }   
  
  public void run()   
  {   
    // Checks that only one thread sends a message at a time.   
    synchronized(sd)   
    {   
      // synchronizing the sender object   
      sd.SenderMsg(msg);  
    }   
  }   
}   
// Driver Code   
public class ShynchronizedMultithreading  
{   
  public static void main(String args[])   
  {   
    Sender sender = new Sender();   
    SenderWThreads sender1 = new SenderWThreads( "Hola " , sender);  
SenderWThreads sender2 =  new SenderWThreads( "Welcome to Javatpoint website ", sender);  
  
    // Start two threads of SenderWThreads type   
    sender1.start();   
    sender2.start();   
  
    // wait for threads to end   
    try  
    {   
      sender1.join();   
      sender2.join();   
    }   
    catch(Exception e)   
    {   
      System.out.println("Interrupted");   
    }   
  }   
}  
```
