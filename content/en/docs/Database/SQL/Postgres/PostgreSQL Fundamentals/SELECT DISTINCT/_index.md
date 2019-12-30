---
title: "SELECT DISTINCT"
linkTitle: "SELECT DISTINCT"
weight: 3
description: >
  PostgreSQL SELECT DISTINCT
---

{{% pageinfo %}}
**Summary**: in this tutorial, you will learn how to use the PostgreSQL `SELECT DISTINCT` clause to remove duplicate rows from a result set returned by a query.
{{% /pageinfo %}}

## Introduction

The `DISTINCT` clause is used in the `SELECT` statement to remove duplicate rows from a result set. The `DISTINCT` clause keeps one row for each group of duplicates. The `DISTINCT` clause can be used on one or more columns of a table.

The following illustrates the syntax of the `DISTINCT` clause:

```
SELECT
  DISTINCT column_1
FROM
  table_name;
```

In this statement, the values in the column_1 column are used to evaluate the duplicate.

If you specify multiple columns, the `DISTINCT` clause will evaluate the duplicate based on the combination of values of these columns.

```
SELECT
  DISTINCT column_1, column_2
FROM
  table_name;
```

In this case, the combination of values in both column_1 and column_2 columns will be used for evaluating the duplicate.

PostgreSQL also provides the `DISTINCT ON` (expression) to keep the “first” row of each group of duplicates using the following syntax:

```
SELECT
  DISTINCT ON (column_1) column_alias,
  column_2
FROM
  table_name
ORDER BY
  column_1,
  column_2;
```

The order of rows returned from the `SELECT` statement is unpredictable therefore the "first" row of each group of the duplicate is also unpredictable. It is good practice to always use the `ORDER BY` clause with the `DISTINCT ON` (expression) to make the result set obvious.

Notice that the `DISTINCT ON` expression must match the leftmost expression in the `ORDER BY` clause.

## Examples

