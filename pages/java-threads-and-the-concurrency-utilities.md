# Java Threads and the Concurrency Utilities

[> Home](../README.md)
## Chapter 2 : Synchronization



Java provides a special thread-safety guarantee concerning immutable objects. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#fd6a3d4c-df0a-4116-b8df-7d4c0549c6e1))


When a field variable is declared volatile, it cannot also be declared final. However, this isn’t a problem because Java also lets you safely access a final field without the need for synchronization ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#337db0c1-38e6-4cf0-9683-053fb0c8a3cb))


Because stopped has been marked volatile, each thread will access the main memory copy of this variable and not access a cached copy. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#c6c8641a-8e9b-414d-9b45-152325af22f9))


Multithreaded applications face the additional liveness challenges of deadlock, livelock, and starvation: ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#5ecf7b7f-4546-4048-b89a-3caf89c71ea7))


Two or more threads that access the same code sequence must acquire the same lock or there will be no synchronization. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#8c5884bb-b9ae-4eb7-b1e3-20bab2ff6f04))


Suppose you specify the following code sequence:
System.out.println(ID.getID());
The lock is associated with ID.class, the Class object associated with ID. If another thread called ID.getID() while this method was executing, the other thread would have to wait until the executing thread released the lock. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#12f6c21d-d753-4914-96b5-62830967de83))


This property of synchronization is known as mutual exclusion because each thread is mutually excluded from executing in a critical section when another thread is inside the critical section. For this reason, the lock that the thread acquires is often referred to as a mutex lock. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#bd20d391-ae2a-439d-98c3-f0ca28489f36))


Synchronization is a JVM feature that ensures that two or more concurrent threads don’t simultaneously execute a critical section, which is a code section that must be accessed in a serial (one thread at a time) manner. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#59ea5dd2-cd96-4051-a232-9ad8dd8277cf))


A race condition is often confused with a data race in which two or more threads (in a single application) access the same memory location concurrently, at least one of the accesses is for writing, and these threads don’t coordinate their accesses to that memory. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#7e02755d-e652-44ae-bb79-a466393f6825))


Because there is no happens-before ordering (one action must precede another action) between thread 1’s write of parser and thread 2’s read of parser (because there is no coordinated access to parser), a data race has occurred. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#96d9a68c-ee12-4083-8f14-0c60583c5c60))


Although it might look like a single operation, expression counter++ is actually three separate operations: read counter’s value, add 1 to this value, and store the updated value in counter. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#89b19d09-593b-4776-8b5c-81c9da76f651))


Another type of race condition is read-modify-write, in which new state is derived from previous state. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#d94f7429-b1df-4cec-a83c-74ff4f6f0d6d))


A race condition occurs when the correctness of a computation depends on the relative timing or interleaving of multiple threads by the scheduler. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#24caa701-bef3-44c1-a2d8-c74a2c3f75d6))


The code fragment is an example of a common type of race condition that’s known as check-then-act, in which a potentially stale observation is used to decide on what to do next. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch02.xhtml#593b3703-1cc6-4eda-a450-95cc67d76fd9))

## Chapter 1 : Threads and Runnables



A daemon thread is a thread that acts as a helper to a nondaemon thread and dies automatically when the application’s last nondaemon thread dies so that the application can terminate. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch01.xhtml#2ccb8689-b488-4b3c-b4e0-cf7eff9e4c60))


Two terms that are commonly encountered when exploring threads are parallelism and concurrency. According to Oracle’s “Multithreading Guide” (http://docs.oracle.com/cd/E19455-01/806-5257/6je9h032b/index.html), parallelism is “a condition that arises when at least two threads are executing simultaneously.” In contrast, concurrency is “a condition that exists when at least two threads are making progress. [It is a] more generalized form of parallelism that can include time-slicing as a form of virtual parallelism.” ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch01.xhtml#ba3383b9-5d35-4d43-b92c-af6f6d548a84))


There are two ways to create a Runnable object. The first way is to create an anonymous class that implements Runnable, as follows:
Runnable r = new Runnable()             {                @Override                public void run()                {                   // perform some work                   System.out.println("Hello from thread");                }             };
Before Java 8, this was the only way to create a runnable. Java 8 introduced the lambda expression to more conveniently create a runnable:
Runnable r = () -> System.out.println("Hello from thread"); ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch01.xhtml#206f13e7-be07-405d-a7c7-d3560b3d3490))


These threads execute code sequences encapsulated in objects that are known as runnables. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch01.xhtml#0c014b5b-2cf4-49b1-b3ed-eef3d4c1284a))

## Chapter 5: Concurrency Utilities and Executors



The concurrency utilities include executors as a high-level alternative to low-level thread expressions for executing runnable tasks. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch05.xhtml#2bcf6013-8c07-428c-a657-b6451a07c1e3))


The concurrency utilities can be classified as executors, synchronizers, a locking framework, and more. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch05.xhtml#41be505a-2d69-4f73-9910-be1efcf4965f))

## Chapter 4:Additional Thread Capabilities



Timer Framework ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch04.xhtml#2f7ffb9c-45bd-46ce-96fc-74ede3a9d625))


Vikram: [Read later]


Each ThreadLocal instance describes a thread-local variable, which is a variable that provides a separate storage slot to each thread that accesses the variable. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch04.xhtml#e5dc64f0-1d96-4329-8334-39245e0064ee))


This problem is an example of the “time of check to time of use” (https://en.wikipedia.org/wiki/Time_of_check_to_time_of_use) class of software bug. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch04.xhtml#e8e14548-2db7-48df-ba74-6d3a24f685fa))


Using a ThreadGroup object, you can perform an operation on all contained Thread objects. ([link](https://learning.oreilly.com/library/view/-/9781484217009/9781484216996_Ch04.xhtml#e49dfd22-eb5b-4d65-b5a1-7c1202dccc35))

[> Home](../README.md)