---
title: Select and assign multiple tasks
description: Dispatchers can select multiple tasks on which to run dynamic scheduling.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Assigning tasks using Dynamic Scheduling, Scheduling and dispatching, Use, Field Service Management]
---

# Select and assign multiple tasks

Dispatchers can select multiple tasks on which to run dynamic scheduling.

## Before you begin

Role required: wm\_dispatcher or wm\_admin

## About this task

If there has been an update to any of the selected tasks, an informational message notifies the dispatcher to run the recommendations again.

## Procedure

1.  Navigate to a list of work order tasks.

2.  Select the tasks that are pending for dispatch.

3.  From the **Actions on selected rows...** menu at the top of the list, select **Auto Assign**.

    **Note:** If more tasks are selected than dynamic scheduling can handle, a pop-up window displays a message to reduce the number of tasks.

4.  Select **Confirm**.


## Result

The system considers the time mentioned in the following fields before assigning a task to an agent.

-   **Scheduled travel start** and **Scheduled start** when `Ignore calculation of travel time for agents to task location based on schedule` is enabled.
-   **Estimated onsite arrival buffer duration** when `Enable/Disable Onsite Arrival Check-in for Agents` property is enabled. For more information, see [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md).
-   Agent's start and end locations are considered from the **Resource Schedule Attributes** table for the given day. For more information, see [Change schedule attributes for agents](change-agent-start-end-location.md).

The work order tasks are automatically assigned to an agent. If the agent does not accept the tasks in a specific time period, the work order tasks get auto rejected. The dispatcher can reassign the tasks to other available agents.

