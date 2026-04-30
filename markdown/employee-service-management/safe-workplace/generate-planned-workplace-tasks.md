---
title: Generate planned workplace tasks
description: Using planned task definitions in Workplace Core to create planned tasks independent of shifts for recurring activities. For example, you can generate tasks for a selected number of days for cleaning all floors and buildings at midnight every day.
locale: en-US
release: xanadu
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing workplace tasks, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Generate planned workplace tasks

Using planned task definitions in Workplace Core to create planned tasks independent of shifts for recurring activities. For example, you can generate tasks for a selected number of days for cleaning all floors and buildings at midnight every day.

## Before you begin

Role required: sn\_wsd\_core.admin or sn\_wsd\_core.workplace\_manager

## About this task

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Workplace Tasks** &gt; **Planned Tasks Definitions**.

2.  In the list, open the planned task definition.

    You can also generate planned tasks immediately when you create a new planned task definition.

3.  Select **Planned start time** and **Planned end time** values based on the days and time when you need these tasks to be performed.

4.  Select **Generate now**.


## Result

-   Based on the planned start time and planned end time, planned tasks are created for all occurrences of the schedule and appear in the **Workplace Tasks** related list.
-   The **Expected start time** in each generated planned task is auto-calculated from the planned end time and processing time values in the respective tasks as follows:

    `Planned start time = Planned end time – Processing Time`


You can view all planned tasks by navigating to **Workplace Core** &gt; **Workplace Tasks** &gt; **Planned Tasks**.

**Parent Topic:**[Managing workplace tasks](workplace-maintenance-tasks.md)

