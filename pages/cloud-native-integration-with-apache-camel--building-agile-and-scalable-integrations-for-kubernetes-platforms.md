# Cloud Native Integration with Apache Camel: Building Agile and Scalable Integrations for Kubernetes Platforms

[> Home](../README.md)
## 2. Developing REST Integrations



@Singleton
@Unremovable
public class MyObjectConverter implements TypeConverters { ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#45a680f5-45a2-45a9-a458-c03e6f524bdc))


Vikram: [A type converter]


.choice()
.when(header("preferred_title").isEqualToIgnoreCase("mrs"))
   .setBody(simple("Hi Mrs. ${header.name}"))
.when(header("preferred_title").isEqualToIgnoreCase("mr"))
   .setBody(simple("Hi Mr. ${header.name}"))
.when(header("preferred_title").isEqualToIgnoreCase("ms"))
   .setBody(simple("Hi Ms. ${header.name}"))
.otherwise()
   .setBody(simple("Hey ${header.name}")); ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#846b05bd-0611-4b58-a943-6374289bbd9f))


Vikram: [Use a choice to select among alternatives]


exchange.getMessage().setBody(fileList); ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#d2e866ab-ec3b-4bdc-872d-10d965751d9d))


Vikram: [Get the message and set the payload to file list]


bean(FileReaderBean.class, "listFile" ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#cae2ac21-0c12-4a4d-a925-6c35c6d3639b))


Vikram: [Call the bean's listFile method]


MyObjectConverter is a bean because it is annotated with @Singleton, which means that a single instance of this object will be created and maintained by the bean registry ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#6eb9a9f8-cbc4-4f99-8ca2-a74e71c8cca5))


In this example, you are marshalling the data, which means transforming a Java object structure into a binary or textual format. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#511c58fc-be43-4ca9-84eb-8b09514a209b))


Vikram: [This is similar to converting XML/JSON tree to bitstream (or BLOB)]


Using libraries as JAXB or JSON-B you can transform Java objects into XML/JSON or transform the Java object into an XML/JSON document. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#ee1733e9-2232-4c68-b48b-d4fdf152845b))


You can incorporate conditional steps in your routing logic using predicates. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#aa8aba44-a4b2-4dbf-acaf-aea169b72764))


Beans can be accessed using the beans() fluent builder or using the bean component, in that case making reference to bean: endpoint. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#e31db8ff-df2a-4023-b978-cb3a6e60db45))


even though each exchange produces logs in different routes, the path-router and the logger- router, they are executed in the same thread because of the direct component. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#21e26860-c3c6-43b3-9f58-e144d9810585))


Direct allows you to aggregate a routing logic to another route. This way you can reuse a routing logic in more than one route. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#c5150144-5aa7-45c6-a052-b3a6ea43442e))


The direct component allows you to link, synchronously, different routes in the same Camel context. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#608c5703-b9f4-411c-a153-53050dfdf2a2))


In 2016, the tooling and the specification were split, and the specification was renamed to OpenAPI. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#2b79b092-04c3-4a4d-ae67-f85a19ed7316))


Created in 2011, Swagger is an open-source project that created a JSON/YAML representation for RESTful applications, taking many of the features built for the SOAP protocol. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#696c9018-1bc2-4d9a-954e-0ec9ee650707))


${body} is an example of an EL, in this case the Simple EL. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#59a49f56-b172-40bf-8974-1e54da26554a))


Camel extensions already declare the other extensions they depend on. For example, the camel-quarkus-core dependency is already declared by camel-quarkus-rest. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#34d2d431-c83c-4697-a19d-103d654c0bf6))


The JAX-RPC specification was a big step in standardizing HTTP-based communication using SOAP (Simple Object Access Protocol), an XML-based messaging protocol. JAX-RPC was eventually succeeded by the JAX-WS (Web Service) specification. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_2_Chapter.xhtml#0ae1c84f-12cf-4fb3-a594-bb6df52b9a20))

## 3. Securing Web Services with Keycloak



tokens = client.refreshTokens(tokens.getRefreshToken())
.await().indefinitely();
      currentTokens = tokens; ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#2a6a9a02-00c0-4db8-8c0b-6c6f430d2b71))


Vikram: [Does this keep refreshing asynchronously? Why is it done on demand if it's done in init?

Possibly: Whenever called, the token is checked to see if it's expired, and then this call is made. As a getToken call was already made during initialization, now only refreshToken() is sufficient. The await() possibly means this is done asynchronously and indefinitely() means that there is no time limit.]


currentTokens = client.getTokens().await().indefinitely(); ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#59e0c523-d01e-4810-bd76-75a78dc0071e))


Vikram: [Done at init. Does this keep refreshing asynchronously?

Possibly doing this asynchronously with no time limit.]


.bean("tokenHandlerBean") ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#37f23de6-b786-43ff-ab2c-734140a28e3a))


Vikram: [All Token handling is done in the bean]


You are passing it as a header because HTTP clients transform message headers into HTTP headers. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#ad782ff2-f0b3-4929-9ade-5e635e2a32cf))


You also get a refresh token that allows the client to get new tokens and continue to access the resource server without a new authentication process. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#a500ad62-a36c-41af-b415-459201088383))


The only thing that is somewhat different is to implement the equals() and hashCode() methods . This is done to avoid duplicate entries in the contact list. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#a935c175-d2b1-4709-835d-7a7580e3699b))


By setting the bindingMode(RestBindingMode.json) you’re telling Camel that you want the incoming JSON data to be transformed into a POJO object, in this case the type(Contact.class) for the post() operation, and that the responses must be automatically converted to JSON. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#b3a0bf6c-2e74-451f-9008-4bcd0a2105ce))


Keycloak implements two standards for authentication and authorization: SAML 2.0 and OpenID Connect. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#b5cdafde-6639-41e6-8bc3-df2b01ebff94))


“OpenID Connect 1.0 is a simple identity layer on top of the OAuth 2.0 protocol.”2 ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#066504b0-be33-4b73-861c-9f66d9c7ce49))


The OAuth 2.0 specification, which is the current version, describes six different grant types:
Authorization Code

Client Credentials

Device Code

Refresh Token

Implicit Flow

Password Grant ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#f30cc1b5-6e7f-4b67-97a9-fdc257f82fac))


OpenID is responsible for the authentication and OAuth for authorization. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_3_Chapter.xhtml#f87a1e97-9b50-4ba5-92f9-7ca0d49f67a8))

## 4. Accessing Databases with Apache Camel



SEDA. This component, based on a staged event-driven architecture, will create an in-memory queue so you can process messages in different threads. This way you are asynchronously sending a message copy to be processed by another thread. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_4_Chapter.xhtml#6be2c013-f393-4b85-ad4d-7a980ca6f8b5))


Vikram: [#TryOut Can I use this to implement #StatefulFilter that I had created for YNAP Gigya flow?]


Wire Tap is an integration pattern that allows an exchange to be copied or a new one to be generated using data from the original exchange, and sends it asynchronously to another endpoint. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_4_Chapter.xhtml#57a71e81-7266-4da2-ac52-b309a61ca465))


Camel comes with predefined strategies to handle exceptions called error handlers . ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_4_Chapter.xhtml#e2800dfb-e548-4bdf-a10a-7de0e118a4e1))


As you can see, try/catch/finally works in a very similar way as in the Java language. You could have multiple doCatch() clauses, you could nest a try/catch/finally inside a doTry(), and so on. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_4_Chapter.xhtml#611bd85e-e9aa-487f-87a3-be2a42c79c0a))


You are sending the parameters dynamically using the JPA_PARAMETERS_HEADER header. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_4_Chapter.xhtml#28bb81ec-6a6f-4a6e-9a9e-47fb9f3165ea))


You are using CDI to register a named bean containing the parameters you need for that query. You use the JPQL named parameter as the key for the map and you can set any object as the value ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_4_Chapter.xhtml#152235bf-a0cf-44e9-b442-aa0b6964ddfc))


Instead of declaring the route logic nested in the REST DSL, I decided to separate each route and call them using direct ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_4_Chapter.xhtml#7075d765-e60f-4975-a4ea-1e49e5c6673c))


Vikram: [Makes it easier to follow. 
It is like using a route label, but here each route is equivalent to a new flow]


.to("jpa:" + Contact.class.getName()+ "?findEntity=true"); ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_4_Chapter.xhtml#ef56b312-7b2b-4dfd-868f-8d781146bac9))


Vikram: [New JPA component findEntity]

## 6. Deploying Applications to Kubernetes



A mebibyte is just a different way to represent memory allocation, where 1 MiB = 2ˆ20 bytes or 1,048,576 bytes. Meanwhile 1MB is 10ˆ6 or 1,000,000 bytes. If you want to know how much 73Mi means in MB, just multiply the bytes for 1.04858, which is 76.546MB. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_6_Chapter.xhtml#d9b3c895-4180-48db-94d9-1a3ef7d74d36))


If an application tries to use more memory than its limit, Kubelet will kill the application, causing it to restart to fix the problem. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_6_Chapter.xhtml#6f1a8bd5-cd72-415a-a855-a7940ff38452))


If a new pod has its requirements specified, the scheduler will try to find a node that matches the amount of CPU and RAM requested by the pod. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_6_Chapter.xhtml#fb73a0fe-ba88-432c-b677-f9643e802249))


Requests and Limits are ways to tell Kubernetes how much resources you believe the application should consume. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_6_Chapter.xhtml#3b2abca0-dcaf-4acc-84e9-eec3f29ab987))


In order to identify the application state, Kubernetes defines test routines called probes. There are three: Readiness, Liveness, and Startup. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_6_Chapter.xhtml#d6afc7d0-0582-4a24-989b-17185715dd63))


Quarkus allows you to use the same application.properties files to declare properties for different profiles ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_6_Chapter.xhtml#1be250f2-7050-4b96-afb3-85481bfd257d))


ConfigMaps and Secrets are Kubernetes resources that allow users to separate images from the configuration. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_6_Chapter.xhtml#c6ada3a6-245c-405a-8bed-8d1a2418c21d))

## 1. Welcome to Apache Camel



The code will be packed in the quarkus-app/app directory and the dependencies you use to work with Camel will be in the quarkus-app/lib/main directory. This process guarantees that the foundational classes are loaded first, in this case Quarkus classes, and then your code will be loaded, making the startup process smarter and, therefore, faster. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#f90c496d-2bd2-4e42-8870-4aa1642082e7))


The class-path points to Quarkus’ dependencies only and the main-class attribute points to a Quarkus class. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#4d83c08a-b98e-443f-aff6-0a5c07226344))


Vikram: [This manifest file of quarkus-run.jar   shows this.]


With the plugin goal quarkus:add-extension you can manipulate your pom structure in a simplified way. This command will add the dependencies you need using the version you have mapped in the Quarkus bill of materials, so you don’t need to worry about compatibility. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#03ca7267-8ccd-4d04-b7a0-c2143379ecd9))


Established in June 2015, the OCI is a Linux Foundation project, as is the CNCF, which was designed to create open industry standards around container formats and runtimes. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#8e1af68d-8cd6-468c-8c80-3a6fa5a34887))


Well, now you have the understanding of how to pack Java code using quarkus-maven-plugin. This is going to help you to distribute your code, especially in standalone applications, that you can configure as a service in the OS. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#e2755ef2-624f-4ec1-9946-53796eb3a688))


Native Image is one running mode of GraalVM, a JDK project developed by Oracle to improve the code execution of Java and other JVM languages. In this mode, a native executable is created by the compiler ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#87b52643-4101-42c7-a6a6-96fab8b8a92e))


In Quarkus, there are two ways of doing it: traditional JVM or native compilation. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#d0f83580-e244-42a7-b61d-c539ab8a851c))


The MicroProfile specification is the equivalent of the Jakarta EE (formerly known as Java Platform, Enterprise Edition – Java EE) for the microservices frameworks. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#ef1b5f09-b752-4f95-82d1-bd1cba83aa14))


Vikram: [Microprofile is the J2EE subset for microservices.]


Quarkus provides a “bill of materials” dependency called quarkus-universe-bom, where every component of the framework is declared. This way you won’t need to worry about every dependency version and the compatibility between them. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#0a7889ed-f189-4236-a534-81e7d70a7060))


JDK 11 installed with JAVA_HOME configured appropriately

Maven 3.6.3 with M2_HOME configured ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#a8a69e50-5eac-4fa1-b21f-8c3a87dd8090))


Having many microservices running in Java is now very resource expensive. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#ce91f1c3-48f1-44bd-9bbf-5fe981b3d34c))


Now instead of deploying ten war files to an application server, these ten new services are packed into ten different container images, creating ten JVM process running as containers, which are orchestrated by your Kubernetes cluster. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#6f4d589d-ddba-4e38-b7e7-6514bf69f88e))


Vikram: [These services could be built with fat jars that run on jre.]


They created isolation mechanisms so every application could have its own class loading process, or could specify exactly which dependencies it would use, using for example the OSGi framework, but this didn’t solve the risk of putting all of the eggs in the same basket ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#54472726-d7f3-4624-a464-11da73629137))


Application servers provided centralized capabilities such as security, resource sharing, configuration management, scalability, logging, and so on, with a very small price to pay: a few megabytes for the virtual machine and a few megabytes for the application server code itself, besides additional CPU usage. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#ece5ae80-429f-4ef4-a817-0bf3addf4b13))


Vikram: [These are websphere, web logic and jboss. 
This was ok as all applications were deployed on the same server. 
Scaling these was a problem.]


Quarkus is an open source project released in 2018. It was made especially for the Kubernetes world, creating a mechanism to make Java development for Kubernetes a lot easier, and also dealing with Java “old” problems ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#fe8f3ac8-a9b4-47ec-a474-ff509d84b7e4))


The setBody() method receives as an argument an object of the type Expression ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#39850674-b53f-4a00-9803-1229a399f451))


This means that every time the timer triggers, a new Exchange will be created, and that object will be available until that execution is finished ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#fbb3a9a4-934c-4341-8650-5faf2b6dd0c9))


Vikram: [Analogous to the code is in the compute node being activated for the duration of the message being processed.
Exchange has the properties message, properties, exception which are similar to input root, input properties, and exception list. And it also has from endpoint, exchange id, pattern. The first two are part of the message headers and pattern must be responsible for parsing. If so it’s similar to the parsers set before the computer node.]


This execution of an incoming event is called an Exchange . ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#45d79de7-68ab-4a3c-bc5c-76fc988638a5))


By executing the configure() method, the outcome of these stacked calls is a route definition and it is used to instantiated many objects in memory. These objects in memory will react to events being triggered to or by the from (consumer) endpoint ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#9893420a-3187-4805-b640-132c7235e024))


This is because Camel utilizes a fluent way to write routes where you can append definitions on how your route should behave or simply set attributes to your route ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#ddf6c95e-33ba-4448-abab-44cca07914ee))


Every integration built with Camel uses a concept called a route . The idea is that an integration always starts from an endpoint and then goes to one or multiples endpoints ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#e0dd50b9-9e76-4872-91ab-6fc4590c0c0d))


The CNCF’s objective was to maintain the Kubernetes project and also to serve as an umbrella for other projects that Kubernetes is based on or that would compose the ecosystem. In this context, cloud native means “made for the Kubernetes ecosystem.” ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#5c6cd848-a4a4-490d-9da8-965cafa57406))


Container: “A way of packing and distributing applications and their dependencies, from libraries to runtimes. From an execution standpoint, it is also a way to isolate OS (operating system) processes, creating a sandbox for each container, similar to a virtual machine idea.” ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#de4a4495-4858-49eb-8dcc-6435fe2a6103))


Removing the integration layer wouldn’t mean that business information or data would get lost; it would only impact the integration of those services ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_1_Chapter.xhtml#3b7b026e-64a6-4c12-946a-59fb16efe12d))

## 5. Messaging with Apache Kafka



docker exec -it broker /opt/kafka/bin/kafka-topics.sh       --bootstrap-server localhost:9092 --delete --topic myTestTopic ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#0c0201fd-ad1f-4cff-9514-95a53f5e76c1))


camel-kafka-consumer-v2/ $ mvn clean quarkus:dev 
-Ddebug=5006 -Dkafka.clientid=test -Dkafka.groupid=testGroup           -Dkafka.consumers.count=2  -Dkafka.consumers.stream=1 ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#290372cb-9592-497c-bb20-346da7c905f3))


Vikram: [Two consumers and one thread only. So only message is processed at a time.]


camel-kafka-consumer-v2/ $ mvn clean quarkus:dev 
-Ddebug=5006 -Dkafka.clientid=test -Dkafka.groupid=testGroup  -Dkafka.consumers.count=1 -Dkafka.consumers.stream=10 ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#2f369026-2b07-48ed-8dbb-3e1f41abc5d9))


Vikram: [Starting a consumer with one consumer and 10 threads.]


The consumerStreams parameter is responsible for setting the number of threads for the component’s thread pool and the consumersCount is responsible for setting the number of Kafka consumers in the application. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#11bcf137-7826-4cd3-b491-17ae3fc4526d))


Have in mind that the number of active consumers will depend on the number of partitions currently available for that topic. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#41b1aee4-0642-4a2e-9e4f-2d67f72d8635))


If you look at the consumers’ logs, you will see that the consumer without a partition assigned is not receiving messages. This is called a starving consumer. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#d73af687-1a3d-4cb9-a611-e731272be4da))


i=0; while [ $i -lt 10 ]; do ((i++)); curl -w "n" -X POST 'http://localhost:8080/kafka' -H 'Content-Type: text/plain'   -d "Message number: $i" ; done ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#1025c931-abcc-476f-80ef-4bc49b0dee96))


from("{{kafka.uri}}") ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#a577380f-d3c7-478f-acbe-fc08181f1cca))


kafka.uri=kafka:{{topic}}?brokers={{brokers}}&clientId={{id}} ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#c059adca-1035-415e-a190-fc3315716bc2))


Right before the Kafka component step, you are removing the message headers using a catch-all pattern. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#ba8120aa-7f6f-47e3-a550-77bfa16f0d5b))


.removeHeaders("*")
    .to("{{kafka.uri}}")
    .removeHeaders("*")
    .setBody(constant("message sent.")) ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#fec00330-8f2c-424e-bb38-2c56ed588703))


If you look at the logs on the first consumer, you will see that now only one partition is assigned to it. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#d58ae361-42c4-4102-8c05-11c9bc99b533))


For this example, you are using Docker compose because Kafka needs a Zookeeper instance to connect to, so you define two services in the document, zookeeper and kafka ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#157d4a68-344d-4617-8b3c-a2eb4150c0c8))


topics in Kafka are essentially a group of partitions. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#96bd1972-37ad-40ba-b63a-249e315635e5))


Consumer group allows different instances of the same consumer application to parallelize readings without having duplication. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#0a537d7a-de10-4a51-a649-2eb857e0a2e2))


Kafka keeps message indexes using a structure called offset ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#e063e278-27cf-4a35-ac30-b7b1a315b22e))


In Kafka, messages are not consumed, they are rotated based on storage utilization or based on how long the message is persisted. ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#87aaebad-ed03-451b-b137-84e729be83a5))


Kafka only offers persistent topics ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#2511c7cb-a3aa-420b-8bf5-67f1a180d129))


Vikram: [high volumes and low latency]


In the words of the project web page, “Apache Kafka is an open-source distributed event streaming platform” ([link](https://learning.oreilly.com/library/view/-/9781484272114/html/514395_1_En_5_Chapter.xhtml#2c946efe-6cb5-4731-b879-910d773a8df0))

[> Home](../README.md)