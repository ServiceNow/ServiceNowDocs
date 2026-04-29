---
title: Create an entity filter
description: Create an entity filter under an entity type in the workspace view. Entities in entity type are created based on the conditions set in the Entity Filter. The entity filter defines the table from which data is pulled into each entity type for display.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Entity filters, Entity types, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Create an entity filter

Create an entity filter under an entity type in the workspace view. Entities in entity type are created based on the conditions set in the Entity Filter. The entity filter defines the table from which data is pulled into each entity type for display.

## Before you begin

Roles required: sn\_grc.manager, sn\_risk\_workspace.IT\_risk\_manager, and sn\_risk\_workspace.operational\_risk\_manager

## About this task

You can use one of the following filter conditions for the entity type:

-   Build your own conditions
-   Select from predefined queries

## Procedure

1.  Navigate to the desired workspace, go to the List view, and click **Entity types**.

2.  Click an entity type in the list and navigate to the **Entity Filters** tab.

3.  To create a new entity filter, click **New**.

    The Create New Entity Filter page is displayed.

4.  In the **Details** tab, fill in the fields.

<table id="table_kv1_tx3_jqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Filter for

</td></tr><tr><td>

Entity type

</td><td>

Name of the entity type under which the new entity filter is created.

</td></tr><tr><td class="sub-head" colspan="2">

Filter conditions

</td></tr><tr><td>

Entity filter type: **Build your own conditions**

</td><td>

Type of the entity filter that is used for filtering the data. Use the Configuration Management Database \(CMDB\) Query Builder to build your own query.

 The Configuration Management Database \(CMDB\) is used to search the database for the entities. It provides the following methods for filtering:

 -   **Build your own conditions**
-   **Select from predefined queries**
 Complete the following steps for the **Build your own conditions** entity filter type:

1.  In the **Entity filter type** field, select the entity filter type as **Build your own conditions**.
2.  In the **Table** field, select a table from the populated list.
3.  In the **Filter condition** field, click **Set conditions**, build a filter condition, click **Set**, and view the matching results.


</td></tr><tr><td>

Entity filter type: **Select from predefined queries** option

</td><td>

Predefined query to scope the entity. Complete the following steps for the **Select from predefined queries** option:1.  In the **Query** field, select a predefined query such as **Business Apps using Information Object** that is applicable for the selected entity.

Table associated with the entity when a predefined query is selected. The table is automatically populated.

2.  In the **Information objects** field, select only the applications and processes that have information objects associated with them. To add more information objects, click **Information objects** and type information objects such as `Email`.
 **Note:** To use a predefined CMDB query for entity scoping, GRC administrators must assign the **GRC Scoping** tag to the selected CMDB query.

As a sn\_grc.admin user, navigate to **Policy and Compliance &gt; Administration &gt; GRC Properties** or navigate to **Risk Administration &gt; GRC Properties** in an instance, set the **Enable entity scoping for CMDB query** property as **Yes** and click **Save**.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Entity class

</td><td>

Entity class to be associated with the entity type. You can now assign an entity class to an entity filter under entity type. When a new entity gets created using an entity filter, an entity class gets assigned to it automatically.

</td></tr><tr><td>

Use owner field

</td><td>

Option to use the owner field. The owner is the identified risk owner associated with the entity type. This condition uses the **Owner** field information in the query. When the check box for this field is selected, the following fields are displayed: -   **Owner** field: Select a table before modifying the Owner field. Then, select the owner to be associated with the new entity filter.
-   **Default owner** field: Select a default owner from the list.
-   **Empty owner** field: Select one of the following options:
    -   **Create**: Create an owner for the entity filter.
    -   **Do not create**: Do not create a new owner for the entity filter.
    -   **Use Default**: Use the default owner for the entity filter.


</td></tr><tr><td>

Attachments

</td><td>

Attachments associated with the entity that are displayed in the side panel.

</td></tr></tbody>
</table>5.  To save the entity filter, click **Save**.


**Parent Topic:**[Entity filters](../../grc-common/concept/what-is-an-entity-filter.md)

