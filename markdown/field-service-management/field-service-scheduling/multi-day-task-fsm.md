---
title: Assigning multi-day tasks to agents
description: With the Field Service multi-day task scheduling capability, you can schedule work-order tasks spanning multiple schedule entries or days.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Assigning multi-day tasks to agents

With the Field Service multi-day task scheduling capability, you can schedule work-order tasks spanning multiple schedule entries or days.

Multi-day task scheduling allows dispatchers to assign work order tasks, spanning across multiple schedule entries to agents or crews within their defined working hours. If they’re available throughout the task duration. Task schedulers can split work slots evenly throughout the day after considering the task duration, resource working and non-working hours, and resource availability throughout the task duration. Tasks can be assigned to the same agent or crew for multiple days or weeks by skipping the break and other non-working hours from their schedule.

This feature supports manual and dynamic scheduling methods to assign work order tasks to an agent or a crew using ServiceNow AI Platform and Dispatcher Workspace.

Field Service Multi-Day Task Scheduling uses the value of the **com.snc.wm.wo.task\_window\_days** property to calculate the estimated end date of the task based on the schedule of a selected agent or crew.

The following examples illustrate multi-day scheduling.

## Schedule a task within the same day

Task duration: four hours, Agent schedule: 08:00- 17:00, Excluded lunch break: 12:00-13:00.

The scheduler excludes break hours from the agent's work schedule while scheduling the task. Therefore, the task is scheduled to start at 10:00 and ends at 15:00. the same day, including multiple work schedules of two hours each and pre- and post-break hours of the agent's schedule.

## Schedule a task across multiple days

Task duration: 20 hours, Agent schedule: 08:00- 17:00, Excluded lunch break: 12:00- 13:00.

The scheduler excludes break hours from the agent's work schedule while scheduling the task. Therefore, the task is scheduled to start on Monday at 10:00 and end on Wednesday at 12:00, including multiple work schedules spanning three days. Each work schedule is estimated for four hours, including pre- and post-break hours of the agent's schedule.

-   **[Assign multi-day tasks to agents](../task/assign-multi-day-task.md)**  
Assign a work order task that requires multiple schedules or days to complete the job to a field service agent. This capability avoids having to create more than one task for the same job.

**Parent Topic:**[Scheduling and dispatching work order tasks to agents](scheduling-and-dispatching-agents.md)

**Related topics**  


[Activate Field Service Multi-Day Task Scheduling](../task/install-multi-day-tasks.md)

[Assign multi-day tasks to agents](../task/assign-multi-day-task.md)

[Assign work order tasks to crews on Dispatcher Workspace](../task/assign-wot-to-crew.md)

