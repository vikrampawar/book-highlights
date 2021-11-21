# Event Streams in Action

[> Home](../README.md)
## Chapter 2. The unified log



This helps illustrate the fact that Kafka is serving as a kind of event stream database. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#58f85423-8adf-4e8c-9fe7-bad7ecacf436))


look at it another way, our event consists of two pieces of event metadata (namely, the event and the timestamp), and two business entities (the shopper and the product) ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#bdddd084-d9df-4b80-8e0f-f089234edf6a))


It is up to us to define the internal format of our events—a process we call modeling our events. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#9a87d82b-2753-46d9-ad67-bc5cd91edd23))


We need a way of formalizing this structure further, ideally into a data serialization format that is understandable by humans but also can be parsed by computers ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#015ec375-60b1-4321-bfee-b7473b0b8ea0))


Ordered means that the unified log gives each event in a shard a sequential ID number (sometimes called the offset) that uniquely identifies each message within the shard.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#46665f6d-7186-446b-8955-23dc61003a49))


To make it easier to work across a cluster of machines, unified logs tend to divide the events in a given event stream into multiple shards (sometimes referred to as partitions); ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#c5e077f6-0315-451f-928f-d5386464660e))


A unified log will replicate all events within the cluster.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#bd7cc046-a89c-4d40-a266-43d642451407))


The unified log is distributed because it lives across a cluster of individual machines. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#0f06488f-e764-4a90-889c-838db40ffe8f))


Kafka is designed to allow a single cluster to serve as the central data backbone for a large organization. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#58dde36b-86df-4ed7-b592-b089b058e2a8))


A unified log is an append-only, ordered, distributed log that allows a company to centralize its continuous event streams. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_011.html#c276919b-ae17-457f-8570-5ce440896046))

## Preface



We believe that reframing your business in terms of a continuous stream of events offers huge benefits.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_004.html#71d49cd7-4957-4703-9a5b-ef45521de951))

## Chapter 3. Event stream processing with Apache Kafka



The important thing to understand is that we are looking up the shopper’s IP address in MaxMind, and if it’s found, we are attaching the shopper’s country and city to the outgoing enriched event. If anything goes wrong on the way, we write that error message out to the “bad” topic. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_012.html#65286136-fb9c-4c34-bacd-deaef520eb90))


In multiple-event processing, we have to read multiple events from the event stream in order to generate some kind of output. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_012.html#d5b422c2-40c1-472e-a72d-542686bd37f5))


The first case, single-event processing, is straightforward to implement: we read the next event from our continuous event stream and apply some sort of transformation to it. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_012.html#ea785717-8968-4262-856b-1b0a1f708ecf))

## Chapter 4. Event stream processing with Amazon Kinesis



We can change that by temporarily creating an arbitrarily large file on our hard drive, using the fallocate command. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#085edef9-1058-440c-9f62-56700fcda4f1))


The AWS CLI and boto expose the exact same primitives for stream processing, which is unsurprising, given that the AWS CLI is built on boto!  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#a588f857-59a8-4c6a-8d4f-277523936b11))


import base64
base64.b64decode ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#99f2ae38-1e54-4ad5-b962-617b48e3576a))


We specified that the shard iterator should be of type TRIM_HORIZON. This is AWS jargon for the oldest events in the shard that have not yet been trimmed—expired for being too old. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#b5674b9b-e393-4a8f-8180-bf1ddef3bddc))


Before we can read events from our stream, we need to retrieve what Amazon calls a shard iterator for each shard in the stream.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#360cafb9-e017-437f-bd83-f53ab19a325a))


Apache Spark Streaming, which is Spark’s microbatch processing framework, ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#8b8dcb43-7376-4c81-8626-fbd2d091a274))


AWS Lambda is a fully managed stream processing platform running on a Node.js cluster.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#d26825cb-0f7c-4500-9241-2cb41ef53d6c))


Part of the reason that this code is so simple is that the AWS CLI tool that you configured earlier uses boto, the AWS SDK for Python, under the hood. Therefore, boto can access the AWS credentials that you set up earlier in the AWS CLI without any trouble. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#ccfb9eef-3779-4469-b3d2-2c1482b19f0e))


Figure 4.1. In push-based systems monitoring, an agent pushes metrics at regular intervals into a centralized system. By contrast, in pull-based architectures, the centralized system regularly scrapes metrics from endpoints available on the servers. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#9e14fc08-3484-4790-a463-dea137b58938))


For example, Zabbix and Prometheus are predominantly pull-based systems with some push support ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#da0a8aa4-f187-41eb-b80d-e82a6f7e7181))


This chapter introduces Amazon Kinesis (https://aws.amazon.com/kinesis/), a hosted unified log service available as part of Amazon Web Services. Developed internally at Amazon to solve its own challenges around log collection at scale, Kinesis has extremely similar semantics to Kafka ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_013.html#3e884f30-d2b5-4c56-ac86-695e0242399c))

## Chapter 1. Introducing event streams



Have different users consume different versions of our applications ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#3da7c8ed-fd37-40a7-87ff-635f8f146fcc))


If we can have multiple applications reading from the unified log, then it follows that we can also have multiple versions of the same application processing events from the unified log. This is hugely useful, as it allows us to hot swap our data processing applications—to upgrade our applications without taking them offline. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#80fc0ea6-505d-41ab-b552-f2f2bdc3375a))


Whenever the customer looks like they are about to abandon their shopping cart, pop up a coupon in their web browser to coax them into checking out. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#239af871-73ba-4320-891e-cd3e8b0d938d))


Together, the unified log plus Hadoop archive represent our single version of the truth.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#e6a99c0b-ac0e-4322-a691-8241085b52d7))


A unified log is an append-only log to which we write all events generated by our applications.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#378afc03-3a9e-4cfc-8f20-37d412f38d2b))


See figure 1.9 for an example of a hybrid-era architecture. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#2cff09e6-de68-420d-8411-ad55dca431be))


The nice thing about NSQ for demonstration purposes is that it is super simple to install and set up ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#7e97962a-62ac-4124-a82f-b802bcd6e84a))


Best practice says that you write the log events to disk as log files, and then use a log collection technology, such as Flume, Fluentd, Logstash, or Filebeat, to collect the log files from the individual servers and ingest them into a tool for systems monitoring or log-file analysis.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#eb5beed8-6f2e-41b4-91fb-38b598d84685))


Hoshi Ryokan is one of the oldest businesses in the world, having been founded in AD 718. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#3435698b-f1ea-416a-abd6-9d480b597a00))


Simply put, a continuous event stream is an unterminated succession of individual events, ordered by the point in time at which each event occurred.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#0bb54f95-a300-4a3e-844d-33bc675b814c))


Fortunately, the definition is simple: an event is anything that we can observe occurring at a particular point in time.  ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#7a18fdc0-bbbe-413e-b3a0-fe38c1f8d9d3))


 a new architectural pattern called the unified log promises to simplify things again. ([link](https://learning.oreilly.com/library/view/-/9781617292347/kindle_split_010.html#bb1ce527-a98d-4a9e-a7b5-f427e439cc80))

[> Home](../README.md)