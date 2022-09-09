---
sidebar_position: 1
---

# D9S1. Database reports

Database reports present data in a way that is easy to view and understand.
For example, rather than viewing the log of all vet appointments of all dogs, you might want to run a report to show how many times each dog visited their vet.

SQL has several ways to produce reports and rearrange data storage tables: the window function, `VIEW`S, `WITH` statements. The simplest one is a `GROUP BY` clause.

## `GROUP BY`

The `GROUP BY` statement operates on the result of the FROM and WHERE clauses. The rows of the resul are split into groups. Columns listed in the `GROUP BY` clause determine the grouping. Each group is then reduced to a single row in the result table.

This result table is called a grouped table, and all operations are now defined on groups rather than on rows.

For example, you want to count the number of dogs of different breeds. Table *dogs* is screenshot below.

dogid|dogname|breed|color|image
| - | - | - | - | - |
1|Champ|German Shephard|brown|🐕
2|Pluto|German Shephard|brown|🐕
3|Bobik|Russian Borzoi||
4|Bella|Dalmatian||
5|Azor|Poodle|white|🐩
6|Max|Poodle|grey|🐩

The `GROUP BY` statement below will group all dogs into groups according to their breed and count the number of individuals in each breed group:

```sql
SELECT breed, count(*)
FROM dogs
GROUP BY breed;
```

The resuling grouped table:

breed|count(*)
| - | - |
Dalmatian|1
German Shephard|2
Poodle|2
Russian Borzoi|1

## Aliasing

Using aliases (`AS`) can help make grouped tables more meaningful.

## HAVING

Aggregate SQL functions can't be used with/in WHERE clauses.
For example, the following query is invalid:

```sql
SELECT release_year
FROM films
GROUP BY release_year
WHERE COUNT(title) > 10;
```

When you want to filter the results based on the output of an aggregate function, you need the `HAVING` clause.

## Replit task for databases

Fork the replit below, add some dogs and run some reports.

[<img
    src="/img/icons/replit.svg"
    alt="Link to a forkable replit"
/>](https://replit.com/@missPunter/sql-dogs-many-tables#main.sql)