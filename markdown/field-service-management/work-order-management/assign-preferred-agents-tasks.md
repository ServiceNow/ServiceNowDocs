---
title: Set technician preferences for tasks
description: Specify the technician assignment preference for a task, indicating whether a technician is marked as Preferred, Secondary, Excluded, or Required for the work order task.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Set technician preferences for tasks

Specify the technician assignment preference for a task, indicating whether a technician is marked as Preferred, Secondary, Excluded, or Required for the work order task.

## Before you begin

Role required: wm\_dispatcher, wm\_manager, wm\_admin

If you’re using Technician Preferences for Dynamic Scheduling, then you must have the **Prioritize preferred and secondary technicians** criterion added to your task filter to add preferred technicians. For more information, see [Example - configure dynamic scheduling to assign preferred technicians to tasks](excluded-preferred-agents.md).

If you're using Technician Preferences for Schedule Optimization then your administrator must [Configure the policy to assign preferred technicians to tasks](configure-the-policy-to-assign-preferred-technicians-to-tasks.md).

## About this task

The system copies account preferences from the 'wm\_agent\_assignment\_preferences' table to the 'wm\_task\_tech\_preference' table whenever the account field on a WOT is updated. If the task is already created and the account information is added later, the system also copies the data into the task preferences table from the account agent preferences if they are maintained.

Technician Preferences are used by Dynamic Scheduling, and Schedule Optimization. With dynamic scheduling, technician preferences are considered when you assign the task in Dispatcher Workspace, or when you auto-assign the task. With Schedule Optimization, the technician preferences are considered when the optimization engine auto-assigns tasks.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Order Tasks**.

2.  Select the work order task that you want to add a preferred technician to.

3.  Select the **Technician Preferences** tab.

4.  Select **New**.

5.  Add the technician details and set the **Assignment Preference**.

<table id="table_h3z_5bd_xhc"><thead><tr><th>

Assignment Preference

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Preferred

</td><td>

Specify technician as preferred for task assignment. Optimization prioritizes these technicians when scheduling tasks, but other technicians may still be considered if necessary.

</td></tr><tr><td>

Secondary

</td><td>

Specify a secondary technician as a backup option for task assignment. This setting designates the technician as the second choice if the preferred technician is unavailable.

</td></tr><tr><td>

Excluded

</td><td>

Specify technicians to exclude from task assignment. These technicians will not be considered during Dynamic Scheduling or Schedule Optimization.For more information, see [Exclude Field Service technicians from being assigned work order tasks](exclude-agents-from-being-assigned-tasks.md)

</td></tr><tr><td>

Required

</td><td>

Specify technicians as required for task assignment. When set to Required, only these technicians can be assigned to the task, overriding all other assignment preferences.**Important:**

Required is only used by Schedule Optimization.

</td></tr></tbody>
</table>6.  Select **Submit**.


**Related topics**  


[Exclude Field Service technicians from being assigned work order tasks](exclude-agents-from-being-assigned-tasks.md)

