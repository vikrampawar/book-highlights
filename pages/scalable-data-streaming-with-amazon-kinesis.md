# Scalable Data Streaming with Amazon Kinesis

[> Home](../README.md)
## Chapter 4: Kinesis Data Streams



Amazon API Gateway allows developers to easily create an HTTP endpoint to send records to KDS. API Gateway also has support for authentication to secure access to the endpoint. ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#2e5df14a-3914-4730-a902-9fd05580f23b))


The combination of the order guarantee and the failing record creates a scenario referred to as a poison pill. ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#aa4cee60-370a-4e0f-86f1-9624b8955762))


Utilizing an HTTP/2 WebSocket event stream, the message delivery from producer to consumer can be reduced to as little as 70 milliseconds ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#f5020712-16ec-4531-a677-83d6c8833a26))


With the GetRecords API, a consumer can request a batch of records of up to 10,000 records per shard ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#b6a96c9d-a90b-4133-a007-f3f032c668a4))


You can use the AWS Cloud9 environment, described in the Technical requirements section, to install the Linux-based Kinesis Agent. ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#b9984e63-b49e-4cde-af1e-089ba1ae143b))


You can check that the record is in the stream with the AWS CLI. The first command will get shard-id, and the second command will get ShardIterator. Lastly, we will execute get-records with the value of $SHARD_ITERATOR: ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#6735083c-1018-44d4-879c-49cc148a58b3))


When a record is written to the stream, the record cannot be altered or deleted. ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#2b2fbf35-d9cc-4248-bb68-6d49c2ea0de5))


Shards can be dynamically added or removed through resharding. The actual sharding process within a stream, such as the splitting and merging of data, is fully managed by Amazon KDS: https ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#6f3d0fcd-218a-4e4f-99d6-8afecbc21e25))


A shard provides an ingestion capacity of 1 MB/per second and 1,000 PUT records per second. The consumption capacity is 2 MB/per second and 2,000 GET records per second ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#eaf3ff2a-f7de-472f-a561-141b4f50692b))


The KCL will transparently track the record's sequence number in an Amazon DynamoDB table ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#c7544864-b031-4791-abd2-859ac8db7dfa))


Using an AWS Cloud9 development environment: As an alternative to setting these up in your local development environment, you can create an AWS Cloud9 development environment: https ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#f1f9d73f-ea4f-40dd-a667-55436c4b6e8e))


You want to use KDS when you need to deliver near real-time sub-second performance ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#36913ffd-7bcd-4628-834d-7017bc1b6270))


Amazon KDS is a managed, massively scalable, durable, and low latency real-time data streaming service used by many of the largest data pipelines in the cloud. ([link](https://learning.oreilly.com/library/view/-/9781800565401/B16742_04_Final_SK.xhtml#6108f0e2-7ca1-480c-b719-3d32d880f7e6))

[> Home](../README.md)