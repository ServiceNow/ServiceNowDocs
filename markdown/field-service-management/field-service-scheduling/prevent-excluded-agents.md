---
title: Example - configure dynamic scheduling to ignore excluded technicians
description: Add dynamic scheduling task filters to ensure that work order tasks are not assigned to agents who are excluded from the customer account.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Example - configure dynamic scheduling to ignore excluded technicians

Add dynamic scheduling task filters to ensure that work order tasks are not assigned to agents who are excluded from the customer account.

## Before you begin

Ensure that dynamic scheduling is selected as assignment method for tasks.

Role required: wm\_dispatcher, wm\_manager, wm\_admin

## About this task

Dispatchers or managers can override exclusions at any time by manually assigning work order tasks to excluded technicians. A warning message appears that the work order task has been assigned to an excluded agent.

## Procedure

1.  Navigate to **All** &gt; **Dynamic Scheduling Administration** &gt; **Configuration**.

2.  Select **Work OrderTask Dynamic Scheduling Config**.

3.  On the **Task Filters** tab, add the **Ignore Excluded Technician** criterion to the task filters.

    For information on adding criteria to a task filter, see [Create a task filter for dynamic scheduling](create-task-filter.md)

4.  Select **Update**.

    The dynamic scheduling matching criteria screens out the excluded agents from a particular account when the work order tasks are assigned using any of the following methods:

    -   [Auto assignment](select-tasks-for-bulk-assignment.md)
    -   [Managing appointments in Field Service Management](../concept/managing-appointments-fsm.md)

**Related topics**  


[Configure Field Service Management to use dynamic scheduling](dynamic-sched-config-field-service.md)

[Create a task filter](create-task-filter.md)

[Exclude Field Service agents from being assigned work order tasks](exclude-agents-from-being-assigned-tasks.md)

