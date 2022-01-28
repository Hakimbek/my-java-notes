# Priority of a Thread (Thread Priority)
Each thread has a priority. Priorities are represented by a number between 1 and 10. In most cases, the thread scheduler schedules the threads according to their priority (known as preemptive scheduling). But it is not guaranteed because it depends on JVM specification that which scheduling it chooses. Note that not only JVM a Java programmer can also assign the priorities of a thread explicitly in a Java program.

Setter & Getter Method of Thread Priority
Let's discuss the setter and getter method of the thread priority.

public final int getPriority(): The java.lang.Thread.getPriority() method returns the priority of the given thread.

public final void setPriority(int newPriority): The java.lang.Thread.setPriority() method updates or assign the priority of the thread to newPriority. The method throws IllegalArgumentException if the value newPriority goes out of the range, which is 1 (minimum) to 10 (maximum).

## 3 constants defined in Thread class:
- public static int MIN_PRIORITY
- public static int NORM_PRIORITY
- public static int MAX_PRIORITY

Default priority of a thread is 5 (NORM_PRIORITY). The value of MIN_PRIORITY is 1 and the value of MAX_PRIORITY is 10.

```java
public class ThreadPriorityExample extends Thread {  
  
// Method 1  
// Whenever the start() method is called by a thread  
// the run() method is invoked  
  public void run() {  
    // the print statement  
    System.out.println("Inside the run() method");  
  }  
  
  // the main method  
  public static void main(String argvs[]) {  
    // Creating threads with the help of ThreadPriorityExample class  
    ThreadPriorityExample th1 = new ThreadPriorityExample();  
    ThreadPriorityExample th2 = new ThreadPriorityExample();  
    ThreadPriorityExample th3 = new ThreadPriorityExample();  
  
    // We did not mention the priority of the thread.  
    // Therefore, the priorities of the thread is 5, the default value  
  
    // 1st Thread  
    // Displaying the priority of the thread  
    // using the getPriority() method  
    System.out.println("Priority of the thread th1 is : " + th1.getPriority());  
  
    // 2nd Thread   
    // Display the priority of the thread  
    System.out.println("Priority of the thread th2 is : " + th2.getPriority());  
  
    // 3rd Thread   
    // Display the priority of the thread  
    System.out.println("Priority of the thread th3 is : " + th3.getPriority());  
  
    // Setting priorities of above threads by  
    // passing integer arguments  
    th1.setPriority(6);  
    th2.setPriority(3);  
    th3.setPriority(9);  
  
    // 6  
    System.out.println("Priority of the thread th1 is : " + th1.getPriority());  
  
    // 3  
    System.out.println("Priority of the thread th2 is : " + th2.getPriority());  
  
    // 9  
    System.out.println("Priority of the thread th3 is : " + th3.getPriority());  
  
    // Main thread  
  
    // Displaying name of the currently executing thread   
    System.out.println("Currently Executing The Thread : " + Thread.currentThread().getName());  
  
    System.out.println("Priority of the main thread is : " + Thread.currentThread().getPriority());  
  
    // Priority of the main thread is 10 now  
    Thread.currentThread().setPriority(10);  
  
    System.out.println("Priority of the main thread is : " + Thread.currentThread().getPriority());  
  }  
}  
```

### Output:
```
Priority of the thread th1 is : 5
Priority of the thread th2 is : 5
Priority of the thread th3 is : 5
Priority of the thread th1 is : 6
Priority of the thread th2 is : 3
Priority of the thread th3 is : 9
Currently Executing The Thread : main
Priority of the main thread is : 5
Priority of the main thread is : 10
```
