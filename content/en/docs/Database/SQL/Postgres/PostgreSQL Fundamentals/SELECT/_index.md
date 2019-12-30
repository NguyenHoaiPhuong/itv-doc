---
title: "SELECT"
linkTitle: "SELECT"
weight: 1
description: >
  PostgreSQL SELECT
---

{{% pageinfo %}}
**Summary**: in this tutorial, you are going to learn how to use basic PostgreSQL SELECT statement to query data from a table.
{{% /pageinfo %}}

One of the most common tasks, when you work with PostgreSQL, is to query data from tables by using the `SELECT` statement. The `SELECT` statement is one of the most complex statements in PostgreSQL. It has many clauses that you use to form a flexible query.

Because of its complexity, we will break down the PostgreSQL `SELECT` statement tutorial into many shorter and easy-to-understand tutorials so that you can learn the functionality of each clause faster.

The SELECTstatement has the following clauses:

* Select distinct rows using `DISTINCT` operator.
* Sort rows using `ORDER BY` clause.
* Filter rows using `WHERE` clause.
* Select a subset of rows from a table using `LIMIT` or `FETCH` clause.
* Group rows into groups using `GROUP BY` clause
* Filter groups using `HAVING` clause.
* Join with other tables using joins such as `INNER JOIN`, `LEFT JOIN`, `FULL OUTER JOIN`, `CROSS JOIN` clauses.
* Perform set operations using `UNION`, `INTERSECT`, and `EXCEPT`.

In this tutorial, you are going to focus on the `SELECT` and `FROM` clauses.

## PostgreSQL SELECT statement syntax

```
SELECT
   column_1,
   column_2,
   ...
FROM
   table_name;
```

Let’s examine the SELECTstatement in more detail:

* First, specify the column of the table from which you want to query data in the `SELECT` clause. If you retrieve data from multiple columns, use a list of comma-separated columns. In case you want to query data from all columns, you can use an asterisk (*) as the shorthand.
* Second, specify the name of the table from which you want to query data after the `FROM` keyword.

## PostgreSQL SELECT examples

### SELECT single column

```
SELECT 
  first_name
FROM 
  customer;
```

### SELECT multiple columns
```
SELECT
  first_name,
  last_name,
  email
FROM
  customer;
```

### SELECT all columns

```
SELECT
  *
FROM
  customer;
```

### SELECT statement with expressions

```
SELECT 
  first_name || ' ' || last_name AS full_name,
  email
FROM 
  customer;
```

### SELECT statement with  only expressions example

```
SELECT 5 * 3 AS result;
```