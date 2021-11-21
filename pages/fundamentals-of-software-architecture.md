# Fundamentals of Software Architecture

[> Home](../README.md)
## 7. Scope of Architecture Characteristics



Architects use the architecture quantum measure as a way to think about deployment, coupling, where data should reside, and communication styles within architectures. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch07.xhtml#fe5941eb-6954-4de7-adda-36264a1505fa))


Architects must remember that the analysis to yield architecture characteristics represents only a small part of the overall effort to design and implement an application—a lot of design work happens past this phase! During this part of architecture definition, architects look for requirements with structural impact not already covered by the domain. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch07.xhtml#4bbff3a8-e2ed-46e3-894d-e0711eafced1))


In modern systems, architects define architecture characteristics at the quantum level rather than system level. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch07.xhtml#dd50a9d9-d7e7-4886-9bf1-deb7fb626d81))


The bounded context concept recognizes that each entity works best within a localized context. Thus, instead of creating a unified Customer class across the entire organization, each problem domain can create its own and reconcile differences at integration points. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch07.xhtml#942f70c2-6d8a-4e76-bd5b-1b75aa8f0ed8))


Before DDD, developers sought holistic reuse across common entities within the organization. Yet creating common shared artifacts causes a host of problems, such as coupling, more difficult coordination, and increased complexity ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch07.xhtml#9d71a555-f395-4710-b319-332fed589791))


Architecture quantum
An independently deployable artifact with high functional cohesion and synchronous connascence ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch07.xhtml#568ff907-1916-4181-b7f6-7b2aea7227f9))

## 5. Identifying Architectural Characteristics



We could eliminate customizability as an architecture characteristic and plan to implement that behavior as part of application design. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch05.xhtml#2f690e14-b6d8-4d94-9e48-fece282527b1))


A useful exercise once the team has made a first pass at identifying the architecture characteristics is to try to determine the least important one—if you must eliminate one, which would it be ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch05.xhtml#3e13114d-17be-4e72-b107-b43c8483d296))


Architects must remember: there is no best design in architecture, only a least worst collection of trade-offs. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch05.xhtml#f212be9a-ea92-43c9-8815-01ad3c0e860b))


Architects shouldn’t stress too much about discovering the exactly correct set of architecture characteristics—developers can implement functionality in a variety of ways ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch05.xhtml#9bb285a2-4d2e-43c8-a594-2adaf69c03fa))


The architecture implies some structural component, whereas design resides within the architecture. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch05.xhtml#b45174cd-1f35-420d-9a93-fa901fc1c6fa))


his design element isn’t critical to the success of the application though. It is important to note that there are no correct answers in choosing architecture characteristics, only incorrect ones (or, as Mark notes in one of his well-known quotes):

There are no wrong answers in architecture, only expensive ones. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch05.xhtml#24c128b3-07e7-4247-b046-ea2dee68035a))


Often, elastic systems also need scalability: the ability to handle bursts and high numbers of concurrent users. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch05.xhtml#2faa3abf-7150-455c-8423-beede7f26ac3))


A common anti-pattern in architecture entails trying to design a generic architecture, one that supports all the architecture characteristics. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch05.xhtml#b2caa54c-0046-4277-8cd8-f8f81869ab33))

## 2. Architectural Thinking



Leveraging automation by creating simple command-line tools and analyzers to help the development team with their day-to-day tasks is another great way to maintain hands-on coding skills while making the development team more effective ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#f6155d05-2c8d-48f7-8ee3-bc2d7d2aa47c))


The second reason is that by writing production-quality proof-of-concept code, the architect gets practice writing quality, well-structured code rather than continually developing bad coding practices. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#ad80c07e-f529-4438-a103-9e48822e5a69))


The first way is to do frequent proof-of-concepts or POCs ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#30f1645c-84e8-4cd6-9f8c-41f49eab70b5))


The point here is that everything in software architecture has a trade-off: an advantage and disadvantage. Thinking like an architect is analyzing these trade-offs, then asking “which is more important: extensibility or security?” The decision between different solutions will always depend on the business drivers, environment, and a host of other factors. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#f29b2f41-ccc8-4da9-8031-133358a671ff))


n the queue option in Figure 2-9, each consumer can have its own contract specific to the data it needs ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#06d28efe-c485-40ce-8f48-dfd940de9a19))


In other words, it is very easy to wiretap into a topic, but not a queue ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#56e71133-5e65-4bd4-b946-fd29c520dacd))


Programmers know the benefits of everything and the trade-offs of nothing. Architects need to understand both ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#448a52be-b76f-47c8-b9c2-3f116cb8c5f9))


