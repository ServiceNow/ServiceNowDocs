---
title: Enable a work order template to create relevant tasks for a work order
description: Add the standalone task template to a work order template along with filtering conditions. This enables the work order template to identify and create the same task for different work orders only when the filtering conditions matches.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Standalone task templates, Template Management, Work orders, Work orders and tasks, Configure, Field Service Management]
---

# Enable a work order template to create relevant tasks for a work order

Add the standalone task template to a work order template along with filtering conditions. This enables the work order template to identify and create the same task for different work orders only when the filtering conditions matches.

## Before you begin

You must activate the Template Management for Field Service plugin \(com.snc.fsm\_template\_management\).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Template Management** &gt; **Work Order Templates**.

2.  Open a work order template from the Work Order Templates list.

3.  In the Service Order Task Models related list, select **Add**.

4.  On the form, fill in the fields.

<table id="table_a5k_pbl_b5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order Model

</td><td>

Name of the work order template to which you’re adding the task template.This field is automatically set based on the selected order model.

</td></tr><tr><td>

Table

</td><td>

Table that is associated with this work order template. For example, wm\_order.

</td></tr><tr><td>

Task Model

</td><td>

Name of the work order task template that you want to add to the work order template.

</td></tr><tr><td>

Order

</td><td>

Order in which the task template should be evaluated to create the task for a work order.

</td></tr></tbody>
</table>5.  Add filter conditions.

    1.  Select **Add Filter Condition**.

    2.  Create the condition.

        For example, **\[Account\] \[is\] \[Boxeo\] AND \[Active\] \[is\] \[true\]**.

    3.  If you want to add an alternate condition set to the query, select **New condition set** and add the conditions for the alternate set.

    The conditions to help determine the task for a work order when using this work order template are set.

6.  Select **Submit**.


## Result

The work order template is enabled to create this task for different work orders if the defined filtering conditions match.

