---
sidebar_position: 1
---

# D7S1. Introduction to DML, DDL, DQL

## Databases

## DML, DDL, DQL

SQL is a difficult language. Firstly, it is declarative: the programmer does not tell the computer how to do something, just what exactly they want done.

Secondly, there are several brands of SQL languages, e.g., [Postgresql](https://www.postgresql.org/https://www.postgresql.org/), [SQLite](https://www.sqlite.org/docs.html).

Finally, SQL consists of several sublanguages. They are:

- DDL – Data Definition Language
- DQL – Data Query Language
- DML – Data Manipulation Language
- DCL – Data Control Language

## DDL

Data Definition Language(DDL) is used by data engineers and software developers. DDL allows creating and modifying database objects such as tables.

Here is an example of a DDL create statement in **Postgresql**:

```sql
CREATE TABLE users
(
    id BIGSERIAL PRIMARY KEY NOT NULL,
    first_name VARCHAR(150) NOT NULL,
    email VARCHAR(60) NOT NULL,
    hashed_password VARCHAR(255) NOT NULL,
    date_of_birth DATE NOT NULL,
    in_greater_london BOOLEAN NOT NULL,
    paid_breaks BOOLEAN NOT NULL,
    created_at TIMESTAMPTZ NOT NULL DEFAULT now(),
    updated_at TIMESTAMPTZ NOT NULL DEFAULT now()
);
```

We will be using SQLite for our second week project. Here is some DDL in SQLite:

```sql
-- DDL
DROP TABLE IF EXISTS famous_women;

CREATE TABLE IF NOT EXISTS famous_women (
    userid INTEGER PRIMARY KEY NOT NULL,
    user_name VARCHAR(50) NOT NULL,
    why_famous VARCHAR(320) NOT NULL,
    lastlogin INTEGER(4) DEFAULT CURRENT_TIMESTAMP
);
```

The `DROP` command deletes a table. The `CREATE` command creates a table.

## DML

Data Manipulation Language (DML) is a language used for adding (inserting), deleting, and modifying (updating) data in a database.

Data engineers and software developers use DML to populate databases, e.g., to connect the user to the database via a user interface.

Here is a Postgresql example:

```sql
INSERT INTO users
    (first_name, email, date_of_birth, in_greater_london, paid_breaks)
VALUES('fac', 'fac@fac.com', '1992-06-08', true, true);
```

Here is an SQLite example:

```sql
-- DML
INSERT INTO
  famous_women (user_name, why_famous)
VALUES
  ("Maria Pevchikh", "Investigates Corruption in Russia"),
  ("Andrea Dworkin", "Feminist"),
  ("Alexandria Ocasio-Cortez", "Politician and activist"),
  ("Emmeline Pankhurst", "Organized the UK suffragette movement");
```

## DQL

Data Analysts are most likely to use Data Query Language (DQL). It allows to gain insights from the database data.

[Click on the link](https://console.cloud.google.com/bigquery?sq=946288200397:21dc18cd44b64b0a80f74b1fbb0df6bd&project=hidden-display-339511) to see an example of a DQL `SELECT` statement. It is a sample query that allows to query a public SQL dataset.

Here is an SQLite example:

```sql
SELECT
  *
FROM
  famous_women;
```

## Replit task for DDl, DML and DQL

Fork the replit below and complete commented out tasks. Push your code to GitHub to impress your future employer.

[<img
    src="/img/icons/replit.svg"
    alt="Link to a forkable replit"
/>](https://replit.com/@missPunter/ddldmldql#main.sql)

[Link to replit](https://replit.com/@missPunter/ddldmldql#main.sql)