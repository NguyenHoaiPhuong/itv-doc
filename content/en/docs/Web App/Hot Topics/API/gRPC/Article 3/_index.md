---
title: "Building High Performance APIs In Go Using gRPC And Protocol Buffers"
linkTitle: "Using gRPC And Protocol Buffers"
weight: 3
description: >
  Using gRPC And Protocol Buffers.
---

APIs are backbone of modern applications. APIs are powering the backend for web client and mobile client applications, and also used for communication between applications regardless of technology and platform. When you think about building web based APIs, you typically choose RESTful APIs along with JSON as the standard for interchanging data between applications. This approach is fine and mobile client applications can easily consume these JSON based RESTful APIs. Now we’re building applications for the era of cloud-native applications where our Microservices should be able for massive scale and performance is very critical. And we definitely need a **high performance communication** mechanism for communicating between various Microservices. Then the big question is whether JSON based APIs provide high performance and scalability power which is required for modern applications. Is JSON really a fast data format for exchanging data between applications? Is RESTful architecture capable of building complex APIs?. Can we easily build a bidirectional stream APIs with RESTful architecture?. The HTTP/2 protocol provides lot of capability than its previous version, thus we need to leverage those capabilities when building next-generation APIs. Then enter to gRPC and protocol buffers.

## Introduction to Protocol Buffers



## References

https://medium.com/@shijuvar/building-high-performance-apis-in-go-using-grpc-and-protocol-buffers-2eda5b80771b

https://viblo.asia/p/grpc-va-ung-dung-no-trong-microservices-ORNZqo8N50n

https://grpc.io/docs/quickstart/go/