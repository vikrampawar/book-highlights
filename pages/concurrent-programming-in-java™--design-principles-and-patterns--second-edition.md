# Concurrent Programming in Java™: Design Principles and Patterns, Second Edition

[> Home](../README.md)
## 1. Concurrent Object-Oriented Programming



The techniques for ensuring safety described here rely on careful engineering practices (including several with roots in formalisms) rather than formal methods themselves. ([link](https://learning.oreilly.com/library/view/-/0201310090/ch01.html#3a15d374-b5bb-4e2d-9fa8-658b876c5e81))


But it is a standard engineering (not just software engineering) practice to place primary design emphasis on safety.  ([link](https://learning.oreilly.com/library/view/-/0201310090/ch01.html#f27d8663-d89e-4508-a4be-1fa5a6f87570))


Theoretical accounts of process calculi, event structures, linear logic, Petri nets, and temporal logic have potential relevance to the understanding of concurrent OO systems. For overviews of most approaches to the theory of concurrency, see: ([link](https://learning.oreilly.com/library/view/-/0201310090/ch01.html#34f947f5-f28b-4187-be58-097e826c595c))


This style of mapping can simulate each of the extremes. Purely passive sequential models can be programmed using only one thread. Purely active models can be programmed by creating as many threads as there are active objects, avoiding situations in which more than one thread can access a given passive representation (see § 2.3),  ([link](https://learning.oreilly.com/library/view/-/0201310090/ch01.html#b7c4dc89-cb9b-417c-a1f9-81cfcf0b441a))

[> Home](../README.md)