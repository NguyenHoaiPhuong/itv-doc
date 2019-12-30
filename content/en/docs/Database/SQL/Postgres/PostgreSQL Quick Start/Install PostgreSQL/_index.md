---
title: "Install PostgreSQL"
linkTitle: "Install PostgreSQL"
weight: 2
description: >
  How To Install and Use PostgreSQL on Ubuntu 18.04
---

{{% pageinfo %}}
Summary: in this tutorial, we will show you how to install PostgreSQL on your local system for learning and practicing PostgreSQL.
{{% /pageinfo %}}

## Introduction

Relational database management systems are a key component of many web sites and applications. They provide a structured way to store, organize, and access information.

PostgreSQL, or Postgres, is a relational database management system that provides an implementation of the SQL querying language. It is a popular choice for many small and large projects and has the advantage of being standards-compliant and having many advanced features like reliable transactions and concurrency without read locks.

This guide demonstrates how to install Postgres on an Ubuntu 18.04 VPS instance and also provides instructions for basic database administration.

## Prerequisites

To follow along with this tutorial, you will need one Ubuntu 18.04 server that has been configured by following our [Initial Server Setup for Ubuntu 18.04](/docs/operating-system/linux/initial-server-setup/) guide. After completing this prerequisite tutorial, your server should have a non-root user with sudo permissions and a basic firewall.

## Step 1 — Installing PostgreSQL

Ubuntu’s default repositories contain Postgres packages, so you can install these using the apt packaging system.

```
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
```

Since this is your first time using apt in this session, refresh your local package index. Then, install the Postgres package along with a -contrib package that adds some additional utilities and functionality:

```
sudo apt update
sudo apt -y install postgresql postgresql-contrib
```
Now that the software is installed, we can go over how it works and how it may be different from similar database management systems you may have used.

## Step 2 — Using PostgreSQL Roles and Databases

By default, Postgres uses a concept called “roles” to handle in authentication and authorization. These are, in some ways, similar to regular Unix-style accounts, but Postgres does not distinguish between users and groups and instead prefers the more flexible term “role”.

Upon installation, Postgres is set up to use ident authentication, meaning that it associates Postgres roles with a matching Unix/Linux system account. If a role exists within Postgres, a Unix/Linux username with the same name is able to sign in as that role.

The installation procedure created a user account called `postgres` that is associated with the default Postgres role. In order to use Postgres, you can log into that account.

There are a few ways to utilize this account to access Postgres.

### Switching Over to the postgres Account

Switch over to the `postgres` account on your server by typing:

```
sudo -i -u postgres
```

You can now access a Postgres prompt immediately by typing:

```
psql
```

This will log you into the PostgreSQL prompt, and from here you are free to interact with the database management system right away.

Exit out of the PostgreSQL prompt by typing:

```
postgres=# \q
```

This will bring you back to the `postgres` Linux command prompt.

### Accessing a Postgres Prompt Without Switching Accounts

You can also run the command you’d like with the `postgres` account directly with `sudo`.

For instance, in the last example, you were instructed to get to the **Postgres** prompt by first switching to the `postgres` user and then running psql to open the Postgres prompt. You could do this in one step by running the single command `psql` as the `postgres` user with `sudo`, like this:

```
sudo -u postgres psql
```

This will log you directly into Postgres without the intermediary `bash` shell in between.

Again, you can exit the interactive Postgres session by typing:

```
postgres=# \q
```

Many use cases require more than one Postgres role. Read on to learn how to configure these.

## Step 3 — Creating a New Role

Currently, you just have the **postgres** role configured within the database. You can create new roles from the command line with the `createrole` command. The `--interactive` flag will prompt you for the name of the new role and also ask whether it should have superuser permissions.

If you are logged in as the **postgres** account, you can create a new user by typing:

```
postgres@server:~$ createuser --interactive
```

If, instead, you prefer to use sudo for each command without switching from your normal account, type:

```
sudo -u postgres createuser --interactive
```

The script will prompt you with some choices and, based on your responses, execute the correct Postgres commands to create a user to your specifications.

```
Output
Enter name of role to add: itv
Shall the new role be a superuser? (y/n) y
```

You can get more control by passing some additional flags. Check out the options by looking at the `man` page:

```
man createuser
```

Your installation of Postgres now has a new user, but you have not yet added any databases. The next section describes this process.

## Step 4 — Creating a New Database

Another assumption that the Postgres authentication system makes by default is that for any role used to log in, that role will have a database with the same name which it can access.

This means that, if the user you created in the last section is called **itv**, that role will attempt to connect to a database which is also called "itv" by default. You can create the appropriate database with the `createdb` command.

If you are logged in as the **postgres** account, you would type something like:

```
postgres@server:~$ createdb itv
```

If, instead, you prefer to use `sudo` for each command without switching from your normal account, you would type:

```
sudo -u postgres createdb sammy
```

This flexibility provides multiple paths for creating databases as needed.

## Step 5 — Opening a Postgres Prompt with the New Role

To log in with `ident` based authentication, you’ll need a Linux user with the same name as your Postgres role and database.

If you don’t have a matching Linux user available, you can create one with the `adduser` command. You will have to do this from your **non-root** account with `sudo` privileges (meaning, not logged in as the postgres user):

```
sudo adduser itv
```

Once this new account is available, you can either switch over and connect to the database by typing:

```
sudo -i -u itv
psql
```

Or, you can do this inline:

```
sudo -u itv psql
```

This command will log you in automatically, assuming that all of the components have been properly configured.

If you want your user to connect to a different database, you can do so by specifying the database like this:

```
psql -d postgres
```

Once logged in, you can get check your current connection information by typing:

```
itv=# \conninfo
```

```
Output
You are connected to database "sammy" as user "sammy" via socket in "/var/run/postgresql" at port "5432".
```

This is useful if you are connecting to non-default databases or with non-default users.

## Conclusion

You are now set up with PostgreSQL on your Ubuntu 18.04 server. However, there is still much more to learn with Postgres. Here are some more guides that cover how to use Postgres:

* [A comparison of relational database management systems](https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-postgresql-a-comparison-of-relational-database-management-systems)
* [Learn how to create and manage tables with Postgres](https://www.digitalocean.com/community/tutorials/how-to-create-remove-manage-tables-in-postgresql-on-a-cloud-server)
* [Get better at managing roles and permissions](https://www.digitalocean.com/community/tutorials/how-to-use-roles-and-manage-grant-permissions-in-postgresql-on-a-vps--2)
* [Craft queries with Postgres with Select](https://www.digitalocean.com/community/tutorials/how-to-create-data-queries-in-postgresql-by-using-the-select-command)
* [Learn how to secure PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps)
* [Learn how to backup a Postgres database](https://www.digitalocean.com/community/tutorials/how-to-backup-postgresql-databases-on-an-ubuntu-vps)