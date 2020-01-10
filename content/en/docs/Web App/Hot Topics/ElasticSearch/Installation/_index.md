---
title: "Installation"
linkTitle: "Installation"
weight: 2
description: >
  Elasticsearch Installation.
---

## Download and install archive for Linux

The Linux archive for Elasticsearch v7.5.1 can be downloaded and installed as follows:

```
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.5.1-linux-x86_64.tar.gz
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.5.1-linux-x86_64.tar.gz.sha512
shasum -a 512 -c elasticsearch-7.5.1-linux-x86_64.tar.gz.sha512 
tar -xzf elasticsearch-7.5.1-linux-x86_64.tar.gz
cd elasticsearch-7.5.1/
```

## Running Elasticsearch from command line

Elasticsearch can be started from the command line as follows:

```
./bin/elasticsearch
```

By default, Elasticsearch runs in the foreground, prints its logs to the standard output (stdout), and can be stopped by pressing `Ctrl-C`.

## Checking that Elasticsearch is running

You can test that your Elasticsearch node is running by sending an HTTP request to port 9200 on localhost:

```
GET http://localhost:9200
```

or simply type below address in any web browsers.

```
http://localhost:9200/
```

If Elasticsearch is working, the response of above request will be

```
{
  "name" : "aston-martin",
  "cluster_name" : "elasticsearch",
  "cluster_uuid" : "jTD66tpeQHWwO_tqbVgENg",
  "version" : {
    "number" : "7.5.1",
    "build_flavor" : "default",
    "build_type" : "tar",
    "build_hash" : "3ae9ac9a93c95bd0cdc054951cf95d88e1e18d96",
    "build_date" : "2019-12-16T22:57:37.835892Z",
    "build_snapshot" : false,
    "lucene_version" : "8.3.0",
    "minimum_wire_compatibility_version" : "6.8.0",
    "minimum_index_compatibility_version" : "6.0.0-beta1"
  },
  "tagline" : "You Know, for Search"
}
```

## Running as a daemon

To run `Elasticsearch` as a daemon, specify `-d` on the command line, and record the process ID in a file using the -p option:

```
./bin/elasticsearch -d -p pid
```

Log messages can be found in the `$ES_HOME/logs/` directory.

To shut down Elasticsearch, kill the process ID recorded in the pid file:

```
pkill -F pid
```

## Configuring Elasticsearch on the command line

Elasticsearch loads its configuration from the `$ES_HOME/config/elasticsearch.yml` file by default. The format of this config file is explained in [*Configuring Elasticsearch*](https://www.elastic.co/guide/en/elasticsearch/reference/current/settings.html).

Any settings that can be specified in the config file can also be specified on the command line, using the `-E` syntax as follows:

```
./bin/elasticsearch -d -Ecluster.name=my_cluster -Enode.name=node_1
```

## References

This document is strictly followed the guideline indicated [here](https://www.elastic.co/guide/en/elasticsearch/reference/current/install-elasticsearch.html).