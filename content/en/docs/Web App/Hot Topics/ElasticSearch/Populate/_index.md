---
title: "Populate"
linkTitle: "Populate"
weight: 1
description: >
  Elasticsearch - Populate.
---

In this chapter, let us learn how to add some index, mapping and data to Elasticsearch. Note that some of this data will be used in the examples explained in this tutorial.

## Create Index

You can use the following command to create an index:

```
PUT localhost:9200/school
```

### Response

If the index is created, you can see the following output:

```
{"acknowledged": true}
```

## Add data

Elasticsearch will store the documents we add to the index as shown in the following code. The documents are given some IDs which are used in identifying the document.