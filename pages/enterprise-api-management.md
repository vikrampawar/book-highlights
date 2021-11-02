# Enterprise API Management

[> Home](../README.md)
## Common denominators



A term that is becoming increasingly popular when referring to this specific type of gateways is API microgateways. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/69f86932-1f46-4975-a731-d9cb98f192d2.xhtml#9a6a1a9b-fab8-49d8-8fe5-4a7278301176))


A service endpoint(s), managed through an API platform is referred to as a managed API.
Therefore, a service endpoint that is not managed through an API platform is an unmanaged API.
To avoid confusion, this book refers to managed APIs as simply APIs ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/69f86932-1f46-4975-a731-d9cb98f192d2.xhtml#1bc302db-fe4e-43b0-95b1-7e0c6d0273f9))


The tendency of integration middleware to become bigger and bigger seems to be reversing, almost like a big bubble that bursts into many smaller ones. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/69f86932-1f46-4975-a731-d9cb98f192d2.xhtml#ebb5c147-40c1-42b0-b86e-f0a085a56e10))

## The API value chain



There is another well-known and publicly available API maturity model, known as the Richardson Maturity Model. However ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/1d967053-35e6-4605-806f-635ad0b11361.xhtml#4f66455a-ae04-48ea-91b5-fed29afcc6c6))

## API load balancing



Instead, this capability refers to the ability of an API gateway to also act as a client-based load balancer, thus removing the need for a load balancer in between ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/e02b7b41-45c0-49cd-b92f-e775deb86c88.xhtml#d1ef5c14-be40-463a-a006-1ceea4587aa3))

## Redaction



Redaction refers to having the ability of removing, masking, and/or limiting the presence of fields within request/response payloads and/or headers ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/737629cf-280b-4a2a-8025-551f3865f7e2.xhtml#8cf98d6d-97aa-45ef-b36e-641c4598c85b))

## Avoiding a hyperconnectivity mess



API management differs from related disciplines, most notably SOA governance, in that it is much more lightweight and a lot more focused on making the lives of the API consumers (developers) easier, by providing the right tools for the design and run aspects of APIs, and making processes simple to follow ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/188dfb16-5f8d-4b8b-8b7a-8bf2fc67e759.xhtml#6c08bbfc-c559-4c6a-ba97-f040e13ed83b))


A hyperconnectivity mess occurs as a result of APIs being used in an ad hoc manner and without proper governance.  ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/188dfb16-5f8d-4b8b-8b7a-8bf2fc67e759.xhtml#e99d2692-6abc-4b2b-a48e-aebfc5b985f2))

## API monetization and billing



A better and more commonly accepted definition is that API monetization refers to having the ability to drive revenue through the use of APIs ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/3382e422-9527-4fb7-9232-5b4cab26a838.xhtml#4feed0d5-963b-4716-a709-5ea63f7f04d2))

## APIs as a driving force for many large acquisitions in the software industry



integration market is shifting and that more traditional integration capabilities (traditionally based on large-footprint integration middleware backboxes) are being superseded by API-led architectures ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/770bbb3e-a676-4ec3-a355-ee8e930c29b2.xhtml#4a058894-1027-4be5-a702-fc50e4f2c901))

## API composition



API composition differs from orchestration in that there is no (or should not be any) business logic implemented in the composition, for example, if/then/switch conditionals, for/while loops, or complex data transformations ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/dde7f300-3406-4bd2-b955-a6f8114c36e0.xhtml#2fd8d2e2-2b9d-4c48-b250-8f2d9b0a183b))

## API resource routing



Implementing an API gateway as the only entry point to all services means that API consumers only have to be aware of one URL domain. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/5f93b473-e366-4094-9530-0ff5ed5b3755.xhtml#e401e07b-cb0e-4294-bae4-6723506918f4))


Vikram: [One endpoint
]

## Push notification



The most common way to implement this capability is via Webhooks. Webhooks enable API consumers to subscribe to specific API events, for example, changes in data for a specific resource, and during the subscription process (which is typically just an API POST request), API consumers provide a call-back URL that is subsequently used by the server to push the events. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/6d15ddc2-511a-4ff9-9d1d-9871e75e9b0c.xhtml#2f3b6793-cd1b-4922-b43d-478f7a0e7a3f))

## Who this book is for



Business-led API strategies
API-led architectures and patterns
API architectural styles to use (for example, REST, GraphQL, or gRPC)
The full API life cycle, including related cycles such as the service and API consumer cycles
Target operating models suitable for API products.
Lastly, as the book is technology-agnostic and doesn't offer strong views on tools, it can also be used as a reference to compare different products, whether they are commercial or open-sourced. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/a939f9eb-5d97-4a1c-a52c-ea9e58196bc1.xhtml#c9a2afe1-3e0c-412e-9c05-b5541b0d2e61))

## Event Hub



