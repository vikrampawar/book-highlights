# Reactive Messaging Patterns with the Actor Model: Applications and Integration in Scala and Akka

[> Home](../README.md)
## Foreword



When Carl Hewitt invented the Actor model in the early 1970s he was way ahead of his time.  ([link](https://learning.oreilly.com/library/view/-/9780133846904/pref01.html#c38e0d2a-70f1-4df0-9b96-6b4a3daa5eec))

## Chapter 1. Discovering the Actor Model and the Enterprise, All Over Again



The main focus of the design is to be explicit with your software models, because that’s what makes it possible to understand a complex system. ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#249b75c0-fa49-4e8d-9de7-0cd083cd3c08))


What is more, event-driven, reactive applications are inherently nondeterministic.  ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#6eb5d945-0d98-4ea7-b4db-af04863d49f0))


Considering state transitions, as an actor handles each newly received message, it has the opportunity to prepare its behavior for future messages. In simple terms, an actor does this by exchanging its current receive function for a different one.  ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#59c4db33-1989-4b9f-8b66-205393bf322a))


The actor with a pending state transition must reply to any senders whose messages would overflow its pending work capacity with some kind of “sorry, but you’ll have to try again later” message ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#90597e6e-63ef-41ed-b424-b5703930b782))


According to Amdahl’s law, the speedup of a program using multiple processors in parallel computing is limited by the time needed for the sequential fraction of the program.  ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#f3219b43-64fc-4429-8ec4-3082cf0ab293))


All this enables an actor system to support high-performance, high-throughput, and low-latency operations ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#e210795d-8c11-4a2b-a55f-7ac94e93799d))


By becoming another kind of message handler, the actor implements a finite state machine. ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#6303ab47-9fc2-4bcf-96f0-34f645c91b4d))


In other words, you can solve any given problem by creating yet another actor.

Origin of Actors ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#d3c11b27-5b8e-4214-82e1-6b6c2978a2e5))


Actors are a more powerful computational agent than sequential processes or value transforming functional systems” [Agha, Gul].  ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#31cae30f-22da-4a5a-81fa-6f5ed8c2ecfd))


Years before this statement, Alan Kay commented on messaging between components as “the big idea” that should be the focus, rather than the properties of objects and their internal behavior  ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#34836a33-0c46-4929-9fba-a2efe252538e))


Perhaps you are at the inception of a strategic enterprise project. Compared to what you have previously been able to achieve with “normal” enterprise development tools, your strategic application may have to perform and scale off the charts. You are considering the Actor model to help you attain the inflexible and otherwise unreachable requirements. Beyond performance and scalability demands, you need to produce a software model that reflects the mental model of the business visionaries.  ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#60d9ec77-a6cd-4057-9e7e-1072c390fe7b))


Within each of the general areas across various industries listed earlier, and many others, there will be visions of yet-to-be-realized, company-defining enterprise applications ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#12e30da3-37ad-4b61-8059-da18d7d8ae20))


One of the worst mistakes that a business can make is to try to shoehorn a packaged application into the position of strategic solution. ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#7f415bbf-6e1e-46b4-9e1c-63f0dfa6946f))


In fact, reactive components are given no system-level assurance of the order in which any message may be received. ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#4a4f0a00-2e04-426e-92c7-fc0719fecb0d))


Both the message-driven nature of reactive components and their location transparency lend to scaling applications on demand, that is, elasticity. ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#ee225ec9-1bb7-4164-ab1a-ca71be061553))


In other words, reactive applications enjoy the benefit that their components have location transparency. ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#af9c6f2b-9a49-496d-b689-c786fdce2c09))


. This can be supported by elasticity, which is scale on demand, which is reactive at the core. ([link](https://learning.oreilly.com/library/view/-/9780133846904/ch01.html#45ef176b-73ec-4ee0-9a44-bbc698af6783))

## Preface



When using the Actor model, many of the patterns will be employed in greenfield applications, not just for integration. That is because the patterns are first and foremost messaging patterns, not just integration patterns, and the Actor model is messaging through and through. ([link](https://learning.oreilly.com/library/view/-/9780133846904/pref02.html#3ce54ab5-b23a-47d1-8251-9627d3ad8375))

[> Home](../README.md)