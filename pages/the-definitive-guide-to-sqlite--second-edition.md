# The Definitive Guide to SQLite, Second Edition

[> Home](../README.md)
## CHAPTER 3: SQL for SQLite



That is the purpose of having, a predicate that you apply to the result of group by. It filters the groups from group by in the same way that the where clause filters rows from the from clause.  ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#a6d14afb-2ab9-4b2f-ad3a-460cfa4a84d0))


When group by is used, the select clause applies aggregates to each group separately, rather than the entire result as a whole. Since aggregates produce a single value from a group of values, they collapse these groups of rows into single rows. ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#47489c7d-2af9-49fb-81ae-cc7b7489ae6a))


Operationally, group by sits in between the where clause and the select clause. group by takes the output of where and splits it into groups of rows that share a common value (or values) for a specific column (or columns) ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#ed74ac61-c522-439f-bd58-93dbd9280614))


Aggregates operate within the select clause. They compute their values on the rows selected by the where clause—not from all rows selected by the from clause. The select command filters first and then aggregates. ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#6c2695a3-bb91-4ab2-a960-c1fe9f67850d))


Notice that limit and offset are dead last in the operational pipeline. One common misconception of limit/offset is that it speeds up a query by limiting the number of rows that must be collected by the where clause. ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#309d7a60-acba-435e-b8b8-cc049adda407))


You can limit the size and particular range of the result using the limit and offset keywords. limit specifies the maximum number of records to return. offset specifies the number of records to skip.  ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#292a1314-1b82-44eb-8560-5a7dccdc8315))


As stated earlier, where—a restriction—is a filter. The argument of where is a logical predicate ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#ee306bcd-e596-446a-b54e-423dcde4b7f0))


SQLite applies the where clause to each row of the relation produced by the from clause (R1). ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#47c74601-ca0e-49c9-8837-9a2a4680aa51))


In SQLite, the best way to think of the select command is as a pipeline that  ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter03.html#cc10239d-c746-4241-9828-317a4aa5e5fe))

## CHAPTER 1: Introducing SQLite



SQLite has coarse-grained locking, which allows multiple readers but only one writer at a time. Writers exclusively lock the database during writes, and no one else has access during that time.  ([link](https://learning.oreilly.com/library/view/-/9781430232254/Chapter01.html#e13a084a-e0c6-41e4-a048-35f7f96eb60e))

[> Home](../README.md)