There are no right or wrong answers in architecture—only trade-offs. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#b2be60b9-f73a-4261-b807-6a9a3617d37d))


Unlike a developer, who must have a significant amount of technical depth to perform their job, a software architect must have a significant amount of technical breadth to think like an architect and see things with an architecture point of view ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch02.xhtml#3b150f10-a90a-4be8-bc30-95177867ba3e))

## 23. Negotiation and Leadership Skills



It’s really through collaboration with the development team that the architect is able to gain the respect of the team and form better solutions. The more developers respect an architect, the easier it will be for the architect to negotiate with those developers. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch23.xhtml#82df9bc8-7a0d-43bf-be37-3e53a1a0e8c1))


If a developer disagrees with a decision, have them arrive at the solution on their own. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch23.xhtml#9898e9e3-7ff5-456a-a803-73ecfeebbaea))


Notice here the architect is providing the justification for the demand that all requests need to go through the business layer of the application. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch23.xhtml#40055726-5ead-4272-87a3-096f482e2b50))


When convincing developers to adopt an architecture decision or to do a specific task, provide a justification rather than “dictating from on high.” ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch23.xhtml#c122d210-a92d-4b6a-99b5-301b9787740f))


Always remember that demonstration defeats discussion. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch23.xhtml#87e7e1f6-b307-4e7d-9faf-a9ebd1d299f9))

## 14. Event-Driven Architecture Style



Another inherent difference between the broker and mediator topology is how the processing events differ in terms of their meaning and how they are used. In the broker topology example in the previous section, the processing events were published as events that had occurred in the system (such as order-created, payment-applied, and email-sent). The event processors took some action, and other event processors react to that action. However, in the mediator topology, processing occurrences such as place-order, send-email, and fulfill-order are commands (things that need to happen) as opposed to events (things that have already happened). Also, in the mediator topology, a command must be processed, whereas an event can be ignored in the broker topology. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#dbc4978e-498a-404d-b25e-a797e93e55c5))


Because the mediator controls the workflow, it can maintain event state and manage error handling, recoverability, and restart capabilities. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#7d8941cc-5366-49f7-a76a-8e627335b2c3))


he simple mediator can then interrogate the classification of the event, and based on that classification, handle the event itself or forward it to another, more complex, event mediator ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#c9611298-80b3-4a05-8da1-9a28581764be))


It is important to know the types of events that will be processed through the mediator in order to make the correct choice for the implementation of the event mediator. Choosing Apache Camel for complex and long-running events involving human interaction would be extremely difficult to write and maintain. By the same token, using a BPM engine for simple event flows would take months of wasted effort when the same thing could be accomplished in Apache Camel in a matter of days. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#d958d0d8-c387-45b4-87bb-04b73547095a))


Central to this topology is an event mediator, which manages and controls the workflow for initiating events that require the coordination of multiple event processors. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#b2a6cd90-67cc-45af-97b7-786d6a92325e))


The topics provide the back pressure point if an event processor comes down or slows down due to some environment issue. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#abc8973c-ac55-4ef2-8cc7-c396444fff0a))


Vikram: [Probably means that messsages are queued up]


The event broker component is usually federated (meaning multiple domain-based clustered instances), where each federated broker contains all of the event channels used within the event flow for that particular domain. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#4ea418d5-7526-42c5-b68d-86b243134a40))


Vikram: [This probably means that a queue manager has all of the queues for a particular domain]


The broker topology differs from the mediator topology in that there is no central event mediator. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#47552be0-b050-4422-a3d7-2d3544ba7b25))


An event-based model, on the other hand, reacts to a particular situation and takes action based on that event. An example of an event-based model is submitting a bid for a particular item within an online auction. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#d40b0421-f95e-4dff-81c8-634d59b60122))


A good example of the request-based model is a request from a customer to retrieve their order history for the past six months. Retrieving order history information is a data-driven, deterministic request made to the system for data within a specific context, not an event happening that the system must react to. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch14.xhtml#f460a57a-2b8e-4dc2-a896-03c83f153069))

## 8. Component-Based Thinking



However, the fundamental decision rests on how many quanta the architecture discovers during the design process. If the system can manage with a single quantum (in other words, one set of architecture characteristics), then a monolith architecture offers many advantages. On the other hand, differing architecture characteristics for components, as illustrated in the GGG component analysis, requires a distributed architecture to accommodate differing architecture characteristics ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#ad03aa08-86c0-4b77-8615-82c8596523d9))


Rather, try to objectively assess the trade-offs between different design decisions, and choose the one that has the least worst set of trade-offs. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#f34ddbdb-266d-4563-b4ed-9ba7f42a0950))


