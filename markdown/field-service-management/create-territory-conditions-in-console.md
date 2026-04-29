---
title: Enable identification of relevant territories for a work order or work order task
description: Enable identification of the most relevant territories for work orders or work order tasks by setting matching rules and conditions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Territory Planning Console, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Enable identification of relevant territories for a work order or work order task

Enable identification of the most relevant territories for work orders or work order tasks by setting matching rules and conditions.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner

## About this task

The Field Service Territory Planning configuration enables filtering of the most eligible territories for a work order or work order task. This configuration is stored in a matching rule that is based on the **Selection criteria** matching type.

The default configuration uses the **Field Service Territory Planning: Get eligible territories for Work Orders** and **Field Service Territory Planning: Get eligible territories for Work Order Tasks** matching rules, which use the following matching criteria:

-   Match Territory from Task Location
-   Filter based on Territory condition

You can also use matching rules for auto assignment if you create an assignment rule.

Create conditions to be able to filter and identify the most relevant territory for work orders or work order tasks.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  In the Territories panel, select a territory from the Browse All list.

3.  Select the **Actions** icon \(![Actions icon.](../image/more_actions.png)\) on the territory card and select **View Details**.

4.  Select **More** and then select **Territory Conditions**.

5.  Select **New**.

6.  On the form, fill in the fields.

<table id="table_rvf_vqh_ttb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Territory

</td><td>

Name of the territory.This field is automatically set to the selected territory.

</td></tr><tr><td>

Territory Model Source

</td><td>

Name of the source for which you want to filter the territory, either a work order or work order task.

</td></tr><tr><td>

Table Name

</td><td>

Either the Work Order Task \[wm\_task\] or Work Order \[wm\_order\] table.This field is automatically set based on the value selected in the **Territory Model Source** field.

</td></tr></tbody>
</table>7.  Add filter conditions.

    1.  In the **Condition** field, select **Set conditions**.

    2.  Create the condition.

        For example, **\[State\] \[is\] \[Pending Dispatch\] AND \[Active\] \[is\] \[true\]**.

    3.  Add an alternate OR condition by selecting **New condition set** and adding the conditions.

    4.  Select **Set**.

8.  Select **Save**.


## Result

The conditions to help determine the best matched territories for a work order or work order task are set.

