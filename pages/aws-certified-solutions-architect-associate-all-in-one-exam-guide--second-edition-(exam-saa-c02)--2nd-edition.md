# AWS Certified Solutions Architect Associate All-in-One Exam Guide, Second Edition (Exam SAA-C02), 2nd Edition

[> Home](../README.md)
## Introduction



When you study the chapters, you will find that AWS has a shared responsibility model; this means AWS is responsible for the security of the cloud, and the customer is responsible for the security in the cloud ([link](https://learning.oreilly.com/library/view/-/9781260470192/intro.xhtml#e4046d46-10e0-42f0-858c-7945193eacc3))


Vikram: [Shared responsibility model]

## Chapter 2 Storage on AWS



S3 is going to do the partitioning based on the key prefix. ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#31cc0db4-35f7-4da1-a5fe-7d629d7ee368))


Amazon S3 does not support object locking ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#430998e3-ca2f-40ca-a596-f40cf29b5ccc))


updates to a single key are atomic.  ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#7f7910fd-065c-4218-8b42-4f2f058225d7))


This provides read-after-write consistency. ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#5bc2ec78-c88f-4220-9b37-ffb2fcb31897))


The S3 service is intended to be a “write once, read many” use case ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#0c1846a6-c7cc-4cdb-a72f-fbc3f9b12658))


The name of the bucket must be unique, which means you cannot have two buckets with the same name even across multiple regions ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#14461d8a-db47-4ad4-806a-b9dfc88ca032))


Amazon S3 can be used as your big data object store ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#5e10d3de-01db-4a5e-a431-e9a72056b25b))


These contents can be distributed either directly from S3 or via Amazon CloudFront. ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#1af19dda-66b4-4fc9-a0ce-65423ee7ef6a))


cross-region replication ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#4344ac67-7f7b-4cc9-b064-da869ebf6f8d))


For example, if you put a *.html file in S3, you can access it from a web browser without the need for a web server. This is a great option for getting read-only information. ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#0bc4feec-fff7-4311-8e90-d98f789dc66d))


For S3 Standard, S3 Standard-Infrequent Access, and S3 Glacier storage classes, data is distributed in three copies for each file between multiple availability zones (AZs) within an AWS region. As a result, the data cannot be destroyed by a disaster in one AZ. S3 also provides versioning capacity; as a result, you can further protect your data against human error. ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#f4fc8a3a-81cb-4e13-92ce-11a9fa3d8e03))


Amazon S3 is designed to sustain concurrent data loss in two facilities. ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#11dcd518-7204-4714-b839-3b590ad222d1))


It is fundamentally different from other file repositories because it does not have a file system. All objects are stored in a flat namespace organized by buckets ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#a2bc4654-a335-4c0b-b95b-91b520760e35))


 Amazon S3 is an object store and is the backbone for many other services used at Amazon ([link](https://learning.oreilly.com/library/view/-/9781260470192/ch2.xhtml#fdea800b-5508-418f-a3c4-7a3eea28b698))

[> Home](../README.md)