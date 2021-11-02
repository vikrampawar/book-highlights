# Building Microservices with Go

[> Home](../README.md)
## Context



The Context type implements a safe method for accessing request-scoped data that is safe to use simultaneously by multiple Go routines ([link](https://learning.oreilly.com/library/view/-/9781786468666/a6451c7d-520d-4b9c-ac5a-5b441c7417e2.xhtml#272b978d-e4fc-4bfe-bc4a-03d8c830669d))

## Marshalling Go structs to JSON



 are decoding our struct into a byte array and then writing that to the response stream, this does not seem to be particularly efficient and in fact it is not. ([link](https://learning.oreilly.com/library/view/-/9781786468666/4f3ac8c1-a27f-4d1d-819d-2a16e51bb7b3.xhtml#8c90af0e-8d3c-447c-8cc6-091f93a9ba40))

## Unmarshalling JSON to Go structs



The JSON that has been sent with the request is accessible in the Body field. Body implements the interface io.ReadCloser as a stream and does not return a []byte or a string. ([link](https://learning.oreilly.com/library/view/-/9781786468666/b324fa53-6456-4edc-b110-389fc71f7477.xhtml#f78106d0-53ae-4ffb-921e-1fe8c5bc1f22))

## TimeoutHandler



you use the golint command that comes with the standard package then this will report areas of your code which do not conform to the standards ([link](https://learning.oreilly.com/library/view/-/9781786468666/24564c52-185f-419c-bf74-5cdd3d2ed0d5.xhtml#3fab5821-99ba-49c6-8701-382d7bd67256))

## Building a simple web server with net/http



Since ListenAndServe blocks if the server starts correctly we will never exit on a successful start. ([link](https://learning.oreilly.com/library/view/-/9781786468666/3866dcff-baea-4c9d-9d3c-9a10c438f5a0.xhtml#cf0d69f8-48d4-4b14-a54c-9169fb734dda))

[> Home](../README.md)