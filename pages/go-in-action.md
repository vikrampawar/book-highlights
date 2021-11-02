# Go in Action

[> Home](../README.md)
## Chapter 2. Go quick-start



On line 20, we use the built-in function make to create an unbuffered channel.  ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_010.html#090f948d-8114-4a94-b4fe-f69037873d1d))


 slice is a reference type that implements a dynamic array. ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_010.html#03a0f66b-f961-491a-9bf4-d839169f27b6))


In Go, all variables are initialized to their zero value. For numeric types, that value is 0; for strings it’s an empty string; for Booleans it’s false; and for pointers, the zero value is nil. ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_010.html#334141e9-2fb8-4329-8bc2-3b64f5c635d5))


In Go, identifiers are either exported or unexported from a package. ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_010.html#7bca9517-a832-40bc-bfea-b546c4a2a4a3))


The compiler will always look for the packages you import at the locations referenced by the GOROOT and GOPATH environment variables ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_010.html#95352753-d753-425d-95cc-a2d0904f64f9))


This is a technique in Go to allow initialization from a package to occur, even if you don’t directly use any identifiers from the package.  ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_010.html#e4053bb0-c4df-47be-adbb-b43dfb8f0f91))

## Chapter 1. Introducing Go



In contrast, a Go interface typically represents just a single action ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#f6273537-8e4a-40c6-ade2-235b409115ea))


Interfaces allow you to express the behavior of a type. ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#603638d6-c851-405e-9d1a-2319abaeeeec))


Inheritance versus composition ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#03472db0-9b38-4616-b043-925abf4a8747))


Go developers simply embed types to reuse functionality in a design pattern called composition ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#a7681ea4-862f-42e5-83cd-b36d71ad3b7b))


Go provides a flexible hierarchy-free type system that enables code reuse with minimal refactoring overhead. ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#2593f05e-b0e8-4a25-9ea3-af1e4c88263e))


Channels are data structures that enable safe data communication between goroutines.  ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#97f92b23-8b16-4531-babe-ed15fdece425))


As stated before, goroutines have minimal overhead, so it isn’t uncommon to spawn tens of thousands of them ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#6d90380e-dc61-46d1-8c66-fbaa57ec4f57))


The trade-off is that dynamic languages don’t offer the type safety that static languages do and often need a comprehensive test suite to avoid discovering incorrect type bugs at runtime. ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#ff96b10f-6082-4208-976d-a994bbbce3ca))


When you build a Go program, the compiler only needs to look at the libraries that you directly include, rather than traversing the dependencies of all the libraries that are included in the entire dependency chain like Java, C, and C++.  ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#22079630-ca06-4934-9892-8eda08f61034))


Because of Go’s built-in concurrency features, your software will scale to use the resources available without forcing you to use special threading libraries.  ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#526d1100-09e2-41a7-86de-f912cbbcc66f))


Go rethinks the traditional object-oriented development you might be used to, while still providing an efficient means for code reuse ([link](https://learning.oreilly.com/library/view/-/9781617291784/kindle_split_009.html#6e416ccc-36dd-451a-b99d-df61831fa58f))

[> Home](../README.md)