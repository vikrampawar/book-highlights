# The Go Programming Language

[> Home](../README.md)
## 5.2 Recursion



In contrast, typical Go implementations use variable-size stacks that start small and grow as needed up to a limit on the order of a gigabyte. This lets us use recursion safely and without worrying about overflow. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_043.html#2d2239b3-a111-47a8-b4d3-0ec5d7e696df))

## 5.8 Deferred Function Calls



Because an anonymous function can access its enclosing function’s variables, including named results, a deferred anonymous function can observe the function’s results. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_049.html#522fe225-d855-4727-b978-3467fbadc9bf))


The defer statement can also be used to pair “on entry” and “on exit” actions when debugging a complex function ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_049.html#daad3384-5d86-4886-899a-23e25d6fa96c))


defer statement is often used with paired operations like open and close, connect and disconnect, or lock and unlock to ensure that resources are released in all cases, no matter how complex the control flow. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_049.html#b599e6e6-6c54-4066-a09a-f7ab6b940150))

## 7.6 Sorting with sort.Interface



Each element is indirect, a pointer to a Track. Although the code below would work if we stored the Tracks directly, the sort function will swap many pairs of elements, so it will run faster if each element is a pointer, which is a single machine word, instead of an entire Track, which might be eight words or more. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_065.html#18348fbb-817c-4662-9888-dae2d5e836fa))

## 7.3 Interface Satisfaction



a value of type T does not possess all the methods that a *T pointer does, and as a result it might satisfy fewer interfaces. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_062.html#cef19f20-d594-410f-9d49-66d9a1758945))


Go programmers often say that a concrete type “is a” particular interface type, meaning that it satisfies the interface. For example, a *bytes.Buffer is an io.Writer; an *os.File is an io.ReadWriter. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_062.html#1e820ecf-d11d-4fb3-9268-59b389fdec95))

## 7.1 Interfaces as Contracts



This freedom to substitute one type for another that satisfies the same interface is called substitutability,  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_060.html#cca6d327-3cb4-42be-b0ec-3d746f51057b))

## 5.4 Errors



Errors are thus an important part of a package’s API or an application’s user interface, and failure is just one of several expected behaviors. This is the approach Go takes to error handling. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_045.html#b51ebd92-89b6-4d92-8147-fdb79f69f25b))


Indeed, it’s when the most reliable operations fail unexpectedly that we most need to know why. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_045.html#93dbd99d-e2e0-44cb-ae4f-3da8b65d5593))

## 7.14 Example: Token-Based XML Decoding



The encoding/xml package also provides a lower-level token-based API for decoding XML. In the token-based style, the parser consumes the input and produces a stream of tokens, primarily of four kinds—StartElement, EndElement, CharData, and Comment—each being a concrete type in the encoding/xml package. Each call to (*xml.Decoder).Token returns a token. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_073.html#d5d3c292-c284-4484-9ebe-7aac69fc9760))

## 5.6 Anonymous Functions



The problem of iteration variable capture is most often encountered when using the go statement (Chapter 8) or with defer (which we will see in a moment) since both may delay the execution of a function value until after the loop has finished.  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#f54cd81f-042c-4993-a53e-9fa117e7065c))


