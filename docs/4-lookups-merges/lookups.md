---
sidebar_position: 1
---

# D4S1. Lookups in spreadsheets

## Spreadsheets

Often, spreadsheets are used incorrectly. This is fine, as often we're using them as a sketchpad to collect thoughts or perform basic calculations. Ideally, however, as we get more experienced we want to use them in a way that will make our data easily importable into dataframes and databases.

A row is a collection of observations about a particular *entity* - a thing - or a *transaction* - an action.

A row should have a unique identifier, a *key*, that distinguishes it from all other records.

<img
    src="/img/sheets/data_row.png"
    alt="Image of a Row"
/>

We also have columns. Columns are collections of similar observations across different things or actions. Ideally, all of these observations should be of a similar datatype. This means that we can count occurances of particular strings, or perform statistical operations across numerical values. A column should ideally have a *header* at the top to allow us to identify that record.

<img
    src="/img/sheets/data_columns.png"
    alt="Image of a column"
/>

## Lookups in Theory

A lookup is a reference to another table or sheet. These are the basis of relational databases, and are incredibly important for allowing other types of information system to function. Salesforce, which is built on the relational model, also uses lookups heavily.

A lookup effectively links a record in another table. Here, we are using the *reports_to* field to reference another record in the same table. Effectively, we can figure out who someone's boss is. Instead of storing boss's name, boss's role, etc., we can just store a *reference*. 

<img
    src="/img/sheets/data_lookup_same.png"
    alt="Image of a lookup to the same table"
/>

Lookups can also reference other sheets or tables, allowing us to link different datasets. Having different sheets or tables allows us to store different information. For example, here, we are looking up a record in the teams table. The information we want to store about employees is different to the information we want to store about teams, so the columns are different. 

<img
    src="/img/sheets/data_lookup_different.png"
    alt="Image of a lookup to a different table"
/>

Note that the sheets already have lookups in them, so we are storing more information than we need. For example, the team name in column H could be found from a lookup to the teams table, so we would ideally want to remove that from our original sheet. This is called reducing *redundancy* - redundancy is the concept of storing the same information in multiple places.

## Vlookup

It is also possible to do lookups within a spreadsheet, looking for a certain value in a range and returning the corresponding element.
We can do this within a sheet, or between sheets. See below:

<img
    src="/img/sheets/lookup1.png"
    alt="Sheets Image"
/>

<img
    src="/img/sheets/lookup2.png"
    alt="Sheets Image"
/>

<img
    src="/img/sheets/lookup3.png"
    alt="Sheets Image"
/>

<img
    src="/img/sheets/lookup4.png"
    alt="Sheets Image"
/>

<img
    src="/img/sheets/lookup5.png"
    alt="Sheets Image"
/>

When you are ready, complete the following [exercise](https://docs.google.com/spreadsheets/d/1JMW4sl-7rh3LXEhmmlsaCAP9NMAiRb2XGuxDDH-eXoY/edit?usp=sharing)
.
