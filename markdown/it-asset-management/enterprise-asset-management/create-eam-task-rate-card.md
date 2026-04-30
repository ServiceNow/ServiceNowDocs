---
title: Create a task rate card in Enterprise Asset Workspace
description: Create a task rate card to capture costs per task type in the Enterprise Asset Workspace.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Total Cost of Ownership for enterprise assets, Create and manage enterprise assets, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a task rate card in Enterprise Asset Workspace

Create a task rate card to capture costs per task type in the Enterprise Asset Workspace.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## About this task

Task rate cards are included in the base system. Except for the **Number** field, all other fields on the default task rate cards are editable. You can't delete any of the base system task rate cards. The following steps are to create a task rate card.

To use task rate cards, you must activate the ServiceNow® Cost Management \(com.snc.cost\_management\) plugin.

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **TCO configuration** &gt; **Task rate card**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_z5c_y1x_4zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique number automatically created for each task rate card.

</td></tr><tr><td>

Name

</td><td>

Name of the task rate card.

</td></tr><tr><td>

Table

</td><td>

The table this rate card is created for.

</td></tr><tr><td>

Order

</td><td>

Order in which the task rate card applies to the same task.

 When more than one task rate card applies to the same task, the one with the lowest order is used.

</td></tr><tr><td>

Summary type

</td><td>

Select a summary that relates to the task rate card.

</td></tr><tr><td>

Active

</td><td>

Indicates if the task rate card is being used or not. By default, this check box is selected.

</td></tr><tr><td>

Short description

</td><td>

Short description of the task rate card.

</td></tr><tr><td>

Use time worked

</td><td>

By default, this check box isn’t selected. This denotes that the task rate is used for capturing costs.If you want to use the labor rate option where cost is captured based on the time worked, select this check box.

</td></tr><tr><td>

Task rate

</td><td>

Rate of the task along with the currency code.

</td></tr><tr><td>

Default labor rate

</td><td>

The hourly rate to apply to the time worked entries if the worker doesn’t have a labor rate card.This field appears only when the **Use time worked** check box is selected.

</td></tr><tr><td>

Set conditions

</td><td>

Filter to run on the table selected to determine whether this rate card applies to a given task. This field uses the Condition Count Widget to preview what records would be returned by the conditions.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task rate card.

</td></tr></tbody>
</table>4.  Select **Save**.

    After a task rate card is created, expense lines are created based on the value in the **Use time worked** field.


**Parent Topic:**[Configuring Total Cost of Ownership for enterprise assets](../concept/confifure-eam-asset-tco.md)

