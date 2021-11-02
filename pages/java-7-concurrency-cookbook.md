# Java 7 Concurrency Cookbook

[> Home](../README.md)
## Using atomic arrays



Java also introduced atomic arrays that provide atomic operations for arrays of integer or long numbers. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch06s09.html#cda7a6f9-35cf-472c-a762-5f54f2fdd66b))

## Using atomic variables



This operation is called Compare and Set
. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch06s08.html#721a9d0e-41f4-4fc5-8233-b42eab34474f))


To avoid these problems, Java introduced the atomic variables. When a thread is doing an operation with an atomic variable, if other threads want to do an operation with the same variable, the implementation of the class includes a mechanism to check that the operation is done in one step. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch06s08.html#0a953b0b-647c-48b5-a2ce-32c3b5f2b1f2))

## Using conditions in synchronized code



First, check if the storage is full or not. If it's full, it calls the wait() method until the storage has empty space. At the end of the method, we call the notifyAll() method to wake up all the threads that are sleeping in the wait() method. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch02s04.html#ea063e2d-177e-45ce-917a-76254920d69c))


A classic problem in concurrent programming is the producer-consumer problem. We have a data buffer, one or more producers of data that save it in the buffer and one or more consumers of data that take it from the buffer. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch02s04.html#7aeb2f23-2352-454b-af7d-e05265568523))

## Synchronizing a method



In other words, every method declared with the synchronized keyword is a critical section and Java only allows the execution of one of the critical sections of an object. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch02s02.html#64bfa2cd-5ecf-4134-bb82-c1c0487f0039))


Vikram: [If an object has two synchronized methods, and one thread is accessing one of those synchronized methods, another thread cannot access the other synchronized method. It's as if all synchronized methods within a object form a critical section that only one thread can access at time. However, static synchronized method can still be accessed by other threads. ]

## Synchronizing a block of code with a Lock



The Lock interfaces allow a separation of read and write operations having multiple readers and only one modifier. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch02s05.html#350f6eee-1c24-42c1-b266-8744f68d4a2e))


Vikram: [Don't see why this can't be done with two separate synchronized objects]


One of the new functionalities is implemented by the tryLock() method. This method tries to get the control of the lock and if it can't, because it's used by other thread, it returns the lock. With the synchronized keyword, when a thread (A) tries to execute a synchronized block of code, if there is another thread (B) executing it, the thread (A) is suspended until the thread (B) finishes the execution of the synchronized block. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch02s05.html#9fa89a9c-3e7f-4d00-928d-91175719f593))


Vikram: [When using synchronized, threads wait, whereas with tryLock(), thread returns]

## 2. Basic Thread Synchronization



The solution for these problems comes with the concept of critical section
. A critical section is a block of code that accesses a shared resource and can't be executed by more than one thread at the same time. ([link](https://learning.oreilly.com/library/view/-/9781849687881/ch02.html#5c269daf-b85b-47a0-827f-658bb21b5499))

[> Home](../README.md)