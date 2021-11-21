# Strategic Monoliths and Microservices: Driving Innovation Using Purposeful Architecture

[> Home](../README.md)
## Chapter 5: Contextual Expertise



Core Domain is a subdomain within which a focused core strategic business capability is developed ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch05.xhtml#9793d372-8eef-407d-b6f8-dd7239016501))


Trying to harmonize all the meanings of policy into a single software component is fraught with problems ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch05.xhtml#8d5cbb06-8444-4d93-88c2-c06a626b4163))

## Chapter 6: Mapping, Failing, and Succeeding—Choose Two



This chapter promoted the use of Context Maps to identify relationships between any two teams and their respective Bounded Contexts ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch06.xhtml#f30d5b57-4131-4ebf-bbca-8ff55ff261ce))


 In general, abstractions adopted in the name of code reuse or even emphasis on concrete reused goals will lead to unwanted baggage at best, and potentially extensive rework ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch06.xhtml#6755977a-ddc9-45b8-99ba-3b8808b51f56))


known as Context Maps ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch06.xhtml#2ca7c078-2000-492e-a683-2d5a5818ad22))

## Chapter 1: Business Goals and Digital Transformation



Working in #agile should boil down to these four things: collaborate, deliver, reflect, and improve [Cockburn-Forgiveness]. ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch01.xhtml#bb578a82-b997-4973-8efc-d97c06469fad))


The software entropy metaphor names the condition of a software system where change is inevitable, and that change will cause increasing uncontrolled complexity unless a vigorous effort is made to prevent it [Jacobson] ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch01.xhtml#64047357-d8c5-4c40-aafc-8eb1f07b4a8d))

## Part II: Driving Business Innovation



Aggregates are entities that have a special purpose—namely, representing a set of data that per business rules must remain consistent at all times ([link](https://learning.oreilly.com/library/view/-/9780137355600/part02.xhtml#126a171c-78c3-4555-93f6-6ccd5d687d94))


Domain services provide business logic that operates on entities, aggregates, and value objects, but are not directly associated with any one of the types on which they work ([link](https://learning.oreilly.com/library/view/-/9780137355600/part02.xhtml#108740e6-e6f0-4e48-830b-5622c786c2c2))

## Chapter 2: Essential Strategic Learning Tools



A number of ADR templates are available, but Michael Nygard proposed a particularly simple, yet powerful, one [Nygard-ADR]. His point of view is that an ADR should be a collection of records for “architecturally significant” decisions—those that affect the structure, nonfunctional characteristics, dependencies, interfaces, or construction techniques ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch02.xhtml#17bdcdc5-42c6-4cf3-bed7-084ce06125ea))


Each ADR should be stored along with the source code to which it applies, so they are easily accessible for any team member ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch02.xhtml#11dc6c59-686e-45c5-9dcf-2f474c32bda4))


Plain and simple, this book promotes a very simple and versatile architecture style. It is known by a few different names. Two of the most common names for this style are Ports and Adapters and Hexagonal. It is also known as Clean Architecture, and a less common name is Onion Architecture ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch02.xhtml#70dd0af6-6a0e-4523-a8ba-2b705d2bf31b))


Figure 2.6 Impact map for White-Label Auto Insurance. ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch02.xhtml#ce05633e-be84-41ef-b331-b64cae5a836a))


Modularity is an indispensable foundation for Conway’s Law as well. That’s because modules are where we should capture critical communication and what is learned from it. At the same time, modules can save teams from smearing mud all over their solution space. Modules are used both as conceptual boundaries and as physical compartments. ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch02.xhtml#d0a90fe2-0884-4d0e-b575-9a85b48e834f))


In his essay “Delaying Commitment” (IEEE Software, May/June 1988), leading British computer scientist and professor Harold Thimbleby observes that the difference between amateurs and experts is that experts know how to delay commitments and conceal their errors for as long as possible, repairing flaws before they cause problems. Amateurs try to get everything right the first time, so overloading their problem-solving capacity that they end up committing early to wrong decisions [DrDobbs]. ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch02.xhtml#b9b97af2-976c-4069-b243-4033f168266b))

## Chapter 3: Events-First Experimentation and Discovery



It’s cheap to make these kinds of “mistakes” and learn from them. Removing a lot of unnecessary stickies is far better than imagining too few. ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch03.xhtml#cbdcdbfa-86bd-47b5-a717-3bf569ccea08))


Some practitioners—including the originator of EventStorming, Alberto Brandolini—conclude that it is impossible to use this technique properly with online collaboration tools [Remote-Bad] ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch03.xhtml#fe7643f0-fad7-4bad-9e29-c1e567dfee1e))


The basic idea behind EventStorming is to model a time-ordered series of descriptive happenings in a system ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch03.xhtml#3bb0a5e1-4490-419f-91f2-707717100381))


The key point: Teams will often start out to solve one set of problems, but discover greater opportunities to innovate through experimentation and collaboration ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch03.xhtml#d2f786b0-05f7-4eca-a0e3-40f79d4b910e))


From a software perspective, an event captures a record of the fact that a command was executed. It’s a set of data that is named in such a way that it expresses an action that occurred in the past ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch03.xhtml#a5afb88a-134b-4196-a4e3-5a369d4cf892))

## Chapter 7: Modeling Domain Concepts



Modeling Domain Concepts ([link](https://learning.oreilly.com/library/view/-/9780137355600/ch07.xhtml#35ddd8d2-c9f4-4514-85e7-46e83d87f5a8))


Vikram: [Continue from here]

[> Home](../README.md)