As an architect, don’t obsess over finding the one true design, because many will suffice (and less likely overengineered ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#4c6131d4-8f82-4d0b-a461-e6ca694b6637))


The entity trap anti-pattern arises when an architect incorrectly identifies the database relationships as workflows in the application, a correspondence that rarely manifests in the real world ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#bdb69744-c6b8-4330-84a5-585122b274e6))


No accepted “correct” way exists to design components ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#26dc5f07-e04a-4fe0-9d73-119b59245928))


This mapping doesn’t have to be exact—the architect is attempting to find a good coarse-grained substrate to allow further design and refinement by architects, tech leads, and/or developers ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#28ee27ef-a90d-4ace-817b-be8fb437218f))


Outside that, an architect has the freedom to make up whatever components they want, then map domain functionality to them to see where behavior should reside ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#1a648d10-13ca-4b8a-a1d4-678b6390a735))


In a modular monolith, the architect partitions the architecture around domains or workflows rather than technical capabilities ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#0dd657be-a93e-4b87-ad5b-0170a7349729))


The other is an architecture style popularized by Simon Brown called a modular monolith, a single deployment unit associated with a database and partitioned around domains rather than technical capabilities ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#af0e148d-6547-4870-b5b8-839d3ad475b9))


An architect must identify components as one of the first tasks on a new project ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#413d4227-ed66-4ab8-b9e8-e06d60c2f494))


Virtually all the details we cover in this book exist independently from whatever software development process teams use: architecture is independent from the development process ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#8ea7b3e8-87cc-475e-a979-f3713191f5e5))


However, architects typically think in terms of components, the physical manifestation of a module. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch08.xhtml#cb23d19c-ccf3-43ed-8a59-1decb7746871))

## 18. Choosing the Appropriate Architecture Style



For example, architects seriously rethought the implications of code reuse after building architectures that featured it and then realizing the negative trade-offs. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch18.xhtml#6a0b48e6-6e93-4e44-bef8-322580d3d7f0))

## 4. Architecture Characteristics Defined



However, they differ because interoperability implies ease of integration with other systems, which in turn implies published, documented APIs. Compatibility, on the other hand, is more concerned with industry and domain standards. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch04.xhtml#39fec2f4-98e5-4300-974e-2f37b647d7b8))


Support for each architecture characteristic adds complexity to the design. Thus, a critical job for architects lies in choosing the fewest architecture characteristics rather than the most possible. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch04.xhtml#1b2c5c48-5bb3-464c-b395-f94164b85810))


We prefer architecture characteristics because it describes concerns critical to the success of the architecture, and therefore the system as a whole, without discounting its importance. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch04.xhtml#aecded7e-da70-4b4d-91fd-0368a95a0f29))


Vikram: [Other terms are 'Non-functional requirements', 'Quality attributes']

## 21. Diagramming and Presenting Architecture



ArchiMate is a technical standard from The Open Group, and it offers a lighter-weight modeling language for enterprise ecosystems. The goal of ArchiMate is to be “as small as possible,” not to cover every edge case scenario. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch21.xhtml#bed34bdb-8461-4dbd-bb63-9b9d23c975e2))


C4 is best suited for monolithic architectures where the container and component relationships may differ, and it’s less suited to distributed architectures, such as microservices. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch21.xhtml#bd81e84d-3912-446d-884e-7d12edcdbd84))


C4 is a diagramming technique developed by Simon Brown to address deficiencies in UML and modernize its approach. The four C’s in C4 are as follows: ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch21.xhtml#ff8f5ed4-b0ec-4863-b9fd-94c5b8e04749))

## 3. Modularity



Yet, with all the writing and thinking about components and separation, developers and architects still struggle with achieving good outcomes ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch03.xhtml#ea581244-87e0-4c7f-99ac-6c8542cd0d07))


Cohesion refers to what extent the parts of a module should be contained within the same module ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch03.xhtml#f47ee55e-06be-4bb4-8d36-672ca7012083))


Fortunately, researchers created a variety of language-agnostic metrics to help architects understand modularity. We focus on three key concepts: cohesion, coupling, and connascence ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch03.xhtml#c56f99bc-bd67-48b7-a464-c12ca63e0430))

## 13. Service-Based Architecture Style



The basic topology of service-based architecture follows a distributed macro layered structure consisting of a separately deployed user interface, separately deployed remote coarse-grained services, and a monolithic database. ([link](https://learning.oreilly.com/library/view/-/9781492043447/ch13.xhtml#2c34ac46-b8fa-4717-a795-7ffc9c2a6df3))

[> Home](../README.md)