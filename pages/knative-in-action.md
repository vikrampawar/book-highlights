# Knative in Action

[> Home](../README.md)
## 3 Configurations and Revisions



Knative lets you set minimum and maximum levels for CPU share and bytes of RAM. This is another case of directly exposing the underlying Kubernetes feature, which is called resources. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#fe712264-30ca-48cf-ba93-f63f0c866411))


It modifies any probes so that their port value is the same as the port value of the container itself, which will be the same as the PORT environment variable that’s injected. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#87f2e53c-5ece-454e-8ceb-190d7bc21d9d))


This leads to different treatment for each kind of probe. When liveness checks fail, Kubernetes eventually kills the container and relaunches it someplace else. When readiness checks fail, Kubernetes prevents network traffic from reaching the container ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#d501b01e-2803-4b49-bb20-689abc61c0d7))


Software that’s otherwise alive might not be ready for traffic. For example, during a long startup, the software is alive, but it’s not ready ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#ea55ddf1-9210-4890-94f6-656d38d02678))


Remember that Knative Serving spits out a new Revision every time you touch the template. That includes environment variables, which can be used to change system behavior. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#80c514d3-6b22-40b2-a2fc-9e12b7f45ccd))


The names of labels and annotations follow a pattern: <subject area>.knative.dev/ <subject> ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#ddb6594b-6892-4fd9-8c15-587d2540290d))


changing the template causes Revisions to be created. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#4db7215c-8b56-4fe0-8f44-f2b7fe0fd93c))


A Configuration is a definition of your software. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#cd6a3f52-68d1-4334-8460-9e33db74416a))


Revisions are created only when Configurations are changed or created. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/03.htm#d384dd45-d767-46d1-9764-6526201aff65))

## 1 Introduction



Kubernetes explicitly models its architecture on feedback control loops and provides infrastructure to enable the easy development of a variety of controllers for different purposes. Kubernetes then uses hierarchical control to layer responsibilities: Pods can be supervised by ReplicaSets that are supervised by Deployments. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#eb49903f-453e-4c83-a84d-568052eaffb0))


This should be recognizable as architectural layering according to the Single Responsibility Principle ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#fa15a6ec-6c69-458b-af74-5132a33c494f))


Blocking is still blocking, but blocking on threads is faster than blocking on HTTP.  ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#1f0744b4-6a23-4aa1-acb1-619aa9801708))


Each Service combines a Configuration and a Route.  ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#6e647244-dd19-4378-b3c5-20ff473a79b1))


These are snapshots of a Configuration. Each time that you change a Configuration, Knative first creates a Revision ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#6e4aa812-669c-40b7-95d0-e9f86a81e7ec))


As a developer, Knative gives you three basic types of document you can use to express your desires: Configuration, Revision, and Route. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#cdab4beb-c9f7-4325-8009-8441d562941d))


Each Trigger represents an interest in some set of events and where to forward these. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#b3a37d0f-14cb-4700-b6d6-6d26e8d22653))


Vikram: [Is it the same as subscription?]


NOTE Inventory, capacity, and time really are the only options for buffering variability ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#af15cdda-0113-4d09-a2eb-5167a8d0692d))


This layer creates a firmer boundary between the developer and the platform, allowing the developer to concentrate on the software they are directly responsible for. ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#c2b7827c-abb2-4c19-856b-e7b474ffd44c))


Knative builds on the toolbox Kubernetes provides, but it also sets out to achieve a level of consistency, simplicity, and ease of use that brings Kubernetes much closer to meeting the Test’s high standard. Knative is a machine ([link](https://learning.oreilly.com/library/view/-/9781617296642/OEBPS/Text/01.htm#dd2621f0-0980-423f-9858-8e4959750111))

[> Home](../README.md)