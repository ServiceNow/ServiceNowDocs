---
title: Exclude Field Service agents from being assigned work order tasks
description: Exclude Field Service agents from being assigned work order tasks with dynamic scheduling, or Schedule Optimization.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing work order tasks, Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Exclude Field Service agents from being assigned work order tasks

Exclude Field Service agents from being assigned work order tasks with dynamic scheduling, or Schedule Optimization.

## Before you begin

Role required: wm\_dispatcher, wm\_manager, wm\_admin

If you’re using Technician Preferences for dynamic scheduling, then you must have the **Ignore Excluded Technician** criterion added to your task filter to add preferred technicians. For more information, see [Example - configure dynamic scheduling to ignore excluded technicians](prevent-excluded-agents.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Order Tasks**.

2.  Select the work order task that you want to exclude an agent from being assigned to.

3.  Select the **Technician Preferences** tab.

4.  Select **New**.

5.  Add the agent details and set **Assignment Preference** to **Excluded Agent**.

6.  Select **Submit**.

7.  Select **Update**.


**Parent Topic:**[Managing work order tasks](../../planning-and-policy/concept/c_WorkOrderTasks.md)

