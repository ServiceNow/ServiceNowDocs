---
title: Create a task unassignment constraint
description: Dynamic scheduling allows you to define unassignment constraints that prevent certain tasks from being unassigned, even when lower in priority. This feature ensures that critical tasks stay assigned, based on dependencies or urgency.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure dynamic scheduling, Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create a task unassignment constraint

Dynamic scheduling allows you to define unassignment constraints that prevent certain tasks from being unassigned, even when lower in priority. This feature ensures that critical tasks stay assigned, based on dependencies or urgency.

## Before you begin

Role required: admin

## About this task

Unassignment constraints help control when tasks can or can’t be unassigned, ensuring that essential tasks remain assigned. This prevents disruptions, especially when tasks have dependencies or are time-sensitive. For example, a task nearing its SLA breach or one that requires sourced parts shouldn’t be unassigned, regardless of its relative priority in the task ordering rules.

Dynamic scheduling offers three predefined unassignment constraints:

1.  Task with downstream: Prevents unassignment if the task has downstream tasks that depend on it.
2.  Would breach SLA in the next five hours: Prevents unassignment if the task's Service Level Agreement \(SLA\) is expiring within five hours.
3.  Part sourced: Prevents unassignment if one or more parts required for the task have already been sourced.

Enabling the unassignment option in Dynamic Scheduling configuration allows the system to unassign tasks in favor of more important tasks \(as determined by task ordering rules\). However, unassignment constraints can prevent specific tasks from being unassigned, even if the task is of lower priority. If a task is unassigned and has downstream tasks, the downstream tasks are also unassigned and added to the pending dispatch queue.

Real-world use cases:

-   Healthcare: Prevent unassignment of critical medical equipment maintenance tasks nearing an SLA breach.
-   Manufacturing: Block unassignment of tasks that have sourced parts, ensuring resources are used efficiently.
-   Utilities: Keep emergency repair tasks assigned when downstream dependencies are involved.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

2.  In the **Un-Assignment Constraints** related list, click **New**.

3.  Click the lookup icon next to the **Constraint** field.

4.  In the Constraints list, click **New**.

5.  Fill in the fields on the Constraint form, as necessary.

<table id="table_gau_hat_ii"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The constraint name.

</td></tr><tr><td>

Task Table

</td><td>

Select the task table to which this constraint applies.

</td></tr><tr><td>

Type

</td><td>

Choose the type of constraint.-   **Simple**: Define a simple constraint by selecting a table, a task field, and one or more filter conditions.
-   **Advanced**: Define an advanced constraint by creating a script.


</td></tr><tr><td>

Constraint Table

</td><td>

Specify the table used to define the constraint on a task.

</td></tr><tr><td>

Task Field

</td><td>

Select the task field to which this constraint applies.

</td></tr><tr><td>

Constraint Condition

</td><td>

When this condition is true, it prevents task reassignment or unassignment.

</td></tr><tr><td>

Constraint Script

</td><td>

If using an advanced constraint, create a script to define the constraint details.

</td></tr></tbody>
</table>6.  Click **Submit**.

    The constraint is saved and returns you to the Un-Assignment Constraint form.

7.  Click **Submit**.

    The constraint is active and added to the configuration in the **Un-Assignment Constraints** related list.


## Result

This constraint prevents task unassignment based on the specified conditions, ensuring that tasks are not unassigned even if they have lower importance according to the task ordering rules.

