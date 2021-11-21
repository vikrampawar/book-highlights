# Building Microservices, 2nd Edition

[> Home](../README.md)
## 1. What Are Microservices?



In my experience, a distributed monolith has all the disadvantages of a distributed system, and the disadvantages of a single-process monolith, without having enough of the upsides of either. ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#321bce89-d8c4-4333-90d5-b566ab0fe50c))


Shopify is a great example of an organization that has used this technique as an alternative to microservice decomposition, and it seems to work really well for that company.6 ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#da90a857-5d6a-44cb-af81-b4bc1d4b7be3))


In such a situation, our Customer microservice encapsulates a thin slice of each of the three tiers—it has a bit of UI, a bit of application logic, and a bit of data storage ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#8c3f9537-9b2f-46c5-9c0b-d6e7dd9aa55b))


Chris Richardson, the author of Microservice Patterns (Manning Publications), once said—the goal of microservices is to have “as small an interface as possible.” That ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#61709bbe-2556-44ea-b82e-426740798063))


If a microservice wants to access data held by another microservice, it should go and ask that second microservice for the data.  ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#38952266-b72f-4ba0-beed-69674f56f813))


By making our services end-to-end slices of business functionality, we ensure that our architecture is arranged to make changes to business functionality as efficient as possible.  ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#e74b3085-7d1f-4f9b-b675-87bef5b4a583))


So you can also see the focus on independent deployability as a forcing function—by focusing on this as an outcome, you’ll achieve a number of ancillary benefits. ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#7941afe7-80d0-43c4-9ef8-126b6e84d266))


If you take only one thing from this book and from the concept of microservices in general, it should be this: ensure that you embrace the concept of independent deployability of your microservices ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#823d8e82-b21a-4745-a42b-5a964652ea1e))


Microservices embrace the concept of information hiding. ([link](https://learning.oreilly.com/library/view/-/9781492034018/ch01.html#acd9f238-6214-49c6-a6a7-fa86217e0c17))

[> Home](../README.md)