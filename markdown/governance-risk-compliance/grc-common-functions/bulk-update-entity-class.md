---
title: Update entity classes for multiple entities
description: Provide an entity class for multiple entities where the class field is empty. Entity classes are used to add a conceptual information about the entity and classify the entities. As an administrator, you can update the entity classes for multiple entities with a single click.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Entity classes, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Update entity classes for multiple entities

Provide an entity class for multiple entities where the class field is empty. Entity classes are used to add a conceptual information about the entity and classify the entities. As an administrator, you can update the entity classes for multiple entities with a single click.

## Before you begin

Role required: sn\_grc.admin

## About this task

The classes are only added for the entities that match the filter conditions and that do not have any entity classes associated with them. You can use the **Bulk Update Entity Class** option in the classic user interface to perform the action in the following different ways:

-   **All entities with empty class**: Use this option to apply a common class to all entities that have an empty class field across all tables that match the filter criteria. As an administrator, you can set the filter conditions.
-   **Select a table**: Use this option to apply a common class to all the entities that have an empty class field in the selected table.

## Procedure

1.  In the classic user interface, navigate to **Administration** &gt; **Bulk Update Entity Class**.

2.  To select your entities, do one of the following:

    -   In the **Record Selection** field, select the **All entities with an empty class**.

        add the filter condition if applicable with an **ADD** or **OR** clause.

    -   In the **Record Selection** field, select **Select a table** to select the entities from a table.
3.  After selecting the record, click **Refresh**.

    The number of updated records that match the filter condition are displayed. The classes are added only for the entities that match the filter conditions and that do not have any classes associated with them.

4.  To select the class that will be applied to the selected record, use the **Set the entity class as** field.

5.  Click **Submit**.


## Result

The entity classes for multiple entities are updated.

**Parent Topic:**[Entity classes](../concept/entity-class-in-risk-ws.md)

