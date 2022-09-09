---
sidebar_position: 1
---

# D8S1. CREATE, INSERT, UPDATE

[Data engineers](/1-introduction/intro-data.md#data-engineers) are more likely to use `CREATE,` `INSERT` or `UPDATE` statements in their work. However, understanding how to build, populate and update SQL databases is vital for all data professionals.

## DDL

DDL is Data Definition Language. It allows to make the structure of the database.
It does not allow to put actual data into the database.

Relational databases store data in tables. Database tables can be visualized as spreadsheets. All tables have rows and columns; rows are used for observations, columns for features.

| Dog ID | Name | Breed | Color
| :- | -: | :-: | -: |
| 1  | Pluto | Poodle | White |
| 2 | Rover | Borzoi | Brown |

The first step to make a database for storing information about dogs is to build the table structure. During this step we call column names **attributes**. Attributes are defined with names and data types.

Rows in a relational database are also known as records.

One of the atributes in a relational database has to be set as a **Primary Key**.

---

🔑 A Primary Key is a unique identifier of a record in database table.

---

When we define a table it is important to define its Primary Key.

## `CREATE`

When attributes (the future columns of database tables) are defined, they have to be of specific data types.

### SQLite data types for defining attributes

Some of the SQLite data types are:

| Name | Type | Description |
| :- | :- | -: |
| INTEGER  | INTEGER | Whole numbers, e.g., 32, 5, -20  |
| REAL | REAL | Numbers with a decimal point, e.g., 1.2, -3.2 |
| VARCHAR  | VARCHAR  | Variable strings of characters, text, e.g., "hello" |
| TEXT  | TEXT | Longer strings |

### SQLite constraints

SQL constraints are used to limit the type of data that can go into a table.

The most obvious example is the `NOT NULL` constraint. It allows to make sure the column has values in all rows.

The `PRIMARY KEY` constraint does not allow values that are not unique. See above for the `PRIMARY KEY` definition.

### `CREATE TABLE` example

```sql
CREATE TABLE IF NOT EXISTS dogs(
  dog_id INTEGER NOT NULL PRIMARY KEY,
  dog_name VARCHAR(20),
  breed VARCHAR(20),
  color VARCHAR(50)
);
```

## Making an SQLite replit

Today you will create your own SQL database from scratch (without forking).
This should allow you to push you code to GitHub.

First of all, make sure you are signed in to [replit](https://replit.com/) with your GitHub account. On "Your Profile" page check for connected devices.

Find a button to create a new project. There are several.

Make sure your new replit is SQLite:

<img
  src="/img/day-8/make-new-replit.png"
  alt="Make a new SQlite replit"
  class="medium screenshot"
/>

Once you have created your own SQLite replit, in `main.sql` add:

```bash
.open dbdogs
.mode column
.header on
```

`.open dbdogs` will create and open or just open a database called dogsdb. **Your can use your own name.**

`.mode column` and `.header on` are optional commands to make the output look nicer.

Now, write some DDL to create a dogs database with one table, e.g.:

```sql
DROP TABLE IF EXISTS dogs;

CREATE TABLE IF NOT EXISTS dogs(
  dogid INTEGER NOT NULL PRIMARY KEY,
  dogname VARCHAR(20) NOT NULL,
  breed VARCHAR(20),
  color VARCHAR(50)
);
```

Use your own attributes. The overall idea is to build a database of dogs, their owners and services. We'll see how far we can take it.

## `INSERT`

When we create database tables, we develop only a database structure. For a database to contain some data, records need to be inserted. SQLite allows inserting one record at a time, e.g.:

```sql
INSERT INTO dogs (dogname, breed, color) VALUES
("Azor", "Poodle", "brown");
```

or many records in one go:

```sql
INSERT INTO dogs (dogname, breed) VALUES
("Pluto", "German Sheppard"),
("Bobik", "Russian Borzoi");
```

Add some dogs to your database.

## `UPDATE`

The SQL `UPDATE` Query is used to modify the existing records in a table. You can use the `WHERE` clause with the `UPDATE` query to update the selected rows.

```sql
UPDATE dogs
SET color = "white"
WHERE dogid = 2;
```

Without a `WHERE` clause an `UPDATE` statement will update all records in a table. Oops, all dogs turned orange:

```sql
UPDATE dogs
SET color = "orange";
```

Update some dogs in your database.

## `SELECT`

To see what our database contains we always need to run a `SELECT` command, e.g.:

```sql
SELECT * FROM dogs;
```

## Pushing replit SQL to GitHub

First of all find the version control button on replit:

<img
  src="/img/day-8/git-on-replit.png"
  alt="Replit to GitHub"
  class="medium screenshot"
/>

Opt to create a new repo:

<img
  src="/img/day-8/create-new-gh.png"
  alt="Replit to GitHub"
  class="medium screenshot"
/>

Connect to GitHub.

Create new repository.

See your code on GitHub.

## Replit task for databases

The replit below is just an example of what your own replit may look like.
However, you need to fork it to view it and forking will save a copy on your replit account.

[<img
    src="/img/icons/replit.svg"
    alt="Link to a forkable replit"
/>](https://replit.com/@missPunter/dogs-starter#main.sql)
