---
title: "ORDER BY"
linkTitle: "ORDER BY"
weight: 2
description: >
  PostgreSQL ORDER BY
---

{{% pageinfo %}}
**Summary**: in this tutorial, you will learn how to sort the result set returned from the `SELECT` statement by using the PostgreSQL `ORDER BY` clause.
{{% /pageinfo %}}

## Introduction

When you query data from a table, PostgreSQL returns the rows in an **unspecified** order. To sort the result set, you use the `ORDER BY` clause in the `SELECT` statement.

The `ORDER BY` clause allows you to sort rows returned from a `SELECT` statement in ascending or descending order based on the specified criteria.

The following illustrates the syntax of the `ORDER BY` clause:

```
SELECT
  column_1,
  column_2
FROM
  table_name
ORDER BY
  column_1 [ASC | DESC],
  column_2 [ASC | DESC];
```

In this syntax:

* First, specify a column or an expression that you want to sort in the `ORDER BY` clause. If you sort the result set based on multiple columns or expressions, you use a comma to separate two columns or expressions.
* Second, use `ASC` to sort the result set in ascending order and `DESC` to sort the result set in descending order. If skip the `ASC` or `DESC` option, the `ORDER BY` uses `ASC` by default.

## Examples

### Sort rows by one column

```
SELECT
  first_name,
  last_name
FROM
  customer
ORDER BY
  first_name ASC;
```

```
SELECT
  first_name,
  last_name
FROM
  customer
ORDER BY
  first_name;
```

```
SELECT
      first_name,
      last_name
FROM
      customer
ORDER BY
      last_name DESC;
```

### Sort rows by multiple columns

```
SELECT
  first_name,
  last_name
FROM
  customer
ORDER BY
  first_name ASC,
  last_name DESC;
```

### Sort rows by expressions

```
SELECT 
  first_name,
  LENGTH(first_name) len
FROM
  customer
ORDER BY 
  LENGTH(first_name) DESC;
```