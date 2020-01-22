---
title: "API Conventions"
linkTitle: "API Conventions"
weight: 5
description: >
  Elasticsearch - API Conventions.
---

Application Programming Interface (API) in web is a group of function calls or other programming instructions to access the software component in that particular web application. For example, Facebook API helps a developer to create applications by accessing data or other functionalities from Facebook; it can be date of birth or status update.

Elasticsearch provides a REST API, which is accessed by JSON over HTTP. Elasticsearch uses some conventions which we shall discuss now.

## Multiple Indices

Most of the operations, mainly searching and other operations, in APIs are for one or more than one indices. This helps the user to search in multiple places or all the available data by just executing a query once. Many different notations are used to perform operations in multiple indices. We will discuss a few of them here in this chapter.

## Comma Separated Notation

```
POST http://localhost:9200/index1,index2,index3/_search
```

