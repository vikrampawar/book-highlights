# Core Java, Volume II--Advanced Features

[> Home](../README.md)
## Chapter 9: The Java Platform Module System



Automatic modules can read the unnamed module, so their dependencies can go onto the class path. ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#d46bb5d3-15dc-4e30-9777-db895655f3e7))


Any class that is not on the module path is part of an unnamed module. Technically, there may be more than one unnamed module, but all of them together act as if they are a single module which is called the unnamed module. As with automatic modules, the unnamed module can access all other modules, and all of its packages are exported and opened. ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#ed721d61-56f2-47b4-94b5-eef24b521ee7))


Recall from Chapter 5 of Volume I that JAR files can contain, in addition to class files and a manifest, file resources which can be loaded with the method Class.getResourceAsStream, and now also with Module.getResourceAsStream ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#72e74c8c-6734-496e-a2ec-434636ed660c))


Open modules combine the compile-time safety of the module system with the classic permissive runtime behavior. ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#84b1a9c0-1aa3-412c-9f7a-6f9047c5b3ed))


Using the opens keyword, a module can open a package, which enables reflective access to all instances of classes in the given package. ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#cd3ed744-3f90-4a80-ba4f-c0c71f1d907f))


If you want to load a module into JShell, include the JAR on the module path and use the --add-modules option: ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#3b294302-9c92-409a-92ea-1199b72e8757))


Instead, a module can be deployed by placing all its classes in a JAR file, with a module-info.class in the root. Such a JAR file is called a modular JAR. ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#e0b3da1d-ff8e-4660-999b-3cfbef81723a))


Module names are only used in module declarations ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#f7687580-d2df-4611-b1a8-99a37a6b3a10))


A module can make classes and packages selectively available so that its evolution can be controlled. ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch09.xhtml#c440fa6a-c897-4a81-8ec7-e821f3a77e52))

## Chapter 6: The Date and Time API



The Instant class is a close analog to java.util.Date. In Java 8, that class has two added methods: the toInstant method that converts a Date to an Instant, and the static from method that converts in the other direction. ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch06.xhtml#d2bf8bd8-76dd-4017-81d3-7df1daca3c34))


The third time is a charm, and the java.time API introduced in Java 8 has remedied the flaws of the past and should serve us for quite some time. ([link](https://learning.oreilly.com/library/view/-/9780135167175/ch06.xhtml#915c4182-e278-421e-ad13-662eb8da778d))

[> Home](../README.md)