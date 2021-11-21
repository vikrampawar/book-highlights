# Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation, Video Enhanced Edition

[> Home](../README.md)
## Chapter 1. The Problem of Delivering Software



This is known as the Deming cycle: plan, do, study, act. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#03fcfb9f-6016-4b1b-9561-0c3b48ec3f40))


Ultimately the team succeeds or fails as a team, not as individuals.  ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#6dd59508-4d8a-435a-b8ab-9be5a219f1a4))


If creating application documentation is painful, do it as you develop new features instead of leaving it to the end. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#c5f9b680-a7e9-4f88-8aa6-f492cc3e99a0))


It should be possible for a new team member to sit down at a new workstation, check out the project’s revision control repository, and run a single command to build and deploy the application to any accessible environment, including the local development workstation. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#ce695a96-5e68-48be-a299-65aec881315d))


The repeatability and reliability derive from two principles: automate almost everything, and keep everything you need to build, deploy, test, and release your application in version control. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#5f70d711-8279-482f-8a3a-c6105c778458))


Create a Repeatable, Reliable Process for Releasing Software ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#57b91614-ad98-49ef-9221-b2fc52c4c540))


Every time a change is committed to version control, the expectation is that it will pass all of its tests, produce working code, and can be released into production. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#ae0f9bc7-98c3-44f6-b51a-6463e55b9281))


Continuous integration detects any change that breaks the system or does not fulfill the customer’s acceptance criteria at the time it is introduced into the system. Teams then fix the problem as soon as it occurs (this is the first rule of continuous integration ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#f87d964c-e776-435c-b25b-89f838ffa2c7))


In software, when something is painful, the way to reduce the pain is to do it more frequently, not less.  ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#9b209999-1473-4b62-ae57-d73511ee27de))


As long as this is true they will be surrounded with a lot of ceremony and nervousness. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#777ac098-1ef3-44a8-87d4-787240c7fb67))


There are rarely checks of any kind applied to configuration information, particularly if that configuration information is typed directly into some console. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#8c5a7f71-3d71-4408-9384-3ffb931a9d0d))


One of the key principles of the deployment pipeline is that it is a pull system—it allows testers, operations or support personnel to self-service the version of the application they want into the environment of their choice. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#90ca1a30-3f8c-4235-8903-cfb2a6495da4))


This executable code should be the same executable code that is deployed into every environment, whether it is a testing environment or a production environment ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#02ed26a3-a448-4bbe-9f9a-a79987c94bae))


The practice of building and testing your application on every check-in is known as continuous integration; ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#69522709-28ab-46cf-b7ca-d87f083aca6c))


If releases are frequent, the delta between releases will be small.  ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#9d2f89b6-9cfa-4db3-8b5f-aeba6736f1a4))


Our software should be fit for its purpose. Quality does not equal perfection—as Voltaire said, “The perfect is the enemy of the good,” ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#2448bb23-cba6-436a-b145-ac4b4059083c))


 Software release can—and should—be a low-risk, frequent, cheap, rapid, and predictable process.  ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#65179213-c7fe-409d-980c-b0718ea11e95))


Indeed it should not be possible to make manual changes to testing, staging, and production environments. The only way to make changes to these environments should be through an automated process. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#2d849aa4-18f1-4953-b219-08b426e54e7e))


All aspects of each of your testing, staging, and production environments, specifically the configuration of any third-party elements of your system, should be applied from version control through an automated process. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#c8424fd4-cf42-4544-b62a-f0dcea889c07))


Different members of a cluster behave differently ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#56b224ea-1354-455f-a1f6-4afcdc7d4f7a))


We are test addicts, and the extensive use of continuous integration and continuous deployment, as a means of testing both our software and our deployment process, is a cornerstone of the approach that we describe. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#25875799-e999-49eb-ae74-6b1a5e6e6153))


One of the principles that we describe in this book is to use the same script to deploy to every environment. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#7f545452-953b-47b5-8d3b-38b267b7a24b))


An automated deployment process is cheap and easy to test. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#d6a3dc91-468b-4479-a62c-f9461301708a))


Performing manual deployments is boring and repetitive and yet needs significant degree of expertise. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#2cbb0c3d-5f15-4a4d-955d-3baed1f57ed9))


There should be two tasks for a human being to perform to deploy software into a development, test, or production environment: to pick the version and environment and to press the “deploy” button.  ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch01.html#0e96d205-7849-4872-8468-bbb86c6368ca))

## Preface



We also employed continuous integration, using a CruiseControl.rb server that ran dblatex to produce a PDF of the book every time one of us committed a change ([link](https://learning.oreilly.com/library/view/-/9780321670250/pr03.html#47391e5c-28ce-43de-b052-f45234f711e7))


The time from deciding that you need to make a change to having it in production is known as the cycle time, and it is a vital metric for any project. ([link](https://learning.oreilly.com/library/view/-/9780321670250/pr03.html#37f486e0-5b4d-4300-adcb-fc29d1cefc7a))


Software release should be a fast, repeatable process. These days, many companies are putting out multiple releases in a day.  ([link](https://learning.oreilly.com/library/view/-/9780321670250/pr03.html#df07fcef-5768-47cc-9bf9-4f4664dbb059))

## Chapter 2. Configuration Management



You should also include a link to the identifier in your project management tool for the feature or bug you’re working on.  ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch02.html#65a8eba0-4863-46e3-8404-f6143f77966a))


Finally, storing the binary output of the build breaks the idea of being able to identify a single version of your repository for each application version because there may be two commits for the same version, one for source code and another for the binaries. ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch02.html#d7383185-5949-4649-bed4-f625b47ab48d))


One thing that we don’t recommend that you keep in version control is the binary output of your application’s compilation.  ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch02.html#3ed1a339-6a38-4b3c-8d03-dbf536365305))


You can then store whole environments, including base operating systems with configuration baselines applied, as virtual images for an even higher level of assurance and deployment simplicity ([link](https://learning.oreilly.com/library/view/-/9780321670250/ch02.html#d643e273-e3ed-4564-adcc-1eaddc2b00f0))

[> Home](../README.md)