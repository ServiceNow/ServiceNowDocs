---
title: Create an escalation trigger rule
description: Create a trigger rule to specify both the conditions under which an escalation process should begin and the actions \(workflow or script\) to perform for the escalation.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Designing an escalation process, Escalations in On-Call Scheduling, Defining On-Call Scheduling escalation process, On-Call Scheduling, IT Service Management]
---

# Create an escalation trigger rule

Create a trigger rule to specify both the conditions under which an escalation process should begin and the actions \(workflow or script\) to perform for the escalation.

## Before you begin

Role required: rota\_admin, admin, or rota\_manager

## About this task

-   Users with rota\_manager role can create escalation trigger rules \(with the **Trigger action** field set to **Workflow**\) only for the groups that are managed by the rota\_manager.
-   Users with rota\_admin role can create escalation trigger rules \(with the **Trigger action** field set to **Workflow** or **Subflow**\) for all the groups.
-   Users with admin role can create escalation trigger rules to execute **Workflow**, **Subflow**, and **Script** for all the groups.

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

Run Trigger

</td><td>

Frequency at which the trigger rule is run. Available values:-   Run once: Trigger rule is run only once.
-   Every time trigger field changes: Trigger rule is run every time the value of the **Trigger fields** field is changed.


</td></tr><tr><td>

Trigger fields

</td><td>

List of fields for a specific table which when changed causes the trigger rule to re-run. For example, for the incident table, you can select fields such as assignment group, priority and state.**Note:**

-   This field is visible only if the **Run Trigger** field is set to **Every time trigger field changes**.
-   You can use the Trigger Rule Table Configs table to configure which fields must be displayed for a specific table. For more information, see [Configure a table for escalation trigger rules](configure-tables-for-escalation-trigger-rule.md).


</td></tr><tr><td>

 

</td><td>

 

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

Conditions that must be met for the trigger rule to fire \(run the workflow or subflow or script that is the action for the rule\).

</td></tr><tr><td class="sub-head" colspan="2">

**What action to take**

</td></tr><tr><td>

Group

</td><td>

Group that becomes the **Task assignment group** when the trigger rule fires.**Note:**

-   This field is visible only when the **Trigger fields** field doesn’t contain the **Assignment group** value.
-   This field enables you to set the group level trigger rule. When this field is not set, or the **Trigger fields** field contain the **Assignment group** value, it becomes a global level trigger rule.


</td></tr><tr><td>

Trigger action

</td><td>

Action that is triggered when the **Match conditions** and **Conditions** are met. Possible values:-   Subflow
-   Workflow
-   Script \(server-side JavaScript\)
**Note:**

-   Starting Zurich release, the following options are available:
    -   For new users, the **Subflow** option is visible while the **Workflow** option is not visible.
    -   For existing or upgrade users, both the **Subflow** and **Workflow** options are visible, and either of them can be selected.
-   The **Script** option is available only for users with the rota\_admin and admin roles.
For more information, see [On-Call Scheduling subflows](../reference/on-call-scheduling-subflows-overview.md).

</td></tr><tr><td>

Trigger workflow

</td><td>

Workflow to run. Available only if **Trigger action** is set to **Workflow**.

</td></tr><tr><td>

Trigger subflow

</td><td>

Subflow to run. Available only if **Trigger action** is set to **Subflow**.**Note:** The following subflows under the On-Call Escalation Triggers category can be configured using the trigger rules:

-   On-Call: Assign
-   On-Call: Assign and Notify
-   On-Call: Assign By Acknowledgement
-   On-Call: Escalations by Email


</td></tr><tr><td>

Trigger script

</td><td>

Script \(server-side JavaScript\) to run. Available only if the **Trigger action** field is set to **Script**.**Note:** This action is available only for users with the rota\_admin and admin roles.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Designing an escalation process](../concept/designing-escalation-process-oncall.md)

