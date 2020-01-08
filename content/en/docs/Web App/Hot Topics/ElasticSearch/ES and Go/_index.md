---
title: "Search Service with Go and Elasticsearch"
linkTitle: "Search Service with Go and Elasticsearch"
weight: 100
description: >
  How to Build a Search Service with Go and Elasticsearch.
---

This article shows how to build a simple search service in Go using <a href="https://www.elastic.co/">Elasticsearch</a>. The service will run inside a local Docker machine along side Elasticsearch instance. If you're only interested in the source code, you can find it on <a href="https://github.com/tinrab/go-elasticsearch-example">GitHub</a>.

## Getting started

If you haven't already, install `Docker`, `Go` and `golang/dep` dependency management tool.

Create a directory for your project inside $GOPATH.

## Configure services

Create `docker-compose.yaml` file with the following contents.

```
version: '3.5'
services:
  search_api:
    container_name: 'search_api'
    build: './search-api'
    restart: 'on-failure'
    ports:
      - '8080:8080'
    depends_on:
      - elasticsearch
  elasticsearch:
    container_name: 'elasticsearch'
    image: 'docker.elastic.co/elasticsearch/elasticsearch:7.5.1'
    ports:
      - '9200:9200'
```

This defines two services. The `search_api` service will host your Go app on port 8080, while `elasticsearch` will run the official <a href="https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html">Elasticsearch</a> Docker image.

Create a subdirectory called `search-api` and initialize the project with `dep`.

```
mkdir search-api
cd search-api
dep init
```

Write the Dockerfile for `search_api` service inside `search-api` directory.

```
FROM golang:1.13.3-alpine3.10

RUN adduser --disabled-password --gecos '' api
USER api

WORKDIR /go/src/app
COPY . .

RUN go install -v ./...

CMD [ "app" ]
```

## Connecting to Elasticsearch

Create an entry point `main.go` file inside `search-api` directory.

```
package main

import (
  "encoding/json"
  "fmt"
  "log"
  "net/http"
  "strconv"
  "time"

  "github.com/gin-gonic/gin"
  "github.com/olivere/elastic"
  "github.com/teris-io/shortid"
)
```

## References

https://outcrawl.com/go-elastic-search-service

https://viblo.asia/p/elasticsearch-la-gi-1Je5E8RmlnL

https://levanphu.info/tim-hieu-ve-elasctic-search

https://github.com/elastic/elasticsearch/issues/25067

https://github.com/docker/kitematic/issues/5029