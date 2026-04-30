---
title: Agent auto assignment using priority assignment
description: The priority assignment feature enables you to configure auto assignment so that agents can be assigned to perform tasks or provide services on a continual, 24x7x365 basis. Priority assignment is triggered when the priority of a task matches the priority set in the application configuration page.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent auto assignment using time-based criteria, Agent auto assignment, Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Agent auto assignment using priority assignment

The priority assignment feature enables you to configure auto assignment so that agents can be assigned to perform tasks or provide services on a continual, 24x7x365 basis. Priority assignment is triggered when the priority of a task matches the priority set in the application configuration page.

Priority assignment can be used with location and skills settings. However, it can also operate independently.

To use priority assignment, you must set the following configuration options for the application.

|Field|Description|
|-----|-----------|
|Process life cycle|Set to **task driven \(subtasks are required\)**.|
|Assignment method for tasks|Set to **auto-assignment**.|
|Auto-selection of agents considers agent or task schedules|Enabled.|
|Enable priority assignment|Enabled.|
|Select priorities for assignment|Select one or more priorities.|

Only tasks of the selected priority or priorities trigger auto-assignment based on priority assignment.

When a task is qualified or marked as **Ready for Work**, and the priority of the task matches a priority selected for the application, the agent that best matches the schedule of the task is auto-assigned. If the location and skills options are enabled, agents are first evaluated on their physical proximity to the location of the task, and then on how their skills match the skills required to perform the task. The agent whose location, availability, and skills best match the requirements of the task is auto-assigned.

When a task has a priority that matches a priority in the priority assignment list, the Location Rating and Timezone Rating are ignored, even if they have been enabled.

If the priority of a task matches a priority selected in the **Select priorities for assignment** option, and no agents in the assignment group are available to be auto-assigned, the task is assigned to the group manager, regardless of whether the manager is available. It is the responsibility of the manager to locate an agent to perform the task.

**Note:** If no agent is located in the same time zone as the task, priority assignment fails.

**Parent Topic:**[Agent auto assignment using time-based criteria](c_AgAtAssgnTime.md)

