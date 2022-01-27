# Java join() method
The join() method in Java is provided by the java.lang.Thread class that permits one thread to wait until the other thread to finish its execution. Suppose th be the object the class Thread whose thread is doing its execution currently, then the th.join(); statement ensures that th is finished before the program does the execution of the next statement. When there are more than one thread invoking the join() method, then it leads to overloading on the join() method that permits the developer or programmer to mention the waiting period. However, similar to the sleep() method in Java, the join() method is also dependent on the operating system for the timing, so we should not assume that the join() method waits equal to the time we mention in the parameters. The following are the three overloaded join() methods.

```java
class TestJoinMethod extends Thread {    
  public void run() {    
    for(int i = 1; i < 5; i++) {    
      try {    
        Thread.sleep(500);    
      } catch(Exception e) {
        System.out.println(e);
      } 
      
      System.out.println(i);    
    }    
  }  
 
  public static void main(String args[]) {    
    TestJoinMethod t1=new TestJoinMethod();    
    TestJoinMethod t2=new TestJoinMethod();    
    TestJoinMethod t3=new TestJoinMethod();    
    
    t1.start();    
    
    try{    
      t1.join();    
    } catch(Exception e) {
      System.out.println(e);
    }    
    
    t2.start();    
    t3.start();    
  }    
}    
```

### Output:

```
 1
 2
 3
 4
 5
 1
 1
 2
 2
 3
 3
 4
 4
 5
 5
```
