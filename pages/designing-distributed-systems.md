# Designing Distributed Systems

[> Home](../README.md)
## 2. The Sidecar Pattern



The sidecar pattern is a single-node pattern made up of two containers. The first is the application container. It contains the core logic for the application. Without this container, the application would not exist. In addition to the application container, there is a sidecar container. The role of the sidecar is to augment and improve the application container, often without the application container’s knowledge. ([link](https://learning.oreilly.com/library/view/-/9781491983638/ch02.html#a31e4257-594e-42e3-a86a-76d5a2d16b95))

[> Home](../README.md)