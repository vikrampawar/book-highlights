# Reactive Programming with RxJava

[> Home](../README.md)
## Foreword



Even though the details of RxJava are slightly different that that of other Rx implementations, it is still built specially for all you developers that need to survive in the brave new world of distributed real-time data processing and focus on essential complexity without accidental complexity that suck the life out of you.  ([link](https://learning.oreilly.com/library/view/-/9781491931646/foreword01.html#27c91e08-4b02-4fea-a1fb-671b4b5a0ecf))


Since Java does not have language support for async await, the community extended the Observer and Observable types with the concept of reactive pull and introduced the Producer interface. ([link](https://learning.oreilly.com/library/view/-/9781491931646/foreword01.html#d7b57512-c660-415d-ad5e-b35d5c626caa))


Fast forward to 2016 and the popularity and use of Rx has skyrocketed. All traffic through the Netflix API relies upon RxJava, as does the Hystrix fault-tolerance library that bulkheads all internal service traffic, and via related reactive libraries RxNetty and Mantis, Netflix is now creating a completely reactive network stack for connecting all internal services across machine and process boundaries ([link](https://learning.oreilly.com/library/view/-/9781491931646/foreword01.html#df360a8e-6230-4071-a913-651da00f868c))


After many false starts it finally dawned on us that by dualizing the Iterable/Iterator interface for synchronous collections, we could obtain a pair of interfaces to represent asynchronous event streams, with all the familiar sequence operators such as map, filter, scan, zip, groupBy, etc. for transforming and combining asynchronous data streams, and thus Rx was born somewhere in the summer of 2007. ([link](https://learning.oreilly.com/library/view/-/9781491931646/foreword01.html#cb03289c-fb3b-40d5-8084-eadca62cfe28))

## 1. Reactive Programming with RxJava



Hence this is where the tagline for Reactive Extensions (Rx) in general and RxJava specifically comes from, “a library for composing asynchronous and event-based programs.” RxJava is a concrete implementation of reactive programming principles influenced by functional and data-flow programming. ([link](https://learning.oreilly.com/library/view/-/9781491931646/ch01.html#daba1122-188d-418b-bad1-30e27f3a38bd))


you need to combine events (or asynchronous responses from functions or network calls), have conditional logic interacting between them, and must handle failure scenarios and resource cleanup on any and all of them. This is where the reactive-imperative approach begins to dramatically increase in complexity and reactive-functional programming begins to shine ([link](https://learning.oreilly.com/library/view/-/9781491931646/ch01.html#e17eca08-90e9-4c96-84b6-38e5cf8617d8))


Now, if the code in question is handling only one event stream, reactive-imperative programming with a callback is going to be fine, ([link](https://learning.oreilly.com/library/view/-/9781491931646/ch01.html#282f45fe-09dc-412b-8a25-e1ce1f8ba8d9))


So, the short answer to what reactive-functional programming is solving is concurrency and parallelism. More colloquially, it is solving callback hell, which results from addressing reactive and asynchronous use cases in an imperative way. ([link](https://learning.oreilly.com/library/view/-/9781491931646/ch01.html#b26b32ae-1fa3-4d97-bacd-1ecf2db08c25))


Reactive-functional programming therefore is an approach to programming—an abstraction on top of imperative systems—that allows us to program asynchronous and event-driven use cases without having to think like the computer itself and imperatively define the complex interactions of state, particularly across thread and network boundaries. ([link](https://learning.oreilly.com/library/view/-/9781491931646/ch01.html#322890d5-ee22-487d-b8fe-d4507626a8a3))

## Introduction



Note from Tomasz Nurkiewicz
I first came across RxJava around 2013 while working for a financial institution. We were dealing with large streams of market data processed in real-time. By then, the data pipeline consisted of Kafka delivering messages, Akka processing trades, Clojure transforming data, and a custom-built language for propagating changes throughout the system. RxJava was a very compelling choice because it had a uniform API that worked very well for different sources of data. ([link](https://learning.oreilly.com/library/view/-/9781491931646/preface01.html#7dfc748a-2d1e-4af8-a13e-ebb26ce27504))

[> Home](../README.md)