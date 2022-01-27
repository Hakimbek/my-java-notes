# Thread.sleep() in Java with Examples
The Java Thread class provides the two variant of the sleep() method. First one accepts only an arguments, whereas the other variant accepts two arguments. The method sleep() is being used to halt the working of a thread for a given amount of time. The time up to which the thread remains in the sleeping state is known as the sleeping time of the thread. After the sleeping time is over, the thread starts its execution from where it has left.

```java
class TestSleepMethod extends Thread {    
  public void run() {    
      for(int i = 1; i < 5; i++) {   
        // the thread will sleep for the 500 milli seconds   
        try {
          Thread.sleep(500);
        } catch(InterruptedException e) {
          System.out.println(e);
        } 
        
        System.out.println(i);    
      }    
  }    
 
  public static void main(String args[]) {    
    TestSleepMethod1 t1 = new TestSleepMethod1();    
    TestSleepMethod1 t2 = new TestSleepMethod1();    
     
    t1.start();    
    t2.start();    
  }    
}    
```
