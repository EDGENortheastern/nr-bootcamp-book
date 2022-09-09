---
sidebar_position: 2
---

# D10S3. Plenary

## Many-to-Many

Sometimes, when Entity Relationship diagrams are being drawn, data engineers come across many-to-many relationships. Those are impossible to build. They need to be resolved and turned into one-to-many.

For exampls, the diagram below reads: one dog can visit many vets and each vet can see many dogs.

<img
    width="70%"
    src="/img/day-10/m2m.svg"
    alt="An svg of 2-table schema"
/>

## Resolving many-to-Many

To actually build the database that matches dogs and vets the database designer has to have a think: how to resolve many-to-many. In case of dogs and vets it is not too difficult. We know that dogs visit vets during appointment. So, the Entity Relationship diagram will look like this:

<img
    width="100%"
    src="/img/day-10/m2m-solved.svg"
    alt="An svg of 2-table schema"
/>

[Link to Diagrams.net](https://drive.google.com/file/d/15QHxSXjyq0vN_6DcdAACxSwO03jIIUeY/view?usp=sharing)

## Replit task

[<img
    src="/img/icons/replit.svg"
    alt="Link to a forkable replit"
/>](https://replit.com/@missPunter/dogs-many-tbl-start#main.sql)