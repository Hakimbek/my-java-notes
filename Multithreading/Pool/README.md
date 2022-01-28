# Java Thread Pool
Java Thread pool represents a group of worker threads that are waiting for the job and reused many times.

In the case of a thread pool, a group of fixed-size threads is created. A thread from the thread pool is pulled out and assigned a job by the service provider. After completion of the job, the thread is contained in the thread pool again.

## Thread Pool Methods
### newFixedThreadPool(int s)
  - The method creates a thread pool of the fixed size s.

### newCachedThreadPool()
  - The method creates a new thread pool that creates the new threads when needed but will still use the previously created thread whenever they are available to use.

### newSingleThreadExecutor()
  - The method creates a new thread.

# Advantage of Java Thread Pool
Better performance It saves time because there is no need to create a new thread.

# Real time usage
It is used in Servlet and JSP where the container creates a thread pool to process the request.

### WorkerThread.java
```java
class WorkerThread implements Runnable {  
    private String message;  
    
    public WorkerThread(String s) {  
        this.message = s;  
    }  
    
     public void run() {  
        System.out.println(Thread.currentThread().getName() + " (Start) message = " + message);  
        processMessage(); //call processMessage method that sleeps the thread for 2 seconds  
        System.out.println(Thread.currentThread().getName() + " (End)");  //prints thread name  
    }
    
    private void processMessage() {  
        try {  
           Thread.sleep(2000);  
        } catch (InterruptedException e) { 
           e.printStackTrace(); 
        }  
    }  
}  
```

### TestThreadPool.java

```java
public class TestThreadPool {  
     public static void main(String[] args) {  
        ExecutorService executor = Executors.newFixedThreadPool(5); //creating a pool of 5 threads  
        
        for (int i = 0; i < 10; i++) {  
            Runnable worker = new WorkerThread("" + i);  
            executor.execute(worker); //calling execute method of ExecutorService  
        }
        
        executor.shutdown();  
        while (!executor.isTerminated()) {   }  
  
        System.out.println("Finished all threads");  
    }  
 }  
```

### Output:
```
pool-1-thread-1 (Start) message = 0
pool-1-thread-2 (Start) message = 1
pool-1-thread-3 (Start) message = 2
pool-1-thread-5 (Start) message = 4
pool-1-thread-4 (Start) message = 3
pool-1-thread-2 (End)
pool-1-thread-2 (Start) message = 5
pool-1-thread-1 (End)
pool-1-thread-1 (Start) message = 6
pool-1-thread-3 (End)
pool-1-thread-3 (Start) message = 7
pool-1-thread-4 (End)
pool-1-thread-4 (Start) message = 8
pool-1-thread-5 (End)
pool-1-thread-5 (Start) message = 9
pool-1-thread-2 (End)
pool-1-thread-1 (End)
pool-1-thread-4 (End)
pool-1-thread-3 (End)
pool-1-thread-5 (End)
Finished all threads
```

# Risks involved in Thread Pools

## Deadlock
It is a known fact that deadlock can come in any program that involves multithreading, and a thread pool introduces another scenario of deadlock. Consider a scenario where all the threads that are executing are waiting for the results from the threads that are blocked and waiting in the queue because of the non-availability of threads for the execution.

## Thread Leakage
Leakage of threads occurs when a thread is being removed from the pool to execute a task but is not returning to it after the completion of the task. For example, when a thread throws the exception and the pool class is not able to catch this exception, then the thread exits and reduces the thread pool size by 1. If the same thing repeats a number of times, then there are fair chances that the pool will become empty, and hence, there are no threads available in the pool for executing other requests.

## Resource Thrashing
A lot of time is wasted in context switching among threads when the size of the thread pool is very large. Whenever there are more threads than the optimal number may cause the starvation problem, and it leads to resource thrashing.
