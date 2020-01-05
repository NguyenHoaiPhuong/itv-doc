---
title: "WHERE"
linkTitle: "WHERE"
weight: 4
description: >
  PostgreSQL WHERE
---

{{% pageinfo %}}
**Summary**: in this tutorial, you’ll learn how to use PostgreSQL `WHERE` clause to filter rows returned from the `SELECT` statement.
{{% /pageinfo %}}

In the previous tutorial, you have learned how to use the `SELECT` statement to query data from a table. What if you want to query just particular rows from a table that satisfy a certain condition. In this case, you need to use the `WHERE` clause.

## Overview

The syntax of the PostgreSQL `WHERE` clause is as follows:

```
SELECT select_list
FROM table_name
WHERE condition;
```

The `WHERE` clause appears right after the `FROM` clause of the `SELECT` statement.  The `WHERE` clause uses the condition to filter the rows returned from the SELECT statement.

The **condition** must evaluate to true, false, or unknown. It can be a Boolean expression or a combination of Boolean expressions using AND and OR operators.

The query returns the rows that satisfy the **condition** in the `WHERE` clause. In other words, only rows that cause the condition evaluates to true will be included in the result set.

Besides the `SELECT` statement, you can use the `WHERE` clause in the `UPDATE` and `DELETE` statement to specify rows to be updated or deleted.

The following table illustrates the standard comparison operators.

<table class="table-2">
  <colgroup>
    <col class="thirty" />
    <col class="seventy" />
  </colgroup>

  <tr>
    <th>Operator</th>
    <th>Description</th>
  </tr>

  <tr>
    <td>=</td>
    <td>Equal</td>
  </tr>
  <tr>
    <td>></td>
    <td>Greater than</td>
  </tr>
  <tr>
    <td><</td>
    <td>Less than</td>
  </tr>
  <tr>
    <td>>=</td>
    <td>Greater than or equal</td>
  </tr>
  <tr>
    <td><=</td>
    <td>Less than or equal</td>
  </tr>
  <tr>
    <td><> or !=</td>
    <td>Not equal</td>
  </tr>
  <tr>
    <td>AND</td>
    <td>Logical operator AND</td>
  </tr>
  <tr>
    <td>OR</td>
    <td>Logical operator OR</td>
  </tr>
</table>

## Examples

### Using WHERE clause with the equal (=) operator example

```
SELECT
  last_name,
  first_name
FROM
  customer
WHERE
  first_name = 'Jamie';
```

### Using WHERE clause with the AND operator example

```
SELECT
  last_name,
  first_name
FROM
  customer
WHERE
  first_name = 'Jamie'
AND last_name = 'Rice';
```

### Using WHERE clause with the OR operator example

```
SELECT
  first_name,
  last_name
FROM
  customer
WHERE
  last_name = 'Rodriguez' OR 
  first_name = 'Adam';
```

### Using WHERE clause with the IN operator example

```
SELECT
  first_name,
  last_name
FROM
  customer
WHERE 
  first_name IN ('Ann','Anne','Annie');
```

### Using WHERE clause with the LIKE operator example

```
SELECT
  first_name,
  last_name
FROM
  customer
WHERE 
  first_name LIKE 'Ann%'
```

The `%` is called a wildcard that matches any string. The `Ann%` pattern matches any string that starts with `Ann`.

### Using WHERE clause with the BETWEEN operator example

```
SELECT
  first_name,
  LENGTH(first_name) name_length
FROM
  customer
WHERE 
  first_name LIKE 'A%' AND
  LENGTH(first_name) BETWEEN 3 AND 5
ORDER BY
  name_length;
```

### Using WHERE clause with the not equal operator (<>) example

```
SELECT 
  first_name, 
  last_name
FROM 
  customer 
WHERE 
  first_name LIKE 'Bra%' AND 
  last_name <> 'Motley';
```