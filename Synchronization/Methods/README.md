# Inter-thread Communication in Java
Inter-thread communication or Co-operation is all about allowing synchronized threads to communicate with each other.

Cooperation (Inter-thread communication) is a mechanism in which a thread is paused running in its critical section and another thread is allowed to enter (or lock) in the same critical section to be executed.It is implemented by following methods of Object class:

- wait()
- notify()
- notifyAll()

# 1) wait() method
The wait() method causes current thread to release the lock and wait until either another thread invokes the notify() method or the notifyAll() method for this object, or a specified amount of time has elapsed.

The current thread must own this object's monitor, so it must be called from the synchronized method only otherwise it will throw exception.

| Method |	Description |
| ------ | ----------- |
| public final void wait() throws InterruptedException |	It waits until object is notified. |
| public final void wait(long timeout) throws InterruptedException |	It waits for the specified amount of time. |

# 2) notify() method
The notify() method wakes up a single thread that is waiting on this object's monitor. If any threads are waiting on this object, one of them is chosen to be awakened. The choice is arbitrary and occurs at the discretion of the implementation.

# 3) notifyAll() method
Wakes up all threads that are waiting on this object's monitor.

# Why wait(), notify() and notifyAll() methods are defined in Object class not Thread class?
It is because they are related to lock and object has a lock.

# Difference between wait and sleep?

| wait() |	sleep() |
| ------ | ------- |
| The wait() method releases the lock. |	The sleep() method doesn't release the lock. |
| It is a method of Object class |	It is a method of Thread class |
| It is the non-static method |	It is the static method |
| It should be notified by notify() or notifyAll() methods |	After the specified amount of time, sleep is completed. |
