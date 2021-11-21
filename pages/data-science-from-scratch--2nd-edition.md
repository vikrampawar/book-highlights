# Data Science from Scratch, 2nd Edition

[> Home](../README.md)
## 2. A Crash Course in Python



The asterisk (*) performs argument unpacking, which uses the elements of pairs as individual arguments to zip ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#42967eed-0aae-421b-aa43-5a7928981c46))


The zip function transforms multiple iterables into a single iterable of tuples of corresponding function: ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#b7f2f2dd-3cf6-4458-b828-a728ed64a047))


The random module actually produces pseudorandom (that is, deterministic) numbers based on an internal state that you can set with random.seed if you want to get reproducible results: ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#bbdb76a7-0c00-49d0-b2bc-eef403797609))


Not infrequently, when we’re iterating over a list or a generator we’ll want not just the values but also their indices. For this common case Python provides an enumerate function, which turns values into pairs (index, value): ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#d9efb8f3-f6a8-43b8-82d2-9cc9135dceb3))


Often all we need is to iterate over the collection using for and in. In this case we can create generators, which can be iterated over just like lists but generate their values lazily on demand. ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#038e9a9f-24f1-45d8-b5c5-2fe0820a7ecc))


A slice can take a third argument to indicate its stride, which can be negative:

every_third = x[::3]               ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#1ef9d9f5-a191-466f-b1a1-c8ab38cdb300))


IPython has a magic function called %paste, which correctly pastes whatever is on your clipboard, whitespace and all. This alone is a good reason to use IPython. ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#73faae47-ce7f-4bfe-8ce6-452e0f1b0ec0))


Now that you have your environment, it’s worth installing IPython, which is a full-featured Python shell: ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#e07a2d3b-5fd0-437e-a3ad-a8f9a889c4f8))


As a matter of good discipline, you should always work in a virtual environment, and never using the “base” Python installation ([link](https://learning.oreilly.com/library/view/-/9781492041122/ch02.html#a75d6803-4f5d-4781-89b0-0f96567a2a7e))

[> Home](../README.md)