Apache Kafka, originally developed by LinkedIn and now also open sourced, is by far the most popular technology used to implement an Event Hub. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/97fa22ac-5cad-4f0d-b257-884b61c1c42a.xhtml#cd7a9baf-e0b7-456f-8338-8e74332a21e1))


This capability is typically used, for example, when implementing a Change Data Capture pattern, whereby it is possible to detect and propagate to multiple target changes in a source database ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/97fa22ac-5cad-4f0d-b257-884b61c1c42a.xhtml#d19686f5-ac81-44d7-94c2-d19e41cf4dea))

## Policy definition and implementation



For example, policies can be applied to protect against common security threats, to implement authentication and authorization, to route and load balance incoming calls to multiple backend services, and even to enforce monetization plans. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/a5060a7d-0283-48e6-8a84-bb663a6b5ab0.xhtml#5c026063-92dd-4ca0-9f0a-5b18e4def1a5))

## Preface



The emergence of APIs as the means to enable digital ecosystems has created an economy of its own, an API economy, which has a more fundamental impact on how businesses organize their teams. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/288f1743-6834-40bb-9806-4f0095a2c16e.xhtml#c95924c7-82e5-4a98-8ec2-d953ff928415))


In fact, a study conducted by Mckinsey predicts that by 2025, digital ecosystems will account for 30% of global revenues, which according to the firm is about 60 trillion US dollars ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/288f1743-6834-40bb-9806-4f0095a2c16e.xhtml#128a4e57-da07-435e-9e36-c4ca93b6e93d))


To summarize, API management must be as much about providing the means to discover and use public APIs as it is about implementing new ones. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/288f1743-6834-40bb-9806-4f0095a2c16e.xhtml#662796f6-b2cf-4122-b62e-fc6cbb2bf1d1))

## Generation zero



During this period, if a web service had to be accessed from outside the internal networks, typically web proxies would be implemented in Demilitarized Zones (DMZs), to proxy the HTTP traffic to the ESB, and also implement transport security (HTTPS) ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/782e5307-c695-4cba-8ef8-a250392afc9a.xhtml#7c33f257-fddd-4659-92e0-e4be1bca14d0))

## Service registry



For example, Apache Kafka uses Apache Zookeeper as its internal registry. Kubernetes makes use of ETCD as its internal registry. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/62deb947-bb78-4d8a-ad1a-4cf2710ecdc5.xhtml#269f5e20-a868-4a23-9efa-403e8871b1a4))


a registry can be used by a service to obtain configuration metadata during startup and to register its runtime metadata (for example, HTTP endpoints) once it is up and running. The registry can also be used by other infrastructure components (for example, API gateways or a service mesh) to dynamically determine the status of a service and dynamically route requests to active and healthy service endpoints ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/62deb947-bb78-4d8a-ad1a-4cf2710ecdc5.xhtml#7e82cfae-5fae-4037-abf6-7b39ba6d2525))

## Service mesh



popular choice for implementing a service mesh in Kubernetes infrastructures is Istio.io. Another popular choice for a Java-based service mesh is Hystrix, which was originally developed by Netflix but also open sourced. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/8e61cb3e-b6ec-4a56-ac2f-4c79044d9ecf.xhtml#5a543646-98d8-4131-b699-e918024a73c9))

## Conceptual architecture view



From an API exposure perspective, this block aids authentication and authorization policies by, for example, enabling tokens (for example, OAuth 2.0, OpenID, and/or even Security Assertion Markup Language (SAML)) to be generated and enforced at runtime. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/8e452d3d-17a2-43f7-baf6-9746600c9357.xhtml#bbc5e0ec-e488-40e5-852d-00dfec3e2df0))

## Polyglot programming



use of microservices frameworks as aids. For example, Spring Boot in the case of Java, Node.js/Express in the case of server-side JavaScript, and Flask in the case of Python. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/87fb08fc-a143-46e6-a924-1fef765b2b85.xhtml#38f1cfcb-193b-481f-bf46-7a58605f5ed4))

## Application Services Governance



These communities did not just put into question the use of traditional (monolithic) SOA stacks (for example, ESBs) but, broadly speaking, also regarded their use as a bad practice ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/3f811df6-48dc-4f69-b77c-0144fdc3dbb7.xhtml#da7b40b7-a4e3-405f-9f9b-a15b89cbf177))

## Choreography



Instead, all interactions are event-driven and asynchronous, and this capability is typically supported with the use of an Event Hub as the core infrastructure where events are published and consumed from. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/5898fbd6-13f2-48ce-a746-53284c01eca5.xhtml#7618c07c-c215-4d7e-89f0-463a9dc2de72))

## API exposure



An API gateway is a runtime component that handles incoming requests, which are then mediated (also known as routed) to the individual services that are responsible for delivering the business capability that a consuming application is after ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/8d92c0a6-5c09-445b-bc1d-f5b80583d506.xhtml#2c16c661-b440-4cc4-8f4d-86096e81c95d))

