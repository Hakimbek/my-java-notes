# What if we call Java run() method directly instead start() method?
- Each thread starts in a separate call stack.
- Invoking the run() method from the main thread, the run() method goes onto the current call stack rather than at the beginning of a new call stack.

```java
class TestCallRun extends Thread {  
   public void run() {  
     for(int i = 1; i < 5; i++) {  
       try {
          Thread.sleep(500);
       } catch(InterruptedException e) {
          System.out.println(e);
       }
       
       System.out.println(i);  
     }  
   }  
 
   public static void main(String args[]){  
     TestCallRun t1 = new TestCallRun();  
     TestCallRun t2 = new TestCallRun();  
   
     t1.run();  
     t2.run();  
   }  
}  
```

### Output:
```
1
2
3
4
1
2
3
4
```
