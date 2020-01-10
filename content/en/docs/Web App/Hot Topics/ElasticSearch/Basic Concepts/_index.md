---
title: "Basic concepts"
linkTitle: "Basic concepts"
weight: 1
description: >
  Elasticsearch - Basic concepts.
---

Elasticsearch is an Apache Lucene-based search server. It was developed by Shay Banon and published in 2010. It is now maintained by Elasticsearch BV. Its latest version is 7.0.0.

Elasticsearch is a real-time distributed and open source full-text search and analytics engine. It is accessible from RESTful web service interface and uses schema less JSON (JavaScript Object Notation) documents to store data. It is built on Java programming language and hence Elasticsearch can run on different platforms. It enables users to explore very large amount of data at very high speed.

## General Features

- Elasticsearch is scalable up to petabytes of structured and unstructured data.
- Elasticsearch can be used as a replacement of document stores like MongoDB and RavenDB.
- Elasticsearch uses denormalization to improve the search performance.
- Elasticsearch is one of the popular enterprise search engines, and is currently being used by many big organizations like Wikipedia, The Guardian, StackOverflow, GitHub etc.
- Elasticsearch is an open source and available under the Apache license version 2.0.

## Key Concepts

### Node

It refers to a single running instance of Elasticsearch. Single physical and virtual server accommodates multiple nodes depending upon the capabilities of their physical resources like RAM, storage and processing power.

### Cluster

It is a collection of one or more nodes. Cluster provides collective indexing and search capabilities across all the nodes for entire data.

### Index

It is a collection of different type of documents and their properties. Index also uses the concept of shards to improve the performance. For example, a set of document contains data of a social networking application.

### Document

### Shard

### Replicas

## Comparison between Elasticsearch, RDBMS and NoSQL Database

<table class="table-2">
  <colgroup>
    <col class="thirty" />
    <col class="thirty" />
    <col class="thirty" />
  </colgroup>

  <tr>
    <th>Elasticsearch</th>
    <th>RDBMS</th>
    <th>NoSQL</th>
  </tr>

  <tr>
    <td>Cluster</td>
    <td>Database</td>
    <td>Database</td>
  </tr>
  <tr>
    <td>Shard</td>
    <td>Shard</td>
    <td>--</td>
  </tr>
  <tr>
    <td>Index</td>
    <td>Table</td>
    <td>Collection</td>
  </tr>
  <tr>
    <td>Field</td>
    <td>Column</td>
    <td>Field</td>
  </tr>
  <tr>
    <td>Document</td>
    <td>Row</td>
    <td>Document</td>
  </tr>  
</table>