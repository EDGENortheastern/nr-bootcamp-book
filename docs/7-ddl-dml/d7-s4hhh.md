---
sidebar_position: 4
---

# D7S4. Introduction to Data modeling

[Slides](https://hackmd.io/@D3o17PKxQImUPBfYYD6wYg/BkgYdbrb5#/1)

Data Modelling is analyzing the data objects and their relationship to the other objects. In database design, the primary outcome of the data modeling process is the final entity-relationship diagram, ERD.

## ER diagrams

An Entity Relationship Diagram (ERD) is a picture representing the structure of a database. It shows the relationships of entity sets and how tables are linked via primary and secondary keys.

<img
    width="100%"
    src="/img/schemadogs.svg"
    alt="An svg of 2-table schema"
/>

An ER model is typically drawn at up to three levels of abstraction:

- Conceptual ERD / Conceptual Data Model
- Logical ERD / Logical Data Model
- Physical ERD / Physical Data Model

## Conceptual models

Conceptual ERD models the business objects and some of the relationships between them. A conceptual model is developed to present an overall picture. It defines entities, NOT tables. "Many-to-many" relationships may existon a conceptual data model.

<img
  src="/img/day-7/conceptual.png"
  alt="Dismiss offer to set up billing"
  class="wide screenshot"
/>

## Logical models

Logical ERD is a more detailed version of a Conceptual ERD. A logical ER model defines explicitly the column heading in each entity and introduces some linking entities. However, it still may have some "many-to-many." Although a logical data model is still independent of the actual database system in which the database will be created, you can still consider that if it affects the design.

<img
  src="/img/day-7/logical1.png"
  alt="Dismiss offer to set up billing"
  class="wide screenshot"
/>

## Physical models

Physical ERD represents the actual design blueprint of a relational database. A physical data model elaborates on the logical data model by assigning each column with type, length, nullable, etc. Since a physical ERD represents how data should be structured and related in a specific DBMS it is important to consider the convention and restriction of the actual database system in which the database will be created. Make sure the column types are supported by the DBMS and reserved words are not used in naming entities and columns.

<img
  src="/img/day-7/physical.png"
  alt="Dismiss offer to set up billing"
  class="wide screenshot"
/>

## Diagrams.net task

Create a single-table Entity Diagram for the famous_women table from the previous task.

[Link to diagrams.net](https://www.diagrams.net/)