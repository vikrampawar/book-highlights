# Using SQLite

[> Home](../README.md)
## Not the Best Choice



The concurrency protection offered by SQLite depends on file locks to protect against data loss. This model allows multiple database connections to access a database at the same time, but the whole database file must be locked in an exclusive mode to make any changes. As a result, write transactions are serialized across all database connections, limiting the overall transaction rate. ([link](https://learning.oreilly.com/library/view/-/9781449394592/ch02s08.html#127e5d26-9ca9-4b25-b424-c59480e9fcfc))


Depending on the size and complexity of your updates, SQLite might be able to handle a few hundred transactions per minute from different processes or threads.  ([link](https://learning.oreilly.com/library/view/-/9781449394592/ch02s08.html#b07b073b-de82-4df7-adbf-aab4cb620178))

[> Home](../README.md)