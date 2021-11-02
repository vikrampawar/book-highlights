# Classic Computer Science Problems in Java

[> Home](../README.md)
## 2 Search problems



Amazingly, the algorithm for a breadth-first search is identical to the algorithm for a depth-first search, with the frontier changed from a stack to a queue. ([link](https://learning.oreilly.com/library/view/-/9781617297601/OEBPS/Text/ch02_Kopec3.htm#7c7f1dd0-71c8-486c-98d6-da941b97cc07))


The depth-first search algorithm relies on a data structure known as a stack. ([link](https://learning.oreilly.com/library/view/-/9781617297601/OEBPS/Text/ch02_Kopec3.htm#594948e6-4389-479d-a52b-0155f92579f2))

## 1 Small problems



We could break the recursive case into three steps:

Move the upper n-1 discs from tower A to B (the temporary tower), using C as the step in between.

Move the single lowest disc from A to C.

Move the n-1 discs from tower B to C, using A as the step in between. ([link](https://learning.oreilly.com/library/view/-/9781617297601/OEBPS/Text/ch01_Kopec3.htm#e76a59e2-cbf3-465e-ad82-904db0934cb6))


If the bits of two numbers are combined using XOR, a helpful property is that the product can be recombined with either of the operands to produce the other operand:
  C = A ^ B
A = C ^ B
B = C ^ A ([link](https://learning.oreilly.com/library/view/-/9781617297601/OEBPS/Text/ch01_Kopec3.htm#c541678c-ea4f-43bf-8a4c-d54622756403))


Vikram: [1, 0 => 1.  So 0, 0 => 1 and 1,1=>0
lly 0,1 => 1
0,0 => 0.  Cleary 0,0 => 0 and 0,0 =>0
1,1=>0.     So 0,1 => 1 

]


The two bits are composed together in the variable lastBits. lastBits is made by shifting the first bit back one place, and then ORing (| operator) the result with the second bit. When a value is shifted, using the << operator, the space left behind is replaced with 0s. An OR says, “If either of these bits are a 1, put a 1.” Therefor ORing secondBit with a 0 will always just result in the value of secondBit. L ([link](https://learning.oreilly.com/library/view/-/9781617297601/OEBPS/Text/ch01_Kopec3.htm#61304dc0-a353-45b2-9376-82c8b8f32525))


Memoization is a technique in which you store the results of computational tasks when they are completed so that when you need them again, you can look them up instead of needing to compute them a second (or millionth) time (see figure 1.4). ([link](https://learning.oreilly.com/library/view/-/9781617297601/OEBPS/Text/ch01_Kopec3.htm#65d76970-952b-4ef8-823d-1b8c039e3504))


The reason for the infinite recursion is that we never specified a base case. In a recursive function, a base case serves as a stopping point. ([link](https://learning.oreilly.com/library/view/-/9781617297601/OEBPS/Text/ch01_Kopec3.htm#9d83a712-1f86-4b4f-a1eb-070e71a58253))

[> Home](../README.md)