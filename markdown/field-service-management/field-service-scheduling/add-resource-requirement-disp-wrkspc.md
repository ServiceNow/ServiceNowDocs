---
title: Add resource requirement for a work order task in Dispatcher Workspace
description: Add or update the resource requirements for a task that requires a crew, such as the number of agents with specific skills or equipment required to work on the task.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Crew operations, Using Dispatcher Workspace, Assigning tasks from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Add resource requirement for a work order task in Dispatcher Workspace

Add or update the resource requirements for a task that requires a crew, such as the number of agents with specific skills or equipment required to work on the task.

## Before you begin

-   You must select the **Needs crew** and **Resource requirements** options in the work order task.

    **Note:** The Resource requirements option displays only when the **Needs Crew** option is selected.

-   You must activate the Equipment Scheduling plugin \(com.snc.fsm\_resource\_scheduling\) to add any equipment-related requirement.

Role required: wm\_admin, wm\_dispatcher

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  Open a work order task that is in the Draft or Pending Dispatch state for which you want to configure the resource requirement.

    For more information, see [Search for tasks that need a crew on Dispatcher Workspace](search-crew-task.md).

4.  Select the **Resource requirement** option if not already selected, and then select **Save**.

5.  In the Resource Requirements related list, select **New**.

6.  On the form, fill in the fields.

7.  <table id="table_k42_n12_qvb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the type of resource category. For example, electrician.

</td></tr><tr><td>

Resource type

</td><td>

Type of resource required for the task, either agent or equipment.**Note:** The equipment option is available only if the Equipment Scheduling plugin \(com.snc.fsm\_resource\_scheduling\) is activated.

</td></tr><tr><td>

Minimum quantity

</td><td>

Minimum number of resources required to work on the task.

</td></tr><tr><td>

Recommended quantity

</td><td>

Actual number of resources required to work on the task.

</td></tr><tr><td>

Mandatory skills

</td><td>

Skills that are mandatory to complete a task. For example, wiring.

</td></tr><tr><td>

Skill level

</td><td>

Define a level for the selected skill.

</td></tr><tr><td>

Optional skills

</td><td>

Skills that are optional to complete a task.

</td></tr><tr><td>

Mandatory

</td><td>

Option to identify if the skills are mandatory to complete a task.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

The resource requirement is added to the work order task that requires a crew.

