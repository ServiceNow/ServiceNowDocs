---
title: Create an entity filter in the Core UI
description: Create an entity filter under an entity type in the classic user interface. The entity filter defines the table from which data is pulled into each entity type for display. If the entities belong to an application, the users who have access to the entity class that is associated with the entity can only view those entities.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Entity filters, Entity types, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Create an entity filter in the Core UI

Create an entity filter under an entity type in the classic user interface. The entity filter defines the table from which data is pulled into each entity type for display. If the entities belong to an application, the users who have access to the entity class that is associated with the entity can only view those entities.

## Before you begin

Role required: sn\_grc.manager

## Procedure

1.  In the classic user interface, navigate to the **Entity types** list.

2.  Click an entity type in the list and navigate to the **Entity Filters** tab.

3.  To create a new entity filter, click **New**.

<table id="table_kv1_tx3_jqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity type

</td><td>

Name of the entity type.

</td></tr><tr><td>

Entity filter type

</td><td>

Type of the entity filter. The options are as follows:-   **Build your own conditions**
-   **Select from predefined queries**


</td></tr><tr><td>

Table

</td><td>

Name of the table from which the records are filtered.

</td></tr><tr><td>

Filter condition

</td><td>

Filter conditions that display the matching results.

</td></tr><tr><td>

Entity class

</td><td>

Entity class for the entity type.

</td></tr><tr><td>

Use owner field

</td><td>

Option to use **Owner** field information in the query. The owner is the identified risk owner associated with the entity type. When this option is selected, the following fields are displayed: -   **Owner** field: Select a table before modifying the Owner field. Then, select the owner to be associated with the new entity filter.
-   **Default owner** field: Select a default owner from the list.
-   **Empty owner** field: Select one of the following options:
    -   **Create**: Create an owner for the entity filter.
    -   **Do not create**: Do not create a new owner for the entity filter.
    -   **Use Default**: Use the default owner for the entity filter.


</td></tr></tbody>
</table>4.  To save the entity filter, click **Submit**.


**Parent Topic:**[Entity filters](../concept/what-is-an-entity-filter.md)

