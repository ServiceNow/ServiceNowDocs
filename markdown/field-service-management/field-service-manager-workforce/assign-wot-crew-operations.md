---
title: Assign work order tasks to crews
description: Assign crews to work order tasks that require a group of agents to work on them.
locale: en-US
release: zurich
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Crew operations, Workforce, Use, Field Service Management]
---

# Assign work order tasks to crews

Assign crews to work order tasks that require a group of agents to work on them.

## Before you begin

If you are scheduling a task across multiple schedule entries or days, a work schedule must have been assigned to the crew. For more information, see [Create a work schedule for agents](../../customer-service-management/task/create-agent-work-schedule.md).

**Note:** If the crew schedule has not been defined and you are auto-assigning a task, the system uses the default schedule.

Role required: wm\_admin, wm\_dispatcher, and wm\_manager

## About this task

Key factors for task assignment:

-   Crew availability: Confirms the crew's availability \(effective dates\) aligns with task deadlines \(window start and end dates\).
-   Agent skills: Aligns specific skills needed for the task with those possessed by crew members.
-   Task requirements: Matches crew capabilities with task demands.
-   Territory Membership: Agent eligibility for task assignment is determined by their membership in the associated territory.

    **Note:** Territory Membership is available when the Territory Planning plugin is active and Territory Model is enabled.


Task assignment methods:

1.  Manual Assignment: The dispatcher selects the best crew for the task, ensuring their effective dates align with the task window start and end dates. The dispatcher also checks agent availability within the crew based on their territory membership dates.
2.  Dynamic Assignment: Dynamic Scheduling automatically assigns tasks to crews based on factors like crew availability, agent skills, and task requirements. If a suitable crew exists, it is assigned the task; otherwise, a new crew is created. When the dynamically created crew is assigned for a work order task within a territory, the crew membership is updated and appears in the Crew Membership related list of the territory.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Order Tasks**.

2.  Open the work order task for assignment.

3.  Select the **Needs Crew** check box if it is not already selected.

4.  If you need to schedule work order tasks spanning multiple schedule entries or days, select the **Assign across the schedule entries** check box if it isn’t already selected.

5.  Assign the task either manually or through auto-assignment.

<table id="choicetable_urr_4n2_yrb"><thead><tr><th align="left" id="d39760e150">

Option

</th><th align="left" id="d39760e153">

Description

</th></tr></thead><tbody><tr><td id="d39760e159">

**To assign a task manually**

</td><td>

1.  In the **Assigned Crew** field, select a crew available to work on the task.
2.  Select **Update**.


</td></tr><tr><td id="d39760e183">

**To auto-assign a task**

</td><td>

1.  Select **Auto Assign**.

The Confirm Assignment dialog box is displayed.

2.  Select **Confirm**.
 **Note:** If an available planned crew exists, then they're assigned the work order task. If no available crew exists, then one is created.

</td></tr></tbody>
</table>
## Result

The task is assigned to the crew. All crew members receive a push notification that the work order task is assigned. The Task Assignees table is added to the work order task for more information see, [Task assignees table for crew members or equipment](../reference/task-assignees-table.md).

