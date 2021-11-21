# Programming AWS Lambda

[> Home](../README.md)
## 1. Introduction to Serverless, Amazon Web Services, and AWS Lambda



With a serverless service we expect the vendor to provide HA transparently for us. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch01.html#f0bbf490-7627-44ae-8ae2-67348b4d26c9))


Auth0 and Amazon’s Cognito. Both of these products allow mobile apps and web apps to have fully featured authentication and user management, but without a development team having to write or manage any of the code to implement those features. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch01.html#f1a9d94a-94e7-486b-86fc-77f87b3206b4))


Backend as a service (BaaS) allows us to replace server-side components that we code and/or manage ourselves with off-the-shelf services ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch01.html#c9fe5317-1d25-4733-82c1-377629d0b6cf))


Lambda implements the FaaS pattern by instantiating ephemeral, managed, Linux environments to host
each of our function instances. Lambda guarantees that only one event is processed per environment
at a time. At the time of writin ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch01.html#41abc3ce-426b-468a-8ed4-88ebf4d1948f))


the scaling flexibility of Lambda surpasses any other compute option within AWS. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch01.html#7c4b505c-9f30-4f34-9c1b-3ad66c7a2861))


We can build scheduled-task applications, similar to cron programs, using CloudWatch Scheduled Events as the trigger. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch01.html#a1ae375d-9a7f-43cb-9017-8863dd1d7f09))


We can build message-processing applications, using message buses like Simple Notification Service (SNS), Simple Queue Service (SQS), EventBridge, or Kinesis as the event source. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch01.html#e51cb9f7-c489-42a3-9430-e0dab5f71814))


In RestaurantsFunction we can, for example, make a call to a database—Amazon’s DynamoDB is a popular database to use with Lambda, partly due to the similar scaling capabilities of the two services. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch01.html#f93a01b9-0784-408b-a09c-179db39f81ff))


Vikram: [Amazon DynamoDB]

## Foreword



he software industry.
Theyâve greatly improved the productivity of millions of developers by eliminating many of the hassles, costs, and âundifferentiated heavy liftingâ of dealing with servers, from security pa ([link](https://learning.oreilly.com/library/view/-/9781492041047/foreword01.html#bb8f24a3-988a-4651-9a10-2d87cd252808))


Vikram: [AWS Lambda]

## 3. Programming AWS Lambda Functions



Most important, however, it specifies a principal, which is the identity that is allowed to assume the role. In this case, we’re allowing the Lambda service’s data plane (lambda.amazonaws.com) to assume this role ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch03.html#ef0b6a03-9f77-485f-b2b2-c313dfe226dd))


Vikram: [Start from here 11/10/2021]


That said, the principle of least privilege is not only applicable to preventing compromises. It’s also an effective means of limiting the “blast radius” of bugs in your application code. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch03.html#9ee78bde-32fe-4855-b2ab-334ba38663a7))


Fortunately, as AWS serverless developers, we have the good fortune to be able to use a different “flavor” of CloudFormation called the Serverless Application Model (SAM), which we used in Chapters 2 and 3. This is essentially a superset of CloudFormation, which allows us to use some special resource types and shortcuts to represent common serverless components and application architectures ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch03.html#c23a9524-c5da-4aeb-926f-79fcf5c181b5))


A set of AWS resources created from a CloudFormation template file is called a stack. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch03.html#71d12ec3-56c0-4073-8586-dcf378b24159))


Rather than manually interacting with AWS via the web console or CLI, we can declaratively specify our desired infrastructure in a JSON or YAML file and submit that file to AWS’s infrastructure-as-code service: CloudFormation ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch03.html#3528efef-16ee-4e60-bf79-077c79cc1e4b))


Vikram: [AWS Infrastructure as code tool is called CloudFormation]


First, the uberjar approach unpacks and then overlays libraries on top of each other in the target uberjar file. ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch03.html#b2c97a1c-817f-4653-83e3-ef50b1d4138e))


Vikram: [So if the same folder & file exists in another jar file, one of them will be overwritten.
Lambda runtime ignores the meta data in a jar a file.
The jar file contains build timestamps, so a binary is created everytime we run the build process.
We want the output to be the same if there are no code changes. 
This helps in caching and speeds up the processing.]

## 2. Getting Started with AWS Lambda



For example, to tear down the HelloWorldLambdaJava stack, run the following:

$ aws cloudformation delete-stack --stack-name HelloWorldLambdaJava ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch02.html#de823aea-e280-4cc8-9a40-2dd40ea2d1a8))


$ aws s3 mb s3://bucketname ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch02.html#db744f32-938a-4811-8a9c-930786a35ad8))


Vikram: [Create S3 bucket on command line]


A good way to quickly validate your AWS profile is to run the command aws iam get-user ([link](https://learning.oreilly.com/library/view/-/9781492041047/ch02.html#e507f646-b849-4579-a8ac-930bcf73d3e0))

[> Home](../README.md)