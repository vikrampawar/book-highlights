# Mastering Service Mesh

[> Home](../README.md)
## Service mesh architecture



The control and data plane, when used together, form the service mesh: ([link](https://learning.oreilly.com/library/view/-/9781789615791/0d0d93c3-538d-4959-b23f-91c2c5266a46.xhtml#029106c1-f785-40c8-a35f-f2f36b34b284))

## Service mesh overview



Smart endpoints: Service-to-service communication is done through the intelligent endpoints, which is a DNS record that resolves to a microservice. The use of DNS records facilitates one service to communicate with others, and this eliminates the load balancer between microservices ([link](https://learning.oreilly.com/library/view/-/9781789615791/6c7e3a5a-2c0d-418a-b9d7-9e99a0d8b024.xhtml#fdd59c7a-6bee-4298-b40f-d54229240904))


Dumb pipes: Service-to-service communication uses basic network traffic protocols such as HTTP, REST, gRPC, and so on. This type of connection is opposed to a centralized smart pipe using the ESB/MQ of monolithic applications ([link](https://learning.oreilly.com/library/view/-/9781789615791/6c7e3a5a-2c0d-418a-b9d7-9e99a0d8b024.xhtml#c1500984-c8b5-4e3f-8965-bcb0e9531bd0))


The service mesh concept is a significant shift from earlier versions of DevOps, where operations were limited to software release management. ([link](https://learning.oreilly.com/library/view/-/9781789615791/6c7e3a5a-2c0d-418a-b9d7-9e99a0d8b024.xhtml#e9539b78-0c38-4079-80a8-3dfa0af62b64))


We can view a service mesh as a decoupling agent between Dev (provider) and Ops (consumer) ([link](https://learning.oreilly.com/library/view/-/9781789615791/6c7e3a5a-2c0d-418a-b9d7-9e99a0d8b024.xhtml#1ff42108-c7bd-4df9-a531-9cbe236ead6e))

## Who owns the service mesh?



In a cloud-native environment, the service mesh has moved from Dev to Ops ([link](https://learning.oreilly.com/library/view/-/9781789615791/a46e9885-a658-4f2c-8a5f-b1a2049754ca.xhtml#1dc63131-2a08-4032-a378-9a0513a0dd96))


In the legacy world, service mesh models used to belong to developers during the times of monolithic applications and SOA/ESB applications. ([link](https://learning.oreilly.com/library/view/-/9781789615791/a46e9885-a658-4f2c-8a5f-b1a2049754ca.xhtml#1024bd5b-2b23-4c01-9e44-e3f3728d8a68))

## Service mesh rules



A perfect service mesh should establish the ORASTAR rules without having to code anything at the microservice level ([link](https://learning.oreilly.com/library/view/-/9781789615791/06dd8fef-c3b2-41c4-a887-23742cbd7a22.xhtml#d4a1c749-ff5a-4ee5-8181-8ac36ed3cf21))

## Useful terms



The circuit breaker breaks the connection between microservices following the detection of latency/faults ([link](https://learning.oreilly.com/library/view/-/9781789615791/c064cb9b-0532-4ac4-8cb1-44868176406d.xhtml#ce775284-1ad8-413d-8887-3b22c1aa3383))


Canary release is about a new version of a microservice available to a small subset of users in a production environment along with the old version ([link](https://learning.oreilly.com/library/view/-/9781789615791/c064cb9b-0532-4ac4-8cb1-44868176406d.xhtml#76f6174e-41ca-42b2-8b0d-f805834af000))

## Cloud-native infrastructure



Red Hat OpenShift, Cloud Foundry, Apache Mesos, and others fill the hybrid cloud model ([link](https://learning.oreilly.com/library/view/-/9781789615791/91f3898f-ce41-4918-bb8d-c0cfb9907745.xhtml#c9cf43aa-417c-49bc-b6bb-bcd99ecea4f6))

## Service Mesh Architecture



Service mesh has gained popularity since 2017, and it is still a relatively young concept ([link](https://learning.oreilly.com/library/view/-/9781789615791/9d975ee7-fc79-4df3-9884-74001f76cc63.xhtml#abf5e148-9d0c-4485-af0e-246ea45d7dfa))

## Who this book is for



This book covers the operation part of DevOps, and so is most suited for operational professionals who are responsible for managing microservices-based applications. ([link](https://learning.oreilly.com/library/view/-/9781789615791/3481a187-cf3e-488d-8540-1c73973599e9.xhtml#ab070184-5d85-4e82-9088-3efbcf7c7c9d))

## Early pioneers



One nugget of wisdom from Jeff Bezos was two-pizza teams – individual teams shouldn't be larger than what two pizzas can feed ([link](https://learning.oreilly.com/library/view/-/9781789615791/3fd7bd40-c129-4831-b772-fcd4b4c693dc.xhtml#7dd69f4a-6eb8-4293-b407-70b0a3c384c2))

## Container orchestration platforms



Decoupling is the central theme of a container orchestration platform ([link](https://learning.oreilly.com/library/view/-/9781789615791/2218ac3b-059e-4f51-bc88-ea43a42b67d5.xhtml#8d89d3d4-2e4a-4222-87c2-bf49dde7b91f))


Red Hat integrated CoreOS with OpenShift starting with version 4.1 to provide a container orchestration platform for enterprises that has zero downtime. It's a self-updating operating system with Kubernetes++ ([link](https://learning.oreilly.com/library/view/-/9781789615791/2218ac3b-059e-4f51-bc88-ea43a42b67d5.xhtml#c877623a-0cfc-4311-8f21-cf7628ae1f88))

## Preface



A service mesh is a framework on top of a cloud-native microservices application. Istio, Linkerd, and Consul are all service mesh implementations. ([link](https://learning.oreilly.com/library/view/-/9781789615791/b59ac405-dba8-4a5c-9ad4-a7843043b30b.xhtml#ce0f9fc6-1e6d-4fd6-9e20-5fad5af91a74))


William Morgan, the creator of Linkerd, which is an incubating project at CNCF, coined the term service mesh. ([link](https://learning.oreilly.com/library/view/-/9781789615791/b59ac405-dba8-4a5c-9ad4-a7843043b30b.xhtml#3344d8f5-6aca-480a-a900-ffe670283310))


It assumes that you have prior knowledge of Docker and Kubernetes. As a developer, knowing Service-Oriented Architecture (SOA) and Enterprise Service Bus (ESB) patterns will be beneficial, but not mandatory. ([link](https://learning.oreilly.com/library/view/-/9781789615791/b59ac405-dba8-4a5c-9ad4-a7843043b30b.xhtml#96893470-ee42-437f-ac4a-4a9427973705))

## What is a microservice?



self-service model for the consumption of services ([link](https://learning.oreilly.com/library/view/-/9781789615791/de27c1c1-0d69-41c5-a387-f1b68145ad3a.xhtml#5b5177a9-60bd-4aba-a021-4ab86dd55001))


The business logic, including inter-service communication, is done through smart endpoints and dumb pipes. This means that the centralized business logic of ESBs is now distributed among the microservices through smart endpoints, and a primitive messaging system or a dumb pipe is used for service-to-service communication using a lightweight protocol such as REST or gRPC. ([link](https://learning.oreilly.com/library/view/-/9781789615791/de27c1c1-0d69-41c5-a387-f1b68145ad3a.xhtml#720dbe2b-ed17-4bcc-a3ce-4aae75cd86af))


The microservices architecture eliminated the need for a centralized ESB ([link](https://learning.oreilly.com/library/view/-/9781789615791/de27c1c1-0d69-41c5-a387-f1b68145ad3a.xhtml#3c11c7d2-17d9-4891-9dd6-f49ec02285fe))


The natural transition of SOA/ESB is toward microservices, in which services are decoupled from a monolithic ESB ([link](https://learning.oreilly.com/library/view/-/9781789615791/de27c1c1-0d69-41c5-a387-f1b68145ad3a.xhtml#ea1f006d-7542-4943-997c-634d0c102a4b))

## API Gateway



In the preceding diagram, the API gateway is used to expose the three-tier and SOA/ESB-based services in which the business logic contained in the ESB still hinders the development of the independent services ([link](https://learning.oreilly.com/library/view/-/9781789615791/ca3e8a26-b91d-479c-b2aa-b9dbe8c9267a.xhtml#ff449235-6b5b-4992-b516-b0a3af1989a3))

## An introduction to CNAs



One of the most popular cloud-native application development platforms is known as Red Hat OpenShift, a platform where we can focus on writing the business logic for the application. Containerization happens automatically, without having to write any code, while deployment (production or canary) occurs automatically through a CI/CD pipeline. ([link](https://learning.oreilly.com/library/view/-/9781789615791/5d1b86d2-90d6-4d36-a233-013de8ddeda7.xhtml#dcdd9860-ddc9-4bcf-ab47-7d15ae4ce3b8))

## Shifting Dev responsibilities to Ops



It is important to note that a proper service mesh implementation frees up developers, but it adds more responsibilities to operations ([link](https://learning.oreilly.com/library/view/-/9781789615791/e4469341-eb4f-41d8-8df6-4e45e254ce42.xhtml#13d917fc-bf97-4f82-9871-2b82fe968c9c))


The role of a developer ends with a commit process as they continue to focus on the implementation of business logic in the microservices. ([link](https://learning.oreilly.com/library/view/-/9781789615791/e4469341-eb4f-41d8-8df6-4e45e254ce42.xhtml#a7c80321-1a1e-477e-82f1-18ae81bb7118))

[> Home](../README.md)