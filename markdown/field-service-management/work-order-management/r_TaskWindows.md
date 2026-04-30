---
title: Task windows
description: A task window is the time period, bordered by start and end times, in which a task is performed.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring request task management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Task windows

A task window is the time period, bordered by start and end times, in which a task is performed.

Task windows can be flexible or fixed, and are used by the route optimization and auto-dispatch features when determining the daily schedule of staff members. A flexible window has start and end times that the application attempts to respect when dispatching or routing a task automatically. The system can reschedule a flexible task window if necessary, to make it fit into the schedule of a staff member. A fixed task window cannot be rescheduled. If the auto-router that optimizes task routes or the auto-dispatcher cannot schedule the task for the fixed window time period, that task is not scheduled at all. The time interval configured for a window cannot be less than the time required to perform the task.

For more information on creating work order tasks, see [Create a work order task](../task/t_CreateAWorkOrderTask.md).

For more information on Work order task start and end dates, see [Work order task start and end dates](../../field-service-management/reference/dynamic-sched-task-window-dates.md).

