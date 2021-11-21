# Domain-Driven Design Distilled

[> Home](../README.md)
## About the Author



Vaughn specializes in consulting around Domain-Driven Design and DDD using the Actor model with Scala and Akka. ([link](https://learning.oreilly.com/library/view/-/9780134434964/pref03.html#ff6177b5-b8dd-43a0-b2a6-d767306e2530))


He is the author of the best-selling books Implementing Domain-Driven Design and Reactive Messaging Patterns with the Actor Model, also published by Addison-Wesley.  ([link](https://learning.oreilly.com/library/view/-/9780134434964/pref03.html#60b5afc1-667a-4d83-8623-794208b8d691))

## Chapter 1. DDD for Me



Using Domain Events will help you both to model explicitly and to share what has occurred within your model with the systems that need to know about it. The ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#2113f22d-fdc0-4121-ac97-68b37ba3f062))


Tactical design is like using a thin brush to paint the fine details of your domain model. One of the more important tools is used to aggregate entities and value objects together into a right-sized cluster. It’s the Aggregate pattern. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#75bf4aef-3b06-4268-bd0a-f1e92bc827f7))


You will also see how to integrate multiple Bounded Contexts using a technique called Context Mapping.  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#b279246f-ed46-424e-a659-4128d2f5c8f2))


First you will learn how to segregate your domain models using the strategic design pattern called Bounded Contexts. Hand in glove, you will see how to develop a Ubiquitous Language as your domain model within an explicitly Bounded Context. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#434b0a3e-e48e-44f3-885e-8f9033e03561))


Strategic design is used like broad brushstrokes prior to getting into the details of implementation. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#0fcd9b9a-9460-47c1-b64b-1ae209153519))


Most people make the mistake of thinking design is what it looks like. People think it’s this veneer—that the designers are handed this box and told, “Make it look good!” That’s not what we think design is. It’s not just what it looks like and feels like. Design is how it works.

—Steve Jobs ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#9e34f2a6-b3df-414d-b8b1-f057e692377a))


In Scrum, knowledge acquisition is done through experimentation and collaborative learning and is referred to as “buying information” [Essential Scrum].  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#f17ef965-9041-4f07-bec8-82a34d669c42))


One model employed minimal, base intellect. The other model exploited maximum cognition. Software can be modeled from either perspective ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#766987af-1e71-47bc-9480-3a3b4145fdff))


These makeshift thoroughfares aren’t traveled today because they were well designed, but because they exist ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#e5082a5f-b2a5-48e0-9a92-4453bfe85a7e))


—Book Design: A Practical Introduction by Douglas Martin ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#63151c54-7789-4ffb-addf-07ed4aa9390e))


Questions about whether design is necessary or affordable are quite beside the point: design is inevitable. The alternative to good design is bad design, not no design at all. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#3d065d31-13c2-4a10-8bfa-beb55e3e5026))


This all seems to happen in the spirit of “no design yields lower-cost software.”  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#f460c8d0-38c5-4ba4-ab74-c253f6663764))


Developers are too wrapped up with technology and trying to solve problems using technology rather than careful thought and design.  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch01.html#141e279f-2f6c-4850-96f3-69e947e46f1a))

## Chapter 2. Strategic Design with Bounded Contexts and the Ubiquitous Language



The policy in each of these business areas exists for different reasons. There is no escaping this fact, and no amount of mental gymnastics changes this. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#1e28252f-a2a2-4414-a2cd-c18d9ac072e9))


Thus, a Big Ball of Mud is often the result of unbridled effort made by a team of software developers who don’t listen to the business experts. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#3eca8288-96c7-491c-b186-9637a08eaee1))


To understand one big reason to use Bounded Contexts, let’s consider a common problem with software designs. Often teams don’t know when to stop piling more and more concepts into their domain models ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#efed841a-4d83-4832-a809-17bba4b509aa))


It is especially important to be clear that one team works on a single Bounded Context ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#b8932f03-27b6-4d2e-a3ec-45c0d896bf5f))


This is the primary value proposition of DDD, and you want to invest appropriately by committing your best resources to a Core Domain. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#01f8633b-62ce-472e-b378-151deeef2215))


A Core Domain is developed to distinguish your organization competitively from all others ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#1d10d681-89c9-491c-b63e-1a5beb2643db))


In short, DDD is primarily about modeling a Ubiquitous Language in an explicitly Bounded Context ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#64c71e42-debe-4c8a-b3c4-23175d5403ce))


. In the end the code is the model and the model is the code ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#db3ed426-a9c9-4ff7-be64-883b68929052))


Both developers and Domain Experts should reject any tendency to allow documents to rule over conversation ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#0936651f-896f-46ad-94b2-6e948b63577c))


Still, you are using DDD because the business model is more complex than the technical aspects of the project. That’s why the developers have to dig into the business model with Domain Experts! ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch02.html#0811e544-f0ad-4465-a5c8-55e3e7bebf1c))

## Chapter 4. Strategic Design with Context Mapping



This generally means that if the events are published as JSON, or perhaps a more economical object format, the consumer should consume the events by parsing them to obtain their data attributes. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#897ea5fe-7fce-4641-ab14-f95da0e5d660))


Going Asynchronous with REST

It’s possible to accomplish asynchronous messaging using REST-based polling of a sequentially growing set of resources ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#bc77dae7-d245-4261-ad08-945e7b515bf5))


Using messaging is one of the most robust forms of integration because you remove much of the temporal coupling associated with blocking forms such as RPC and REST.  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#2859a4e2-79df-4ed8-ae6f-1d9f57442de2))


The book REST in Practice [RiP] is a good place to start. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#06747057-a4a8-479c-8d0a-da990abbac24))


An Open Host Service defines a protocol or interface that gives access to your Bounded Context as a set of services. T ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#9bcc9ab3-937b-4fe6-9ef8-5a9c592fbf1e))


An Anticorruption Layer is the most defensive Context Mapping relationship, where the downstream team creates a translation layer between its Ubiquitous Language (model) and the Ubiquitous Language (model) that is upstream to it. The layer isolates the downstream model from the upstream model and translates between the two. Thus, this is also an approach to integration. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#19ba0a9e-ba37-470b-a5ac-ccc64552e136))


A team will often become a Conformist, for example, when integrating with a very large and complex model that is well established. Example: Consider the need to conform to the Amazon.com model when integrating as one of Amazon’s affiliate sellers. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#4caf42a5-b189-4ea9-be32-55c277a42ca7))


A Customer-Supplier describes a relationship between two Bounded Contexts and respective teams, where the Supplier is upstream (the U in the diagram) and the Customer is downstream (the D in the diagram).  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#fd48b874-d72d-4006-b6df-bea818d559e3))


A Shared Kernel, depicted on page 54 by the intersection of the two Bounded Contexts, describes the relationship between two (or more) teams that share a small but common model. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#6d52543c-665f-4742-9f86-93023c678e33))


Considering that in two different Bounded Contexts there are two Ubiquitous Languages, this line represents the translation that exists between the two languages. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#f11f0b66-8ec4-45f9-950f-5c3427425fb1))


 Each team is responsible for one Bounded Context. They create a Partnership to align the two teams with a dependent set of goals ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#f0d24017-523d-4c6b-bc1f-8f5f0482504e))


When we talk about Context Mapping, what is of interest to us is what kind of inter-team relationship and integration is represented by the line between any two Bounded Contexts.  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#7257b90b-9a54-4d00-bd55-1b65343e96ce))


You also learned that the Agile Project Management Core Domain would have to integrate with other Bounded Contexts. That integration is known in DDD as Context Mapping ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch04.html#a96604d4-1cb6-4ac8-9373-ec7c39540eba))

## Chapter 5. Tactical Design with Aggregates



Even so, it is only the business that can determine the acceptable time frame for updates to occur between various Entities. Some are immediate, or transactional, which means they must be managed by the same Aggregate. Some are eventual, which means they may be managed through Domain Events and messaging, for example ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#603db2d2-b28b-4c8f-b1d1-b5af45a5d67f))


Some are immediate, or transactional, which means they must be managed by the same Aggregate. Some are eventual, which means they may be managed through Domain Events and messaging, for example. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#b087c8a6-3fbf-4ef4-a7e7-ac39f6aa8864))


This exercise indicates that eventual consistency is business driven, not technically driven. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#d9ba833e-6abf-424f-8703-266159586352))


Don’t get taken in by this alluring, highly abstract implementation trap. Model the Ubiquitous Language explicitly according to the mental model of the Domain Experts that is refined by your team ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#7d82d597-f39f-4932-8cc1-f5dd4aaf1afc))


When using functional programming, the rules change considerably. While an Anemic Domain Model is a bad idea when using object-oriented programming, it is somewhat the norm when applying functional programming.  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#ddf44c57-9d99-4a39-8439-21f3b965d19b))


Place your business logic in your domain model, or suffer bugs sponsored by an Anemic Domain Model. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#50aba38b-ad0f-46bc-ade0-f3e32bee0dac))


One big, nasty hook is the Anemic Domain Model [IDDD]. This is where you are using an object-oriented domain model, and all of your Aggregates have only public accessors (getters and setters) but no real business behavior.  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#b28cb533-0f24-4f71-9446-bb2bdbecd619))


Each Aggregate forms a transactional consistency boundary. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#7dd462f9-f5fc-42ef-b85d-f25b968d9a57))


The name of the Root Entity is the Aggregate’s conceptual name. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#17bfad4e-1af7-4aa3-b1c4-5806cea9fce5))


Each Aggregate is composed of one or more Entities, where one Entity is called the Aggregate Root. Aggregates may also have Value Objects composed on them.  ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#87c65b99-fa40-4ce4-b770-8bb3a0f62542))


The main thing that separates an Entity from other modeling tools is its uniqueness—its individuality. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#79a1a1ac-ba05-4332-870d-c4571c46916e))


The interested Bounded Context can be the same one from which the Domain Event was published, or it could be different Bounded Contexts. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#0ee76110-0e98-411b-991f-e42a4ab54d56))


As part of the BacklogItem Aggregate’s transaction, it publishes a Domain Event named BacklogItemCommitted. The BacklogItem transaction completes and its state is persisted along with the Backlog-ItemCommitted Domain Event. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#ce151c69-39ab-4f69-b661-21e9e0bbcac5))


Another benefit to using reference by identity only is that your Aggregates can be easily stored in just about any kind of persistence mechanism, such as relational database, document database, key-value store, and data grids/fabrics. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#53967129-8575-4faa-8d66-fc476cc05f6c))


Perhaps most importantly, these Aggregates will have transactional success much more frequently than the previous large-cluster Product Aggregate. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#a8195503-6b62-44bf-a8db-46923114abc0))


Rule 1 means that the business should ultimately determine Aggregate compositions based on what must be consistent when a transaction is committed. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#8522df18-df29-4716-bd0a-88504c2b3cc0))


Let’s next consider the four basic rules of Aggregate design:

1. Protect business invariants inside Aggregate boundaries.

2. Design small Aggregates.

3. Reference other Aggregates by identity only.

4. Update other Aggregates using eventual consistency. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch05.html#fbcc3cd8-d8cc-4441-889e-7f652d05ce36))

## Chapter 6. Tactical Design with Domain Events



A Domain Event is a record of some business-significant occurrence in a Bounded Context. ([link](https://learning.oreilly.com/library/view/-/9780134434964/ch06.html#14a8987a-6401-477a-a1b6-465f8e79594f))

[> Home](../README.md)