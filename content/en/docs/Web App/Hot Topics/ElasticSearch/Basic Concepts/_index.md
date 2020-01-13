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

It is a collection of fields in a specific manner defined in JSON format. Every document belongs to a type and resides inside an index. Every document is associated with a unique identifier called the UID.

### Shard

Indexes are horizontally subdivided into shards. This means each shard contains all the properties of document but contains less number of JSON objects than index. The horizontal separation makes shard an independent node, which can be store in any node. Primary shard is the original horizontal part of an index and then these primary shards are replicated into replica shards.

### Replicas

Elasticsearch allows a user to create replicas of their indexes and shards. Replication not only helps in increasing the availability of data in case of failure, but also improves the performance of searching by carrying out a parallel search operation in these replicas.

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

## Advantages

- Elasticsearch is developed on Java, which makes it compatible on almost every platform.
- Elasticsearch is real time, in other words after one second the added document is searchable in this engine
- Elasticsearch is distributed, which makes it easy to scale and integrate in any big organization.
- Creating full backups are easy by using the concept of gateway, which is present in Elasticsearch. 
- Handling multi-tenancy is very easy in Elasticsearch when compared to Apache Solr.
- Elasticsearch uses JSON objects as responses, which makes it possible to invoke the Elasticsearch server with a large number of different programming languages.
- Elasticsearch supports almost every document type except those that do not support text rendering.

## Disadvantages

- Elasticsearch does not have multi-language support in terms of handling request and response data (only possible in JSON) unlike in Apache Solr, where it is possible in CSV, XML and JSON formats.
- Occasionally, Elasticsearch has a problem of Split brain situations.