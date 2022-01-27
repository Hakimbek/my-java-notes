# Naming Thread
The Thread class provides methods to change and get the name of a thread. By default, each thread has a name, i.e. thread-0, thread-1 and so on. By we can change the name of the thread by using the setName() method.

```java
class TestMultiNaming extends Thread {  
   public void run() {  
     System.out.println("running...");  
   }  
   
   public static void main(String args[]) {  
     TestMultiNaming t1 = new TestMultiNaming();  
     TestMultiNaming t2 = new TestMultiNaming();  
     System.out.println("Name of t1:" + t1.getName());  
     System.out.println("Name of t2:" + t2.getName());  
   
     t1.start();  
     t2.start();  
  
     t1.setName("Sonoo Jaiswal");  
  System.out.println("After changing name of t1:" + t1.getName());  
   }  
}  
```

### Output:
```
Name of t1:Thread-0
Name of t2:Thread-1
After changing name of t1:Sonoo Jaiswal
running...
running...
```

## Example of currentThread() method

```java
class TestMultiNaming2 extends Thread {  
  public void run() {  
     System.out.println(Thread.currentThread().getName());  
  }  
  
  public static void main(String args[]){  
    TestMultiNaming t1=new TestMultiNaming();  
    TestMultiNaming t2=new TestMultiNaming();  
  
    t1.start();  
    t2.start();  
  }  
}  
```

### Output:
```
Thread-0
Thread-1
```