for _, dir := range tempDirs() {
    dir := dir // declares inner dir, initialized to outer dir
    // ... ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#66d1ee75-7928-4794-8534-246cdc447003))


dir := d               // NOTE: necessary! ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#e90f0c06-23dd-4442-bd7a-c37f1994b549))


the argument “f(item)...” causes all the items in the list returned by f to be appended to the worklist. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#bb58f376-dca6-4d42-998f-638e44182c51))


 topoSort example showed a depth-first traversal; for our web crawler, we’ll use breadth-first traversal, at least initially. In Chapter 8, we’ll explore concurrent traversal. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#06a4516f-7f37-484a-993c-4616c7f7d300))


Instead of appending the raw href attribute value to the links slice, this version parses it as a URL relative to the base URL of the document, resp.Request.UR ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#4047f235-7c05-4e62-8963-02c8b8bc513e))


Here again we see an example where the lifetime of a variable is not determined by its scope ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#1bc304a8-75b4-435f-a6b5-9df0933a7501))


The squares example demonstrates that function values are not just code but can have state. The anonymous inner function can access and update the local variables of the enclosing function squares ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#f44645c0-76c9-450f-b8fb-b806325365d5))


More importantly, functions defined in this way have access to the entire lexical environment, so the inner function can refer to variables from the enclosing function ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_047.html#2a7e8336-094c-41a1-9928-d222750159b0))

## 8.6 Example: Concurrent Web Crawler



Also notice that the initial send of the command-line arguments to the worklist must run in its own goroutine to avoid deadlock, a stuck situation in which both the main goroutine and a crawler goroutine attempt to send to each other while neither is receiving. An alternative solution would be to use a buffered channel ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_081.html#c587f3d4-3bf8-4157-a6ab-44a90a2115bd))


we’ll make it concurrent so that independent calls to crawl can exploit the I/O parallelism available in the web. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_081.html#a0678591-f166-41b2-885f-31b1089dac7a))

## 4.2 Slices



So, if you need to test whether a slice is empty, use len(s) == 0, not s == nil ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#53d4e9a3-b7fe-4aaf-ae28-39456c9b452e))


The zero value of a slice type is nil ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#9cd4cc6b-07b2-4746-a689-3ab39c85d87d))


, unlike array elements, the elements of a slice are indirect, making it possible for a slice to contain itself ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#d360393e-9615-4000-90fa-f149c3439a79))


bytes.Equal function for comparing two slices of bytes ([]byte) ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#d9d5f0de-4b68-4a5e-806f-7ae253df0d07))


Unlike arrays, slices are not comparable, so we cannot use == to test whether two slices contain the same elements.  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#9aafa990-cb94-45d7-be3e-14edea308032))


A slice literal looks like an array literal, a sequence of values separated by commas and surrounded by braces, but the size is not given.  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#dce2f121-4a3b-4787-97b5-ca400be02826))


A simple way to rotate a slice left by n elements is to apply the reverse function three times, first to the leading n elements, then to the remaining elements, and finally to the whole slice. (To rotate to the right, make the third call first.) ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#c2c8a04b-0fe1-4fc8-974c-92103d515804))


In other words, copying a slice creates an alias (§2.3.2) for the underlying array. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#1e221f4a-8732-47f8-b0ff-3eceec6a3810))


The slice operator s[i:j], where 0 ≤ i ≤ j ≤ cap(s), creates a new slice that refers to elements i through j-1 of the sequence s, which may be an array variable, a pointer to an array, or another slice ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#c5914c04-72b9-405d-a54d-2a6b649f8b38))


The slice operator s[i:j], where 0 ≤ i ≤ j ≤ cap(s), creates a new slice that refers to elements i through j-1 of the sequence s, which may be an array variable, ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_036.html#2fa91342-fee8-4c72-9c5c-f390d92ad024))


Vikram: [s can be a pointer]

## 5.5 Function Values



Using a function value, we can separate the logic for tree traversal from the logic for the action to be applied to each node, letting us reuse the traversal with different actions. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_046.html#158eb5e5-5881-4934-90fa-76f7a1ad4641))

## 8.1 Goroutines



The main function then returns. When this happens, all goroutines are abruptly terminated and the program exits. Other than by returning from main or exiting the program, there is no programmatic way for one goroutine to stop another, but as we will see later, there are ways to communicate with a goroutine to request that it stop itself. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_076.html#38d17817-42dc-44b6-8f57-48ba6a17f624))


In Go, each concurrently executing activity is called a goroutine.  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_076.html#f4b5bdcf-77d5-417a-9437-0de4213c1c12))

## 5.3 Multiple Return Values



This is called a bare return ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_044.html#f8d0c6c9-5dce-4f51-8ef5-c4772235e4f4))

## 7.5 Interface Values



The problem is that although a nil *bytes.Buffer pointer has the methods needed to satisfy the interface, it doesn’t satisfy the behavioral requirements of the interface. In particular, the call violates the implicit precondition of (*bytes.Buffer).Write that its receiver is not nil, so assigning the nil pointer to the interface was a mistake. The solution is to change the type of buf in main to io.Writer, thereby avoiding the assignment of the dysfunctional value to the interface in the first place: ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_064.html#e4f4d986-2312-420a-ab51-45995aff9a61))


When main calls f, it assigns a nil pointer of type *bytes.Buffer to the out parameter, so the dynamic value of out is nil. However, its dynamic type is *bytes.Buffer, meaning that out is a non-nil interface containing a nil pointer value (Figure 7.5), so the defensive check out != nil is still true. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_064.html#f7f8768a-2fe2-4127-a253-5ea2cd92ee7d))


When handling errors, or during debugging, it is often helpful to report the dynamic type of an interface value. For that, we use the fmt package’s %T verb: ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_064.html#6a0814fd-bebd-4287-b1a3-17a52987877d))

## 7.7 The http.Handler Interface



The behavior of its ServeHTTP method is to call the underlying function. HandlerFunc is thus an adapter that lets a function value satisfy an interface, where the function and the interface’s sole method have the same signature. In effect, this trick lets a single type such as database satisfy the http.Handler interface several different ways: once through its list method, once through its price method, and so on. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_066.html#4ab3712d-5326-4511-bec8-4deb6c3fe9c6))


w.WriteHeader(http.StatusNotFound); this must be done before writing any text to w. (Incidentally, http.ResponseWriter is another interface. It augments io.Writer with methods for sending HTTP response headers.) ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_066.html#db8e5284-5f9b-486b-905b-315e5457b33b))

## 3.5 Strings



fmt.Println(strconv.FormatInt(int64(x), 2)) // "1111011" ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#825937f6-556f-431a-ad3f-71ad4721f777))


In addition to conversions between strings, runes, and bytes, it’s often necessary to convert between numeric values and their string representations. This is done with functions from the strconv package. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#18e7d4f1-8d84-485a-8f95-73806b6f5a61))


The bytes package provides the Buffer type for efficient manipulation of byte slices ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#5330db47-a49c-4472-b0bd-49f60f8a2460))


A string contains an array of bytes that, once created, is immutable. By contrast, the elements of a byte slice can be freely modified. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#7aa28088-4b70-4ee4-87b8-ca1ce3415b07))


The path and path/filepath packages provide a more general set of functions for manipulating hierarchical names ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#1a14676c-2417-4c83-bc25-0aac8f62c181))


The strconv package provides functions for converting boolean, integer, and floating-point values to and from their string representations, and functions for quoting and unquoting strings. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#a2c532fd-fb99-43ae-a1db-719ad35d951c))


Because strings are immutable, building up strings incrementally can involve a lot of allocation and copying. In such cases, it’s more efficient to use the bytes.Buffer type, which we’ll show in a moment. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#d8fb2620-87a1-4ee0-912c-439db19fc5bc))


The verb % x in the first Printf inserts a space between each pair of hex digits. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#8df6b823-3d85-4dab-861c-932e6d7cf718))


A []rune conversion applied to a UTF-8-encoded string returns the sequence of Unicode code points ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#dbe3d2de-2f07-4774-afdf-b8b6c5d83bcd))


unexpected input byte, it generates a special Unicode replacement character, 'uFFFD', which is usually printed as a white question mark inside a black ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#139942f5-5720-4505-bb24-13ca081735d7))


 range loop, when applied to a string, performs UTF-8 decoding implicitly.  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#447bed7a-d037-4c44-a0dd-a9c75e9e9f5c))


A rune whose value is less than 256 may be written with a single hexadecimal escape, such as 'x41' for 'A', but for higher values, a u or U escape must be used. Consequently, 'xe4xb8x96' is not a legal rune literal, even though those three bytes are a valid UTF-8 encoding of a single code point. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#636aab1b-dcda-4ea8-bff5-e834eacf337b))


Vikram: [So until 256 the hexadecimal number is the same for the bytes and the unicode code point (rune). A character has a number in the unicode code point table. This number represented in hex will be 'uhhhh', but when encoded will have a different bytes sequence
 which will be 'xhhh'. So the number of bytes and the actual values will be different.]


UTF-8 was invented by Ken Thompson and Rob Pike, two of the creators of Go,  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#6f3bd060-a295-4326-884d-6027a3d76f0f))


UTF-8 is a variable-length encoding of Unicode code points as bytes.  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#9a9cbbce-cb33-4300-b327-9b73014aa260))


The natural data type to hold a single rune is int32, and that’s what Go uses; it has the synonym rune for precisely this purpose ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#e089c00f-c175-4b03-8e7e-5110615426d0))


Unicode code point or, in Go terminology, a rune. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#d5a68271-87e6-4900-8ede-e88fdf77f606))


A raw string literal is written `...`, using backquotes instead of double quotes. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#92f6614b-0e29-482a-bb92-a6e24c3e6b2f))


Immutability means that it is safe for two copies of a string to share the same underlying memory, making it cheap to copy strings of any length. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#04961a7b-d317-4959-8f4a-ad46f8aa05a2))


Since strings are immutable, constructions that try to modify a string’s data in place are not allowed: ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_032.html#9f63530f-4157-4b52-88c5-79c325cfdfff))

## 8.5 Looping in Parallel



Problems like this that consist entirely of subproblems that are completely independent of each other are described as embarrassingly parallel. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_080.html#c614441a-6c77-4658-b3ed-1d53a234d167))

## 5.1 Function Declarations



Arguments are passed by value, so the function receives a copy of each argument; modifications to the copy do not affect the caller. However, if the argument contains some kind of reference, like a pointer, slice, map, function, or channel, then the caller may be affected by any modifications the function makes to variables indirectly referred to by the argument. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_042.html#b20aabdb-f9f4-412c-b12c-7f73ec7cfee9))

## 7.2 Interface Types



The syntax used above, which resembles struct embedding, lets us name another interface as a shorthand for writing out all of its methods. This is called embedding an interface ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_061.html#39bd319b-fc8d-4646-906f-b2f458ae16ee))

## 7.10 Type Assertions



A type assertion is an operation applied to an interface value. Syntactically, it looks like x.(T), where x is an expression of an interface type and T is a type, called the “asserted” type. A type assertion checks that the dynamic type of its operand matches the asserted type ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_069.html#bc700106-6599-4561-a206-3429b73d0a4b))

## 7.15 A Few Words of Advice



. Not everything need be an object; standalone functions have their place, as do unencapsulated data types ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_074.html#871c2ece-2276-4bf7-9cb9-dc8de8d14f33))


Interfaces are only needed when there are two or more concrete types that must be dealt with in a uniform way. ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_074.html#1d22e867-a31a-4fa8-a0c3-b79ce98739ee))

## 8. Goroutines and Channels



This chapter presents goroutines and channels, which support communicating sequential processes or CSP, a model of concurrency in which values are passed between independent activities (goroutines) but variables are for the most part confined to a single activity.  ([link](https://learning.oreilly.com/library/view/-/9780134190570/ebook_split_075.html#444fc06a-3894-49e3-a4e2-452e16c65e57))

[> Home](../README.md)