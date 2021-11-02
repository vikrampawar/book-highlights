# Enterprise Integration Patterns: Designing, Building, and Deploying Messaging Solutions

[> Home](../README.md)
## Chapter 7. Message Routing



This process is analogous to the SYN messages exchanged during the connect sequence of the TCP protocol (see [Stevens]). ([link](https://learning.oreilly.com/library/view/-/0321200683/ch07.html#e53984ee-8ed0-45b5-96e8-048e79e7f07e))


When designing messaging solutions, it is actually helpful to look into some of the internals of TCP, because at its core, IP traffic is asynchronous and unreliable and has to deal with many of the same issues enterprise integration solutions do. For a thorough treatment of IP protocols see [Stevens] and [Wright]. ([link](https://learning.oreilly.com/library/view/-/0321200683/ch07.html#ba5d2783-b79e-4098-82cf-0da986e80435))

## Chapter 8. Message Transformation



So, while messaging provides the most reliable and responsive way to transmit information, it may not be the most efficient. ([link](https://learning.oreilly.com/library/view/-/0321200683/ch08.html#459531cf-95de-4a91-9593-60da50f34a5b))

## Chapter 3. Messaging Systems



Connect the applications using a Message Channel, where one application writes information to the channel and the other one reads that information from the channel. ([link](https://learning.oreilly.com/library/view/-/0321200683/ch03.html#edc01b83-d6e2-4d40-bb6f-3361942cd8e8))


How does one application communicate with another using messaging? ([link](https://learning.oreilly.com/library/view/-/0321200683/ch03.html#85e8299e-1a9f-4f89-a895-f2839375a310))

## Chapter 10. Messaging Endpoints



The term idempotent is used in mathematics to describe a function that produces the same result if it is applied to itself: f(x) = f(f(x)). In Messaging (53) this concepts translates into a message that has the same effect whether it is received once or multiple times.  ([link](https://learning.oreilly.com/library/view/-/0321200683/ch10.html#d212b277-4169-4de2-a61e-dc2b01ce942c))


Design a receiver to be an Idempotent Receiver, one that can safely receive the same message multiple times ([link](https://learning.oreilly.com/library/view/-/0321200683/ch10.html#0e400567-f39b-40b0-ab4e-543afadbb010))


For this reason, some messaging systems only provide at-least-once delivery and let the application deal with duplicate messages ([link](https://learning.oreilly.com/library/view/-/0321200683/ch10.html#99146110-5473-410f-8c3f-6c56123edab2))

## Chapter 5. Message Construction



With the SOAP protocol [SOAP 1.1] and WSDL service description [WSDL 1.1], when using RPC-style SOAP messages, the request message is an example of this Command Message pattern ([link](https://learning.oreilly.com/library/view/-/0321200683/ch05.html#fe940735-f9a1-4162-acd9-4445616c27d5))


The Command pattern [GoF] shows how to turn a request into an object that can be stored and passed around ([link](https://learning.oreilly.com/library/view/-/0321200683/ch05.html#db80623c-bbbd-4522-b417-99fc770b6e62))

[> Home](../README.md)