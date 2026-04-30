---
title: Pick up an unassigned task
description: Agents can assign themselves nearby unassigned tasks directly from the agent task map.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Execute a task from the agent map, Execute work order tasks, Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Pick up an unassigned task

Agents can assign themselves nearby unassigned tasks directly from the agent task map.

## Before you begin

Role required: wm\_agent.

## About this task

Agents can assign themselves nearby unassigned tasks directly from the agent task map. This might be necessary to complete a schedule when a another task is cancelled or a fixed [task window](t_CreateAWorkOrderTask.md) cannot be met. Make sure the task's scheduled start time and duration fit into your route and that the travel time is realistic. If the task does not fit into the available time slot in your schedule, the ServiceNow system blocks the assignment and displays a warning.

## Procedure

1.  To pick up an unassigned task, click a red icon near you and open the task record.

2.  Under **Related Links**, click **Assign to me**.

    If the task can be assigned to you, one of the following occurs:

    -   If you belong to more than one assignment group, you are asked to select a group. Only the assignment groups that belong to the dispatch group of the task are displayed.
    -   If you belong to only one assignment group, the system assigns the task to you and enters your assignment group in the Work Order Task form.
    If the assignment is allowed, the task state changes to **Accepted**, and the icon on the map turns green. In the task form, the **Start Travel** and **Start Work** links appear under **Related Links**.


**Parent Topic:**[Execute a task from the agent map](t_ExecuteATaskFromTheAgentMap.md)

