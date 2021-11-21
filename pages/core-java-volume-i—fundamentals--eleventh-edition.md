# Core Java Volume I—Fundamentals, Eleventh Edition

[> Home](../README.md)
## Chapter 6: Interfaces, Lambda Expressions, and Inner Classes



One of the interfaces, BiFunction<T, U, R>, describes functions with parameter types T and U and return type R. You can save our string comparison lambda in a variable of that type: ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#fabcfc72-f2f6-4bf5-91f6-2a408640a4bf))


Vikram: [You can think of it as takes any two parameters  and  returns one.]


You never specify the result type of a lambda expression. It is always inferred from context. For example, the expression ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#353f3d0b-41d0-4e66-bce8-ac093703ec86))


A lambda expression is a block of code that you can pass around so it can be executed later, once or multiple times ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#0d71d794-a1e9-4413-af90-545062013a5c))


The rule is that any captured variable in a lambda expression must be effectively final.  ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#65c696a3-1f94-4666-8251-cbcdf2341272))


 a lambda expression, you can only reference variables whose value doesn’t change ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#65f85ef3-cde4-43dd-a943-b30a4dd3ba2d))


The technical term for a block of code together with the values of the free variables is a closure. ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#ba87835b-197b-43a9-84ed-442c072b6c8b))


6.2.6 Variable Scope
Often, you want to be able to access variables from an enclosing method or class in a lambda expression. Consider this example: ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#82db3a6e-f85c-4be8-8ed5-c566d4f6ce53))


Vikram: [Continue from here 28/09/2021]


Note that a lambda expression can only be rewritten as a method reference if the body of the lambda expression calls a single method and doesn’t do anything else ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#f49fbb4d-020f-4af4-9319-5ae5c591c5c9))


In the second variant, the first parameter becomes the implicit parameter of the method. For example, String::compareToIgnoreCase is the same as (x, y) -> x.compareToIgnoreCase(y). ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#29cee4e1-d641-4b2a-8821-76b959da2ed5))


Arrays.sort(strings, String::compareToIgnoreCase) ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#1e84b399-a530-4304-b864-3b6d676ca557))


The expression System.out::println is a method reference. It directs the compiler to produce an instance of a functional interface, overriding the single abstract method of the interface to call the given method. In this example, an ActionListener is produced whose actionPerformed(ActionEvent e) method calls System.out.println(e ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#cbc84e2b-afff-46a7-8e5f-d61513b1107a))


The Java API defines a number of very generic functional interfaces in the java.util.function package ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#510a6369-4147-4bde-af5a-df7e0f79254a))


It is best to think of a lambda expression as a function, not an object, and to accept that it can be passed to a functional interface ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#346c7160-e735-41a3-a08d-eca0d3c9f61e))


You can supply a lambda expression whenever an object of an interface with a single abstract method is expected. Such an interface is called a functional interface. ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#65389fae-f2e5-47d7-96df-7fb2796669cb))


The key point is that the actionPerformed method contains code that you want to execute later ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#775b4b59-931d-45f4-a204-4a310f816f62))


What happens if the exact same method is defined as a default method in one interface and then again as a method of a superclass or another interface ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#28f32cd3-89ef-4287-aee1-feb5c3fb18dc))


As of Java 8, you are allowed to add static methods to interfaces ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#3e84476f-0c1d-428e-a768-ffb5c5860e8f))


If there is a common algorithm for comparing subclass objects, simply provide a single compareTo method in the superclass and declare it as final. ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#14d1ffa8-3f85-440c-9ac0-aac799911ae1))


Chapter 6Interfaces, Lambda Expressions, and Inner Classes ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter6.xhtml#e56ed09d-622b-4eb1-bca1-6254cb50e575))


Vikram: [Chapter 6 notes]

## Chapter 12: Concurrency



var contents = new String(Files.readAllBytes(
   Path.of("alice.txt")), StandardCharsets.UTF_8); // read file into string
String[] words = contents.split("[\P{L}]+"); // split along nonletters
Arrays.parallelSort(words); ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter12.xhtml#cd01ff87-5b86-411f-81f5-66002cf94923))


Vikram: [Read file contents into a string in one line]

## Chapter 8: Generic Programming



1 The Advantage of Type Paramete ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter8.xhtml#62688b39-7cb8-4717-8045-1db1f78370e9))


Vikram: [1) Otherwise, Object has to be used and a cast becomes compulsory. 
2) Compile time checking.
If objects do not match the parameter type, they are not accepted.
  ]


Generic classes and methods have type parameters. This allows them to describe precisely what should happen when they are instantiated with specific types. Prior to generic classes, programmers had to use the Object for writing code that works with multiple types. ([link](https://learning.oreilly.com/library/view/-/9780135167199/chapter8.xhtml#8283200a-b043-4e84-8971-7e05961a9886))


Vikram: [Defined Generic Classes]

[> Home](../README.md)