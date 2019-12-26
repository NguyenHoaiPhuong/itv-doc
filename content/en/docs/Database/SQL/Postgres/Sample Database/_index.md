---
title: "PostgreSQL Sample Database"
linkTitle: "PostgreSQL Sample Database"
weight: 4
description: >
  Sample database being used for practice.
---

{{% pageinfo %}}
Summary: in this tutorial, we will introduce you to a PostgreSQL sample database that you can use for learning and practice PostgreSQL.
{{% /pageinfo %}}

We will use the DVD rental database for demonstrating the features of PostgreSQL.

The DVD rental database represents the business processes of a DVD rental store. The DVD rental database has many objects including:

* 15 tables
* 1 trigger
* 7 views
* 8 functions
* 1 domain
* 13 sequences

## DVD Rental ER Model

<img class="center" src="dvd-rental-sample-database-diagram.png" />

## PostgreSQL Sample Database Tables

There are 15 tables in the DVD Rental database:

* actor – stores actors data including first name and last name.
* film – stores films data such as title, release year, length, rating, etc.
* film_actor – stores the relationships between films and actors.
* category – stores film’s categories data.
* film_category- stores the relationships between films and categories.
* store – contains the store data including manager staff and address.
* inventory – stores inventory data.
* rental – stores rental data.
* payment – stores customer’s payments.
* staff – stores staff data.
* customer – stores customers data.
* address – stores address data for staff and customers
* city – stores the city names.
* country – stores the country names.

## Download PostgreSQL sample database

You can download the PostgreSQL DVD Rental sample database via the following link:

<a type="button" href="dvdrental.zip">Download DVD Rental Sample Database</a>

The database file is in zipformat (dvdrental.zip) so you need to extract it to  dvdrental.tar before loading the sample database into the PostgreSQL database server.

## Download printable ER diagram

Besides the sample database, we also provide you with a printable ER diagram in PDF format. You can download and print the ER diagram for reference while practicing with PostgreSQL.

<a type="button" href="printable-postgresql-sample-database-diagram.pdf">Download the Printable ER Diagram</a>

This tutorial introduced you to a PostgreSQL sample database named DVD rental. We will use this database in our PostgreSQL tutorials so make sure that you have it on your server.