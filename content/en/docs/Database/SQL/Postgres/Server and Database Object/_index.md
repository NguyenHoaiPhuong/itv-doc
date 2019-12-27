---
title: "PostgreSQL Server and Database Objects"
linkTitle: "PostgreSQL Server and Database Objects"
weight: 5
description: >
  Sample database being used for practice.
---

{{% pageinfo %}}
Summary: in this tutorial, you are going to get familiar with the most common server and database objects provided by PostgreSQL. It is important to understand those objects and their functionality so you do not miss out on the cool features that you may wish to have in the system.
{{% /pageinfo %}}

After installing PostgreSQL, loading sample database and connecting to the database server using pgAdmin GUI application, you will see that PostgreSQL provides many server and database objects. To leverage the features of each object that PostgreSQL provides effectively, you should have a good understanding of what each object is and how to use it effectively.

Let’s get familiar with these PostgreSQL server and database objects.

## Server service

When you install a PostgreSQL instance, you will have a corresponding PostgreSQL server service. The PostgreSQL server service is also known as the PostgreSQL server. You can install multiple PostgreSQL servers on a physical server using different ports and having different locations to store data.

## Databases

A database is a container of other objects such as **tables**, **views**, **functions**, and **indexes**. You can create as many databases as you want inside a PostgreSQL server.

<img class="center" src="postgresql-databases.png" />

### Tables

A special feature of PostgreSQL is table inheritance, meaning that a table (child table) can inherit from another table (parent table) so when you query data from the child table, the data from the parent table is also showing up.

