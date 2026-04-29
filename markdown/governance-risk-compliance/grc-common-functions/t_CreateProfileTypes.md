---
title: Generate risks and controls from entity types
description: Create and edit entity types and map them to existing ServiceNow tables for which you must track compliance \(applications, departments, regions, processes, systems, etc.\). Entities are assigned to control objectives and risk statements, which generate controls and risks for every entity type.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Entity scoping, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Generate risks and controls from entity types

Create and edit entity types and map them to existing ServiceNow® tables for which you must track compliance \(applications, departments, regions, processes, systems, etc.\). Entities are assigned to control objectives and risk statements, which generate controls and risks for every entity type.

## Before you begin

Role required:

-   sn\_compliance.admin or sn\_compliance.manager
-   sn\_risk.admin or sn\_risk.manager
-   sn\_audit.admin or sn\_audit.manager

## About this task

An entity type provides you a method to group Entities together. An entity type can be explained in the following example: Assume that you want to generate a risk of earthquake for all the data centers in a particular region. You could simply create an entity type called "Data Center" and associate all the entities of that region to the risk of earthquake based on the risk statement.

## Procedure

1.  Navigate to one of the following locations.

    -   **Policy and Compliance** &gt; **Scoping** &gt; **Entity Types**.
    -   **Risk** &gt; **Scoping** &gt; **Entity Types**.
    -   **Audit** &gt; **Scoping** &gt; **Entity Types**.
2.  Do one of the following actions.

<table id="choicetable_wn5_ds3_4w"><tbody><tr><td id="d228317e139">

**To create a new entity type**

</td><td>

Click **New**.

</td></tr><tr><td id="d228317e151">

**To edit an entity type**

</td><td>

Open the entity type from the list.

</td></tr><tr><td id="d228317e160">

**To delete an entity type**

</td><td>

Open the entity type from the list and click **Delete**.The item generation process executes these actions in the background. With the legacy implementation of the item generation process \(v1\), the entity type that was marked for deletion would get deleted instantly.

 With the implementation of the item generation process \(v2\), an entity type that is marked for deletion is not deleted instantly by the item generation process, but it is marked for deletion. When the nightly scheduled job runs, it deletes the entity type.

 For more information on the item generation process, see [Using the item generation process to generate controls and risks](../concept/item-generation-process.md).

</td></tr></tbody>
</table>3.  Fill in the fields on the form, as appropriate, and click **Submit** or **Update**.

    |Name|Description|
    |----|-----------|
    |Name|Name of the entity type.|
    |Description|Explanation of the entity type with any additional information that a user finds helpful.|

4.  Once the entity type is saved, click the **Entity filters** tab and On the form, fill in the fields.

<table id="table_xdv_yd3_x1b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity Type

</td><td>

Indicates the entity type that the filters belong to.

</td></tr><tr><td>

Table

</td><td>

Table that contains the records to be queried.

</td></tr><tr><td>

Filter condition

</td><td>

Filter conditions for the source table to generate entities.

</td></tr><tr><td>

Owner field

</td><td>

Person who owns any new entities generated from the entity type.Identify the user reference field on the source table to automatically identify risk and control owners. Use default owner to assign risks to a single user when the owner field is empty.

</td></tr><tr><td>

Empty owner

</td><td>

-   Create
-   Do not create
-   Use default


</td></tr></tbody>
</table>5.  Click **Submit**.

6.  From the **Entity type** form, click **Update Entities from Filters**.

    An informational message appears: Updating entities for this entity type.


**Parent Topic:**[Entity scoping in GRC](../concept/c_Scoping.md)

