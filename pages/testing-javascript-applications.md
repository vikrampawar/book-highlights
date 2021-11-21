# Testing JavaScript Applications

[> Home](../README.md)
## 2 What to test and when?



At the moment, the most popular tools for UI testing are Cypress, TestCafe, and Selenium. It’s possible to use these tools to make a browser interact with your application by using JavaScript to control them ([link](https://learning.oreilly.com/library/view/-/9781617297915/OEBPS/Text/02.htm#8b239806-ace1-4656-8ae3-b0924ce30aa9))


The web framework you are going to use to build your API is Koa. It is simple, effective, and small. It’s ideal for what we want to do in this book: focus on tests. Because Koa doesn’t ship with a router, you will also need to install koa-router to map different requests to different actions. ([link](https://learning.oreilly.com/library/view/-/9781617297915/OEBPS/Text/02.htm#21bff255-aadd-4c41-b523-dcb9cfe9a00b))


Because tests for RESTful APIs require only a client capable of performing HTTP requests and inspecting responses, we can write them within Jest. In these examples, you will use isomorphic-fetch to perform HTTP requests. ([link](https://learning.oreilly.com/library/view/-/9781617297915/OEBPS/Text/02.htm#3bfb0f70-643c-460d-be6a-0a5b49878816))

## 1 An introduction to automated testing



The only useful kind of test is a test that will fail when your application doesn’t work. ([link](https://learning.oreilly.com/library/view/-/9781617297915/OEBPS/Text/01.htm#6079374c-8645-49c2-b4ca-541aa7f91a5d))


Vikram: [Highligted this, so I remember I was reading this today]

[> Home](../README.md)