---
title: "Populate"
linkTitle: "Populate"
weight: 3
description: >
  Elasticsearch - Populate.
---

In this chapter, let us learn how to add some index, mapping and data to Elasticsearch. Note that some of this data will be used in the examples explained in this tutorial.

## Create Index

You can use the following command to create an index:

```
PUT http://localhost:9200/school
```

### Response

If the index is created, you can see the following output:

```
{"acknowledged": true}
```

## Add data

Elasticsearch will store the documents we add to the index as shown in the following code. The documents are given some IDs which are used in identifying the document.

### Request Body

Request #1:

```
POST http://localhost:9200/school/_doc/10
{
  "name":"Saint Paul School",
  "description":"ICSE Afiliation",
  "street":"Dawarka",
  "city":"Delhi",
  "state":"Delhi",
  "zip":"110075",
  "location":[28.5733056, 77.0122136],
  "fees":5000,
  "tags":["Good Faculty", "Great Sports"],
  "rating":"4.5"
}
```

Request #2:

```
POST http://localhost:9200/school/_doc/16
{
  "name":"Crescent School",
  "description":"State Board Affiliation",
  "street":"Tonk Road",
  "city":"Jaipur",
  "state":"RJ",
  "zip":"176114",
  "location":[26.8535922,75.7923988],
  "fees":2500,
  "tags":["Well equipped labs"],
  "rating":"4.5"
}
```

### Response

Response #1:

```
{
    "_index": "school",
    "_type": "_doc",
    "_id": "10",
    "_version": 1,
    "result": "created",
    "_shards": {
        "total": 2,
        "successful": 1,
        "failed": 0
    },
    "_seq_no": 0,
    "_primary_term": 1
}
```

Response #2:

```
{
    "_index": "school",
    "_type": "_doc",
    "_id": "16",
    "_version": 1,
    "result": "created",
    "_shards": {
        "total": 2,
        "successful": 1,
        "failed": 0
    },
    "_seq_no": 1,
    "_primary_term": 1
}
```