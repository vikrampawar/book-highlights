# Modern Java in Action

[> Home](../README.md)
## Chapter 6. Collecting data with streams



The Collectors.reducing factory method is a generalization of all of them. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_017.html#284685a7-a565-4a56-ae76-9265d0968e94))


IntSummaryStatistics menuStatistics =
        menu.stream().collect(summarizingInt(Dish::getCalories ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_017.html#fc0307ee-ba7b-4f1e-a5ad-875f9ba0ea89))


double avgCalories =
    menu.stream().collect(averagingInt(Dish::getCalories)); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_017.html#b83964ff-0d97-420d-b1a8-be34552ab5c8))


int totalCalories = menu.stream().collect(summingInt(Dish::getCalories)); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_017.html#92c1bfb5-55bc-4b43-a6ca-9cb80aa9029e))


Comparator<Dish> dishCaloriesComparator =
    Comparator.comparingInt(Dish::getCalories);
Optional<Dish> mostCalorieDish =
    menu.stream()
        .collect(maxBy(dishCaloriesComparator)); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_017.html#74ada264-780a-4160-af31-c8c0967efccf))


Vikram: [Demo of Collectors.maxBy. It takes a comparator which is produced using comparingInt, which in turn takes a lambda that returns an int.]


long howManyDishes = menu.stream().collect(Collectors.counting()); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_017.html#19110dc8-1ff6-42bd-8dab-f7990d281865))


Vikram: [Demonstrates the counting method.]


the groupingBy recipe says, “Make a Map whose keys are (currency) buckets and whose values are a list of elements in those buckets.” ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_017.html#aba1e5c9-e2ce-435f-b621-eefdb8d8323c))


Map<Currency, List<Transaction>> transactionsByCurrencies =
        transactions.stream().collect(groupingBy(Transaction::getCurrency)); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_017.html#ea71fd0a-e9c2-4c7d-aae2-a875972fdf1b))


Vikram: [In functional programming we specify what and not how. 
The above takes several lines of code in regular style of programming.]

## Chapter 3. Lambda expressions



Function<Integer, Apple> c2 = Apple::new;        1
Apple a2 = c2.apply(110);                        2 ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_013.html#78730722-0fce-4557-956a-5f392aef4f07))


Comparator describes a function descriptor with the signature (T, T) -> int. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_013.html#7679fcf3-9afd-4236-9e89-a88ea8b3d8c4))


Note that none of the functional interfaces allow for a checked exception to be thrown. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_013.html#ff3400f3-9193-4541-aa3c-a9a4a82e2f7d))


Vikram: [define your own if you need it]


To refresh a little: every Java type is either a reference type (for example, Byte, Integer, Object, List) or a primitive type (for example, int, double, byte, char). But generic parameters (for example, the T in Consumer<T>) can be bound only to reference types. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_013.html#cb99a6d8-f69e-41aa-91b4-07909e002e46))


Vikram: [A primitives cannot take the place of a generic parameter without some automatic operation. This automatic operation is called autoboxing.]


The signature of the abstract method of the functional interface describes the signature of the lambda expression. We call
         this abstract method a function descriptor. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_013.html#d22e020c-6eaa-4b66-9991-8e7fb739ad2d))


Vikram: [functional descriptor is the signature such as ()-{}]


Java 8 also added a specialized version of the functional interfaces we described earlier in order to avoid autoboxing operations when the inputs or outputs are primitives. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_013.html#79a4dedb-f2cd-47ba-af65-53e4d922cdb3))


Vikram: [This means that there is a IntPredicate to test primitive ints with signature (int i) -> boolean. similarly there are specialized interfaces for all primitives.]

## Chapter 4. Introducing streams



and map are two separate operations, they were merged into the same pass (compiler experts call this technique loop fusion). ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#838538f6-5661-4ccc-9c51-fb5c31150f47))


Stream operations that can be connected are called intermediate operations, and operations that close a stream are called terminal operations.  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#98382ac2-6aa7-463f-8cf2-6a93e9ab924e))


Streams library, by contrast, uses internal iteration ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#fa63bcb6-3db3-4f3b-b85a-89ba4f537547))


stream as a set of values spread out in time. In contrast, a collection is a set of values spread out in space ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#580ae7da-7f1e-4157-89d5-20dd6e67a45b))


Note that, similarly to iterators, a stream can be traversed only once. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#5f5c1941-fee3-40fb-97e5-e99a96df1b0d))


By contrast, a stream is a conceptually fixed data structure (you can’t add or remove elements from it) whose elements are computed on demand ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#a57c0cc5-bd90-4e97-ac6b-a68aa6e52d2d))


A collection is an in-memory data structure that holds all the values the data structure currently has—every element in the collection has to be computed before it can be added to the collection.  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#17f6e594-1373-4dc7-bf7a-717a8b570cbd))


Internal iteration— In contrast to collections, which are iterated explicitly using an iterator, stream operations do the iteration behind the scenes for you.  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#68ea36b0-1e1c-4fed-814f-d381a2f9051a))


First, what exactly is a stream? A short definition is “a sequence of elements from a source that supports data-processing operations.” ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_015.html#8db0a20c-c523-4f4c-96ac-546e6f078a59))

## Chapter 1. Java 8, 9, 10, and 11: what’s happening?



File[] hiddenFiles = new File(".").listFiles(File::isHidden); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#870c0dc4-57b0-4636-83e2-1b7d1233f2ea))


And this means using parallel processing—something Java wasn’t previously friendly to ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#6564539d-fb21-4c2e-8a4a-6be0f74f99fc))


It gives you a new concise way to express behavior parameterization ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#66025962-d6b1-43e1-9c10-b809fb2330a9))


Java 8 adds the ability to pass methods (your code) as arguments to other methods. Figure 1.3, based on figure 1.2, illustrates this idea. We also refer to this conceptually as behavior parameterization. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#e80ae6ed-2d31-492f-bd87-764607d8f322))


Vikram: [lambdas]


Its evolution (via the addition of new features) from Java 1.1 (1997) to Java 7 (2011) has been well managed. Java 8 was released in March 2014, Java 9 in September 2017, Java 10 in March 2018, and Java 11 planned for September 2018. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#75e4db21-09bb-49de-9b71-41f97d2f88a3))


Vikram: [1.1 in 97, 8 in 2014, 9 in 2017, 10 in 2018]


Multicore processors aren’t fully served by pre-Java-8 programming practice. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#7b0c3f72-4255-484f-87cd-4a17bfead14e))


Vikram: [Because, the only way to do it was  by using Threads and Synchronization which was error prone ]


Java 8 facilitates
            new programming styles to better exploit such computers. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#0623ed3b-3886-450e-be9c-d5c5b24a54b8))


Vikram: [Java 8 Streams allows programmers to  exploit multiple cores.  It provides functions  to process streams of data. If these functions do not modify state, these can be executed in parallel.]


Java 8 added default methods to support evolvable interfaces. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#5e445f83-3643-4182-b7ce-75c3c3c1c715))


Vikram: [Before Java 8, whenever a new method was added to an Interface, all programs that used that interface had to be recompiled. Now, in Java 8, a default implementation can be provided so the implementing classes will not have to be recompiled.]


Java 8 introduced the Optional<T> class that, if used consistently, can help you avoid null-pointer exceptions. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#5d949534-aeae-4cc4-8491-e1b1fab8ad32))


Vikram: [To avoid null-pointer exceptions, use Optional<T> class]


The key motivation for this is that you can now program in Java 8 at a higher level of abstraction, structuring your thoughts of turning a stream of this into a stream of that (similar to how you think when writing database queries) rather than one item at a time. Another advantage is that Java 8 can transparently run your pipeline of Stream operations on several CPU cores on disjoint parts of the input—this is parallelism almost for free instead of hard work using Threads.  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_011.html#fe4e77c4-b416-4dbc-b07c-ee8598b5017c))

## Chapter 17. Reactive programming



These techniques not only have the benefit of being cheaper than threads, but also have a major advantage from developers’ point of view: they raise the level of abstraction of implementing concurrent and asynchronous applications, allowing developers to concentrate on the business requirements instead of dealing with typical problems of low-level multithreading issues such as synchronization, race conditions, and deadlocks. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_031.html#800b4713-e9af-4fce-aa1f-0c3c4f14fe62))


Vikram: [reactive techniques]


The Reactive Manifesto (https://www.reactivemanifesto.org)—developed in 2013 and 2014 by Jonas Bonér, Dave Farley, Roland Kuhn, and Martin Thompson—formalized a set of core principles for developing reactive applications and systems. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_031.html#20ea50e5-451d-4925-aa4e-b1ecee9bbbb9))


Reactive programming addresses these issues by allowing you to process and combine streams of data items coming from different systems and sources in an asynchronous way ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_031.html#38794196-2418-4ea2-893c-2a112d9e3072))


Vikram: [The issues are : big data, expectation of faster response times, diversity of environments]

## Preface



We quickly realized that by combining our energy and diverse backgrounds we could deliver, not just a short book on Java 8 lambdas, but instead a book that, we hope, the Java community will still be reading in five or ten years. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_005.html#c228c751-7fa4-4b12-b757-10f2f92d8db0))


Vikram: [a book written for the long term and hopefully concentrates on concepts]

## Chapter 2. Passing code with behavior parameterization



But since Java 8 you can use a lambda expression, so the call to Thread would look like this:

Thread t = new Thread(() -> System.out.println("Hello world")); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_012.html#eb65a198-ec42-4a1e-a691-dd12bc23fb1f))


Vikram: [()->{}]


the behavior of the filterApples method depends on the code you pass to it via the ApplePredicate object. You’ve parameterized the behavior of the filterApples method! ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_012.html#b2bba6c1-2926-4c95-986a-445a4d1577bd))


Vikram: [The code is passed as a lambda. A lambda to filter green apples, another to filter heavy apples etc.]


predicate (a function that returns a boolean) ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_012.html#c90b1146-289f-4bba-960f-fc325abaea9f))


Vikram: [(T) -> boolean]


Behavior parameterization is a software development pattern that lets you handle frequent requirement changes. In a nutshell, it means taking a block
         of code and making it available without executing it. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_012.html#e5267c25-4f83-49db-a763-b94b4da7772d))


Vikram: [Similar to Ruby blocks. A block of code can be given to a method rather than just primitives and objects.]


Behavior parameterization is the ability for a method to take multiple different behaviors as parameters and use them internally to accomplish different behaviors. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_012.html#6ac95f2a-532a-4820-961e-f193b66686da))


Callable interface is used to model a task that returns a result.  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_012.html#deef1949-e718-4734-ad23-5281c5ec5aa6))

## Chapter 5. Working with streams



The methods takeWhile and dropWhile are more efficient than a filter when you know that the source is sorted ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#07c6f0d7-7562-46f3-940c-ee191bae5c44))


In comparison, our approach using iterate was purely immutable; you didn’t modify existing state but were creating new tuples at each iteration. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#76e88376-ca46-4c24-8f95-f4ca636116fc))


Vikram: [The approach using generate uses state of the previous call and is therefore mutable.]


The generate method on IntStream takes an IntSupplier instead of a Supplier<T>. For example, here’s how to generate an infinite stream of ones:

IntStream ones = IntStream.generate(() -> 1); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#16d54366-7a07-4c20-87c2-60280e2365b4))


Similarly to the method iterate, the method generate lets you produce an infinite stream of values computed on demand. But ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#645144a1-4549-4b45-bd27-66979ce1be94))


Vikram: [You have to supply a lambda that satisfies Supplier<T>.]


The iterate method takes an initial value, here 0, and a lambda (of type Unary-Operator<T>) to apply successively on each new value produced.  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#becbfe11-b364-4cc0-9127-7e8fd99b95af))


For example, a useful method is Files.lines, which returns a stream of lines as strings from a given file. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#cdb69c8f-e9c9-45fb-b549-400de1d94fd1))


You can create a stream from an array using the static method Arrays.stream, which takes an array as parameter ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#b98d0b96-7f3a-41a6-8115-83d37a95762e))


You can get an empty stream using the empty method as follows:

Stream<String> emptyStream = Stream.empty(); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#4aad5f6b-7d27-4436-b0f1-3b5da883ad53))


You can create a stream with explicit values by using the static method Stream.of, which can take any number of parameters ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#8947ece6-2543-4428-b773-5d006c7831ab))


IntStream intStream = menu.stream().mapToInt(Dish::getCalories); 1 Stream<Integer> stream = intStream.boxed(); 2 ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#39d92147-ed7f-420a-86e7-27e65580c0dd))


Vikram: [converting int stream back to general stream]


the map operation of an IntStream takes a lambda that takes an int and produces an int (an IntUnaryOperator).  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#b8b89536-0892-4051-ab36-a1b0a5d8e16e))


int calories = menu.stream() 1 .mapToInt(Dish::getCalories) 2 .sum(); ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#6f3fc3a8-08c4-40e6-a1b2-302a74b639f3))


Vikram: [mapToInt returns specialised int stream.]


Using the flatMap method has the effect of mapping each array not with a stream but with the contents of that stream.  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#399f5f69-e98b-4fcb-bef8-f84cfb3fc90d))


In a nutshell, the flatMap method lets you replace each value of a stream with another stream and then concatenates all the generated streams into a single stream. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#e520d0ab-750a-45bb-a102-aed6ff8fbca7))


Arrays.stream()that takes an array and produces a stream: ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#fa0cae63-19b6-4a30-92a1-8f834909bc8d))


that limit(n) and skip(n) are complementary ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#072be497-6810-495b-be1b-97c6e6acffa5))


Streams support the limit(n) method, which returns another stream that’s no longer than a given size.  ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#d074bcca-2114-4e84-9b5e-66f5674b179a))


it even works if there are an infinite number of remaining elements! ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#1906c5e1-b7a0-4961-b453-17631775e33b))


Vikram: [referring to dropWhile]


The dropWhile operation is the complement of takeWhile ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#b51eaff3-12ff-4cce-a586-38deacdcf98b))


The takeWhile operation is here to rescue you! It lets you slice any stream (even an infinite stream as you will learn later) using a predicate. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#ee4f51d4-c1f4-4bd3-bbaf-7969953ddf95))


Java 9 added two new methods that are useful for efficiently selecting elements in a stream: takeWhile and dropWhile. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#36fd3f64-93b7-49ce-9ed3-555e8b858ea8))


Streams API can work out several optimizations behind the scenes. In addition, using internal iteration, the Streams API can decide to run your code in parallel ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_016.html#57853e3b-6b44-4f2b-bc89-af015fd4cb41))

## About this book



The second edition of this book, Modern Java in Action: Lambdas, Streams, Functional and Reactive Programming, is written to get you over that initial hump of “sounds good in principle, but it’s all a bit new and unfamiliar” and into coding like a native ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_007.html#931ed7a3-fe3b-45e0-bc3e-ab57835fa0db))


But Java 8 can optimize operations on streams in a way that Java can’t do for collections—for example, it can group together several operations on the same stream so that the data is traversed only once instead of expensively traversing it multiple times. Even better, Java can automatically parallelize stream operations for you (unlike collections). ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_007.html#2d7f6880-039d-4f97-b1b3-93689eb6baef))


Vikram: [The benefit is that multiple operations can be done in a single pass and these can be parallelized.]


Thus, you can process streams that are too big to fit in your computer memory. ([link](https://learning.oreilly.com/library/view/-/9781617293566/kindle_split_007.html#4bd4406e-d88e-4f9b-b172-d4d16a6ba5b1))


Vikram: [One major use case where Stream processing is required.]

[> Home](../README.md)