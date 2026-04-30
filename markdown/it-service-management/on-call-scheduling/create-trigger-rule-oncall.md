---
title: Create an escalation trigger rule
description: Create a trigger rule to specify both the conditions under which an escalation process should begin and the actions \(workflow or script\) to perform for the escalation.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Designing an escalation process, Escalations in On-Call Scheduling, Define escalation process, On-Call Scheduling, IT Service Management]
---

# Create an escalation trigger rule

Create a trigger rule to specify both the conditions under which an escalation process should begin and the actions \(workflow or script\) to perform for the escalation.

## Before you begin

Role required: rota\_admin, admin, or rota\_manager

## About this task

-   Users with rota\_manager role can create escalation trigger rules \(with the **Trigger action** field set to **Workflow**\) only for the groups that are managed by the rota\_manager.
-   Users with rota\_admin role can create escalation trigger rules \(with the **Trigger action** field set to **Workflow**\) for all the groups.
-   Users with admin role can create escalation trigger rules to execute both **Workflow** and **Script** for all the groups.

## Procedure

1.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **Administration** &gt; **Trigger Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ryc_4ys_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and meaningful name for the trigger rule.

</td></tr><tr><td>

Table

</td><td>

Task table that applies to the trigger rule.

**Note:**

-   Only tables and database views that are in the same scope as the trigger rule appear in the list.
-   Tables that do not extend tasks do appear in the list only if those tables are configured for trigger rules in the [Trigger Rule Table Configuration](configure-tables-for-escalation-trigger-rule.md) \[trigger\_rule\_table\_cfg\] table.
.

</td></tr><tr><td>

Execution order

</td><td>

Run order of the trigger rule.

</td></tr><tr><td>

Active

</td><td>

Option to activate the trigger rule.

</td></tr><tr><td class="sub-head" colspan="2">

**When to activate**

</td></tr><tr><td>

Trigger when group assigned changes

</td><td>

Option to process the trigger rule only when the **Group** field value in the table is changed.-   **False**: Trigger rules fire only if the**assigned\_to** and **assignment\_group** fields are not populated on a record.
-   **True**: Trigger rules fire only if group field populated or changes and **assigned\_to** is not populated on a record.


</td></tr><tr><td>

Trigger when

</td><td>

Type of trigger for the table that is the default behavior or conditional.This field is available only when the **Trigger when group assigned changes** check box is enabled.

 -   **Condition matches**: Triggers escalation when conditions match.
-   **Default**: Triggers escalation based on only the **Trigger action** field value.


</td></tr><tr><td>

Match conditions

</td><td>

Conditions type to match before triggering escalation. -   **All**: Each condition must be met.
-   **Any**: Any one of the conditions can be met.


</td></tr><tr><td>

Conditions

</td><td>

Conditions that must be met for the trigger rule to fire \(run the workflow or script that is the action for the rule\).

</td></tr><tr><td class="sub-head" colspan="2">

**What action to take**

</td></tr><tr><td>

Group

</td><td>

Group that becomes the **Task assignment group** when the trigger rule fires.This field is available only when the **Trigger when group assigned changes** check box is cleared.

</td></tr><tr><td>

Trigger action

</td><td>

**Workflow** or **Script** \(server-side JavaScript\) to execute when the **Match conditions** and **Conditions** are met.

</td></tr><tr><td>

Trigger workflow

</td><td>

Workflow to execute. Available only if **Trigger action** is set to **Workflow**.

</td></tr><tr><td>

Trigger script

</td><td>

Script \(server-side JavaScript\) to execute. Available only if the **Trigger action** field is set to **Script**.**Note:** This action is available only for users with the rota\_admin and admin roles.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Designing an escalation process](../concept/designing-escalation-process-oncall.md)