## Architecting API-led



 A robust architecture must always be reflective of a solid understanding of the business domain in question and the capabilities required in order address it ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/a5ce6e1e-bde6-42d0-a25e-d809e5aee1e0.xhtml#cec5a020-b57d-43fd-ae0e-dc27766bb569))


A common term used to refer to these types of (single-purpose) APIs is Experience APIs, mainly because of their role in enabling applications that humans directly interact with (for example, mobile apps, web apps, and so on) ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/a5ce6e1e-bde6-42d0-a25e-d809e5aee1e0.xhtml#a0c6edc6-a702-4931-b638-53c1686f306e))

## OWASP Top 10 protection



The Open Web Application Security Project (OWASP) Top 10 delivers an industry-recognized awareness document for the most common web application security threats.

As ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/66ca9b5f-1351-4e8c-bb60-f0938f54a11d.xhtml#11616b4e-1ed0-4991-9ea8-cc452600a170))

## Identity federation



it is possible for users whose accounts reside in the identity provider to also be granted access to the main application ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/a429df55-e9fe-44d8-a10d-0c22f6478461.xhtml#b4bc3894-99ab-49d0-8cf0-90db3f651160))

## CORS



Cross-Origin Resource Sharing (CORS) is a W3C standard for allowing user agents (for example, a browser) to enable different-origin requests to take place in a secure way, therefore allowing user agents to securely get by restrictions.

Further information can be found at https://www.w3.org/TR/cors/. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/042555f0-2844-4b43-8d18-766d8c9063f3.xhtml#b35cf342-efeb-427b-bf59-3eb701d4c4f1))


CORS ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/042555f0-2844-4b43-8d18-766d8c9063f3.xhtml#71507b87-6be5-45ef-bc84-e29b31a0f2ac))


Vikram: [Bookmark ]

## What are APIs and why should a business care?



In fact, according to programmableweb.com (a well-known public API catalogue), the number of publicly available APIs has been growing exponentially, reaching over 20k as of August 2018 ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/d3ca40f7-3990-46ab-ad9d-536e23274a7e.xhtml#84993c93-7451-41c9-8a41-3c46dd698ad0))

## Caching



For example, when a second (similar) call occurs, the downstream service won't have to be invoked as the response is already cached. This known as a Response Cache. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/0543b332-a17f-4da8-a346-894bd2bfb462.xhtml#54642e17-7f3a-404b-8a41-f6602c070314))

## The journey of API platforms - from proxies to microgateways



In order to address this, a generally accepted approach is to implement a hybrid Integration Platform as a Service (iPaaS) solution, capable of providing access to information assets regardless of where they are. The iPaaS platform should be capable of connecting to any cloud service and/or on-premise system, and delivering access to APIs. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/35821612-84cb-4348-86ac-87c96ca4ada1.xhtml#2dab95f8-ad09-435b-8a1a-9607d379befe))

## API design and mocking



Quickly design APIs with any of the main specifications available, such as OAS, API Blueprint, RESTful API Modeling Language (RAML), or even GraphQL-based APIs. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/84aa45a8-44b6-4007-b9c6-0cda98b2db48.xhtml#706d528d-f1c1-4c69-9530-11341824c17d))


There are tools on the market dedicated to the API design-first cycle, the most popular ones being Apiary.io and SwaggerHub (swagger.io); however, the latter only supports the OpenAPI Specification (OAS), whereas Apiary offers OAS in addition to API Blueprint. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/84aa45a8-44b6-4007-b9c6-0cda98b2db48.xhtml#90de67a0-ddf3-4859-803d-e941f675da97))

## APIs to monetize on information assets



APIs, on the other hand, are better suited to providing insight about how/by who/when/why information is being accessed, therefore giving the business the ability to make better use of information to, for example, determine which assets have better capital potential. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/9ed3eed4-a822-4d96-a3dd-6be15104eb64.xhtml#48868027-6921-45d4-a9b2-aeef0972ed70))

## APIs as an enabler for innovation and bimodal IT



It requires a multi-disciplinary team of people, with the right technology capabilities available to them, so they can incrementally API-enable the existing technology landscape, based on business-driven priorities ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/cc30b2d2-948c-4e2f-a45d-4aac44f7e150.xhtml#b52461f8-4a37-45cd-86d6-c41728357c8e))


The practice of managing two separate, coherent modes of IT delivery, one focused on stability and the other on agility. Mode 1 is traditional and sequential, emphasizing safety and accuracy. Mode 2 is exploratory and nonlinear, emphasizing agility and speed. ([link](https://learning.oreilly.com/library/view/-/9781787284432/Text/cc30b2d2-948c-4e2f-a45d-4aac44f7e150.xhtml#8727de8b-151b-4463-ba08-4c6db7069ad1))

[> Home](../README.md)