---
title: Create a many-to-many table relationship
description: Create a bi-directional relationship between two tables, so that the related records are visible from both tables in a related list.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a many-to-many table relationship

Create a bi-directional relationship between two tables, so that the related records are visible from both tables in a related list.

## Before you begin

Role required: admin.

## About this task

Many-to-many relationships allow a list to point to a list of entries, rather than to single field.

If a knowledge base article points to a list of related configuration items, it uses a related list. Not all lists can be used as related lists, however. For a list to be related to another list, a many-to-many relationship that refers to both tables must exist.

The Many to Many Definitions `[sys_m2m]` table allows administrators to create custom many-to-many relationships.

Many-to-Many tables aren't considered custom tables and don't count toward your custom table allotment.

## Procedure

1.  In the navigation filter, enter `sys_m2m.list`.

2.  Click **New**.

3.  In the **From table** field, specify a parent table.

4.  In the **To table** field, specify a child table.

    The Many-to-Many form automatically populates the other fields with suggested values.

5.  Edit other field values, if appropriate.

    **Note:** Many-to-Many table names cannot exceed 30 characters.


-   **[Reference default many-to-many relationships](../reference/r_RefDefaultManyToManyRels.md)**  
Some many-to-many relationships are defined by default.

**Parent Topic:**[Managing tables and indexes](../concept/using-table-administration.md)

**Related topics**  


[Reference default many-to-many relationships](../reference/r_RefDefaultManyToManyRels.md)

