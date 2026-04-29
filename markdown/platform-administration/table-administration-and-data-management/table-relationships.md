---
title: Table relationships
description: You can create relationships between tables by extending tables, referencing records in another table, creating many-to-many relationships, and joining tables in a database view.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring tables, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Table relationships

You can create relationships between tables by extending tables, referencing records in another table, creating many-to-many relationships, and joining tables in a database view.

Tables can be related to each other in several ways.

-   **Extensions**

    A table can extend another table. The table doing the extending \(child class\) includes all of the fields of the other table \(parent class\) and adds its own fields. For instance, the Incident \[incident\] table has all of the Task \[task\] table fields \(because an incident is a special form of task\) and has its own incident-specific tasks. See [Table extension and classes](table-extension-and-classes.md).

-   **One-to-many**

    Within a table, a field can hold a reference to a record on another table. There are three types of one-to-many relationship fields.

    -   **Reference fields**

        Allow a user to select a record on a table defined by the reference field. For instance, the **Caller** field on the Incident table allows the user to select any record on the User table.

    -   **Glide lists**

        Allow a user to select multiple records on a table defined by the glide list. For instance, the **Watch list** field on the Incident \[incident\] table allows the user to select records on the User \[sys\_user\] table.

    -   **Document ID fields**

        Allow a user to select a record on any table in the instance. These fields are much less common, but one example is the **Document** field on the Translated Text \[sys\_translated\_text\] table.

-   **Many-to-many**

    Two tables can have a bi-directional relationship, so that the related records are visible from both tables in a related list.

-   **Database views**

    Two tables can be joined virtually in a database view to enable reporting on data that might be stored over more than one table.


**Parent Topic:**[Exploring ServiceNow AI Platform tables](exploring-table-administration.md)

