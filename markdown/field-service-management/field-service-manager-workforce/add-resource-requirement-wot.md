---
title: Add resource requirements for a work order task
description: Add the resources needed to complete a crew work order task, such as necessary agent skills or equipment items, to avoid delays after the task is assigned.
locale: en-US
release: zurich
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Crew operations, Workforce, Use, Field Service Management]
---

# Add resource requirements for a work order task

Add the resources needed to complete a crew work order task, such as necessary agent skills or equipment items, to avoid delays after the task is assigned.

## Before you begin

-   The Equipment Scheduling plugin \(com.snc.fsm\_resource\_scheduling\) must be installed for you to be able to add any equipment-related requirement.

Role required: wm\_admin, wm\_dispatcher

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order Tasks**.

2.  Open the work order task.

    The task must be in the Draft or Pending Dispatch state.

3.  Select the **Needs crew** and **Resource requirements** options if they aren’t already selected.

4.  In the Resource Requirements related list, select **New**.

5.  On the form, fill in the fields.

6.  <table id="table_k42_n12_qvb"><thead><tr><th>

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

Type of resource required for the task, either agent or equipment.

</td></tr><tr><td>

Minimum quantity

</td><td>

Minimum number of resources required to work on the task.

</td></tr><tr><td>

Recommended quantity

</td><td>

Recommended number of resources required to work on the task.

</td></tr><tr><td>

Mandatory skills

</td><td>

Skills required to complete a task. For example, wiring and soldering.

</td></tr><tr><td>

Skill level

</td><td>

If a single skill is entered in the **Mandatory skills** field, define a level for the selected skill.**Note:** You can’t select a skill level for multiple skills.

</td></tr><tr><td>

Optional skills

</td><td>

Skills that are optional to complete a task.

</td></tr><tr><td>

Mandatory

</td><td>

Option to indicate whether the resource requirement is mandatory in order to complete a task.

</td></tr><tr><td>

Leader

</td><td>

Option to indicate that the resource requirement should be matched with available agents to determine the leader.

</td></tr></tbody>
</table>7.  Select **Submit**.


