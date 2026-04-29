---
title: Create work types for a work order task
description: You have the option to categorize the type of work to be performed in Field Service to complete the task.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Create work types for a work order task

You have the option to categorize the type of work to be performed in Field Service to complete the task.

## Before you begin

Role required: wm\_admin

## About this task

Create different work types for a task to determine and configure the various requirements of the task, such as if the task needs a crew and preference of an assignment group.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Work Types**.

2.  Select New.

3.  On the form, fill in the fields.

<table id="table_vnq_14n_dsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the type of work.

</td></tr><tr><td>

Value

</td><td>

Name of the work type to be stored Internally.

</td></tr><tr><td>

Description

</td><td>

Description of the work type.

</td></tr><tr><td>

Scheduling preference

</td><td>

Type of assignment group to which the task should be assigned to, such as internal and external group.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the work type is available for selection when creating a work order task.

</td></tr><tr><td>

Needs crew

</td><td>

Option to indicate if the crew is required for the selected type of work.

</td></tr><tr><td>

Resource requirements

</td><td>

Option to indicate if resource, such as agent or equipment, is required for the selected type of work.**Note:** The field appears only when Field Service Resource Scheduling plugin \(com.snc.fsm\_resource\_scheduling\) is active.

</td></tr></tbody>
</table>4.  Select and hold \(or right-click\) the form header and select **Submit**.

    ![new work type form](../image/new-work-type.png)


## Result

The work type is created successfully.

-   If you have selected the Needs crew option, the work type is created with the Crew Requirements related list record.
-   If you have selected the Resource requirements option, the work type is created with the Resource Requirements related list record.

For more information about adding the resource requirement, see [Add resource requirements for a work order task](add-resource-requirement-wot.md).

