# Mastering Regular Expressions, 3rd Edition

[> Home](../README.md)
## 1: Introduction to Regular Expressions



The sequence ⌈.⌋ is described as an escaped period or escaped dot, and you can do this with all the normal metacharacters, except in a character-class ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#f0491668-73f6-406a-9268-c8d11ad5a2d9))


This yields ⌈<([A-Za-z]+)•+1>⌋. ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#ee713340-9436-4cc3-918f-d9323b8a8b1c))


This is called the interval quantifier. For example, ⌈···{3,12}⌋ matches up to 12 times if possible, but settles for three. One might use ⌈[a-zA-Z]{1,5}⌋ to match a US stock ticker (from one to five letters).  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#9a7fe29d-eda5-40d4-b1e3-8ba78949c50f))


Let’s look at matching color or colour. Since they are the same except that one has a u and the other doesn’t, we can use ⌈colou?r⌋ to match either.  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#4e6c485a-50c6-4569-9a9a-fed783ec136f))


The rules about which characters are and aren’t metacharacters (and exactly what they mean) are different inside a character class. For example, dot is a metacharacter outside of a class, but not within one. Conversely, a dash is a metacharacter within a class (usually), but not outside. Moreover, a caret has one meaning outside, another if specified inside a class immediately after the opening [, and a third if given elsewhere in the class. ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#433844e0-5ef0-45f5-bff8-e29defaf40be))


For example, ⌈Bob⌋ and ⌈Robert⌋ are separate expressions, but ⌈Bob|Robert⌋ is one expression that matches either. When combined this way, the subexpressions are called alternatives. ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#804da5d4-a1c1-4cc5-a55f-a922732824e5))


Probably the easiest metacharacters to understand are ⌈^⌋ (caret) and ⌈$⌋ (dollar), which represent the start and end, respectively, of the line of text as it is being checked.  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#1088a315-1089-439e-bed4-bfd6af8720e1))


Ther egular-expression construct ⌈[···]⌋, usually called a character class, lets you list the characters you want to allow at that point in the match.  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#da1e0927-dbca-4912-8988-ca7105d228a0))


Within a character class, the character-class metacharacter ‘-’ (dash) indicates a range of characters: ⌈<H[1-6]>⌋ is identical to the previous example.  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#13298b78-99da-4e90-ab90-d5e842be20c3))


Negated character classes
If you use ⌈[^···]⌋ instead of ⌈[···]⌋, the class matches any character that isn’t listed. For example, ⌈[^1-6]⌋ matches a character that’s not 1 through  6 ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#5fe25641-afb2-43d3-8841-c8614b3fa467))


In ⌈03[-./]l9[-./]76⌋, the dots are not metacharacters because they are within a character class. (Remember, the list of metacharacters and their meanings are different inside and outside of character classes.) The dashes are also not class metacharacters in this case because each is the first thing after [ or [^. ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#bfcf1f34-d893-4755-9570-ff84c21dc204))


Vikram: [- within character class ie [] has two meanings. as first character, it has literal meaning, other places it denotes range. outside of character class it has literal meaning.]


Remember, a negated character class means “match a character that’s not listed” and not “don’t match what is listed.” ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#c462db07-9025-4bed-bbfa-f98e430f254b))


Vikram: [example q[^u]]


egrep’s command-line option “-i” tells it to do a case-insensitive match.  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#2aed83f2-85c9-4f6f-a8f6-13b75a13bee4))


We can accomplish this by using parentheses to “constrain” the alternation:

⌈^(From|Subject|Date):•⌋ ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#7031cb12-c465-4660-8887-a90fe2e07a00))


The expression ⌈<cat>⌋ literally means “match if we can find a start-of-word position, followed immediately by c·a·t, followed immediately by an end-of-word position.”  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#c7d9c849-bbc4-4c3c-8408-52ec472f94f0))


Note that ⌈<⌋ and ⌈>⌋ alone are not metacharacters — when combined with a backslash, the sequences become special. This is why I called them “metasequences.” ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#4014581a-7d94-4711-a988-3ac9f0cdf742))


The expression ⌈<cat>⌋ literally means “match if we can find a start-of-word position, followed immediately by c·a·t, followed immediately by an end-of-word position.” More naturally, it means “find the word cat.” ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#6b978aa2-7078-4cdd-8fe4-15841fe09cbf))


We can accomplish this by using parentheses to “constrain” the alternation:

⌈^(From|Subject|Date):•⌋ ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#f4594a93-2514-47ae-9660-e216c685c4da))


A very convenient metacharacter is ⌈|⌋, which means “or.” It allows you to combine multiple expressions into a single expression that matches any of the individual ones. For example, ⌈Bob⌋ and ⌈Robert⌋ are separate expressions, but ⌈Bob|Robert⌋ is one expression that matches either. When combined this way, the subexpressions are called alternatives. ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#b1932ad1-8b2a-4e48-809c-ca7db69b8ace))


Remember, a negated character class means “match a character that’s not listed” and not “don’t match what is listed.” These might seem the same, but the Iraq example shows the subtle difference. ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#41c1d945-0d62-463a-86de-1d942bd53798))


Just as the English word “wind” can mean different things depending on the context (sometimes a strong breeze, sometimes what you do to a clock), so can a metacharacter.  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#fb96968b-99b6-4431-82e4-d0cab6230743))


The rules regarding which metacharacters are supported (and what they do) are completely different inside and outside of character classes. ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#5347783e-57cf-4202-9e2d-1e847d42b16a))


the only special characters within the class in ⌈[0-9A-Z_!.?]⌋ are the two dashes). ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#3120022d-6912-4fe4-a814-e5ac11605a15))


Within a character class, the character-class metacharacter ‘-’ (dash) indicates a range of characters: ⌈<H[1-6]>⌋ is identical to the previous example. ⌈[0-9]⌋ and ⌈[a-z]⌋ are common shorthands for classes to match digits and English lowercase letters, respectively.  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#a8db3e7f-4c63-4e81-a89d-03f8232b3978))


The contents of a class is a list of characters that can match at that point, so the implication is “or.” ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#7ea6a9b8-b62c-4347-88f2-e59184ea663e))


Ther egular-expression construct ⌈[···]⌋, usually called a character class, lets you list the characters you want to allow at that point in the match.  ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#b084b2d3-95e7-41f0-9082-e0c907f3ea77))


⌈^cat⌋ matches if you have the beginning of a line, followed immediately by c, followed immediately by a, followed immediately by t ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#ae85a900-0bd9-4fd4-8359-83ad575e085a))


Similarly, ⌈cat$⌋ finds c·a·t only at the end of the line, such as a line ending with scat ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#183ac838-e963-432d-863c-76efab4d393a))


Just as there is a difference between playing a musical piece well and making music, there is a difference between knowing about regular expressions and really understanding them ([link](https://learning.oreilly.com/library/view/-/0596528124/ch01.html#97b331e0-87b8-4e0f-a836-d54fb1eb9d34))

[> Home](../README.md)