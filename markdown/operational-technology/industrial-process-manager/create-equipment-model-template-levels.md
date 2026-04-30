---
title: Create hierarchical sorting levels for an equipment model template
description: Create and assign hierarchical levels for your equipment model template. When you assign an equipment template to an equipment model, these levels sort and structure the data you see in it.
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Defining equipment model templates, Configure, Industrial Process Manager, Operational Technology]
---

# Create hierarchical sorting levels for an equipment model template

Create and assign hierarchical levels for your equipment model template. When you assign an equipment template to an equipment model, these levels sort and structure the data you see in it.

## Before you begin

Role required: admin

## About this task

You can assign levels to an equipment model template for sorting purposes. For example, you can assign Site, Area, Work Center and other levels to the equipment, and designate the sorting sequence for each.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Template**.

2.  Select an equipment model template.

3.  In the Template Levels related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_ec1_wtm_hqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Level name

</td><td>

Name of the level to which you are assigning the equipment model. Examples include:-   **Site**

An industrial site.

-   **Area**

An area in an industrial site.

-   **Work Center**

A work center in an industrial site.

</td></tr><tr><td>

Parent

</td><td>

Identifier for the equipment model template level above this level. If left empty, this level is the top level in the model. For example, you can do the following actions:-   If you are creating a Site level, leave this field empty if it is the top level of the equipment model hierarchy that does not have a parent.
-   If you are creating an Area level, and it is a child to the Site level, select **Site** as its parent.
-   If you are creating a Work Center level, and it is a child to the Area level, select **Area** as its parent.


</td></tr><tr><td>

Application

</td><td>

Selected application scope. Global appears if this scope is the global application scope.

</td></tr><tr><td>

Template

</td><td>

Name of the selected equipment model template.

</td></tr><tr><td>

Order

</td><td>

Number that indicates the position of the level in the equipment model hierarchy for sorting purposes. The smallest number entered represents the highest hierarchical level. For example, enter `1` for Site if the site represents the highest level in the hierarchy for the equipment model template.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

Create granular types within an equipment model template hierarchical level.

**Parent Topic:**[Defining equipment model templates](../concept/defining-equipment-model-templates.md)

