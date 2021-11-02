# Mastering Concurrency Programming with Java 8

[> Home](../README.md)
## A methodology to design concurrent algorithms



If you split the algorithm into fewer tasks than cores (coarse-grained granularity), you are not taking advantage of all the resources ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s03.html#2c1ef7cc-9dba-43ce-960b-da60575c5c29))


It's based on the one presented by Intel in their Threading Methodology: Principles and Practices document. ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s03.html#35bf2913-ad04-4212-84c6-3d1356683b7a))

## Tips and tricks to design concurrent algorithms



Unless it is imperative, don't include blocking operations inside a critical section. ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s07.html#1e30a213-82d6-4809-948e-831d6cc69116))


A elegant solution to this problem has been implemented, as the Initialization-on-demand holder idiom (https://en.wikipedia.org/wiki/Initialization-on-demand_holder_idiom). ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s07.html#9c007fb7-f5b8-4eae-99bf-142e2ada45cf))


A good example of such documentation can be found in the compute() method of the ConcurrentHashMap class. ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s07.html#e5357de8-27fe-4a97-bf73-169b70038dce))


Avoid executing inside the critical section the code you don't control. F ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s07.html#ae4ba0e8-ff2d-45d6-a42a-ff16740eb52b))


These variables are classes that support atomic operations on single variables. They include a method, denominated by compareAndSet(oldValue, newValue), that includes a mechanism to detect if assigning to the new value to the variable is done in one step. ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s07.html#21e7b0d7-ec46-404b-b20f-426e8d1b4582))


If only one of the tasks modifies the data and the rest of the tasks read it, you can use the volatile keyword without any synchronization or data inconsistency problem.  ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s07.html#13dcb92d-3e45-46c5-aeb2-fc57182bbae5))


Another option you have is to use something like ConcurrentHashMap<Thread, MyType> and use it like var.get(Thread.currentThread()) or var.put(Thread.currentThread(), newValue) ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s07.html#869482be-2bce-4332-a022-faa69c00ca61))


Get the information about the system dynamically (for example, in Java you can get it with the method Runtime.getRuntime().availableProcessors()) and make your algorithm use that information to calculate the number of tasks it's going to execute. ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s07.html#d20acccd-8793-4232-914a-89223ee6e517))

## The Java memory model



A memory model describes how individual tasks interact with each other through memory and when changes made by one task will be visible to another.  ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s06.html#adfbf4e2-a333-497f-92c2-f45a4a524e2c))

## Concurrency design patterns



This design pattern defines how to use global or static variables locally to tasks.  ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s05.html#575e8aed-26c8-45d6-b560-50d5233330a6))


In this circumstance, a lock provides poor performance because all the read operations can be made concurrently without any problem. ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s05.html#6dfed0d2-c288-4d5e-a339-363e7f1df4c4))

## Possible problems in concurrent applications



They are Coffman's conditions, which are as follows: ([link](https://learning.oreilly.com/library/view/-/9781785886126/ch01s02.html#08335a42-fa43-404e-9556-7e8aaf23da10))

[> Home](../README.md)