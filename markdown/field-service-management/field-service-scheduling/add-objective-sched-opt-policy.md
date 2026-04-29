---
title: Add objectives to a policy
description: Add objectives to Schedule Optimization policies to achieve additional optimization goals.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create policies, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Add objectives to a policy

Add objectives to Schedule Optimization policies to achieve additional optimization goals.

## Before you begin

Role required: wm\_admin

## About this task

Objectives set the goals of a Schedule Optimization policy and control how tasks are prioritized during optimization. The following default objectives are included in all policies and cannot be removed.

Default objectives:

-   Maximize task assignment: Ensures as many tasks as possible are scheduled by adding tasks to agent schedules to maximize productivity.
-   Minimize travel time: Reduces agent travel time by limiting the distance between tasks for all agents.

The following are examples of optional objectives that can be added to further customize optimization behavior.

Example optional objectives:

-   Maximize High-Priority Task Assignments: Prioritizes urgent tasks.
-   Minimize Under/Over-Skilled Agent Assignments: Matches task complexity with agent skill level.
-   Minimize Number of Shifts with Tasks: Limits the number of tasks per shift.
-   Minimize SLA Violations: Keeps service delivery within agreed time frames.
-   Minimize Overtime: Caps agent work hours within standard time ranges.
-   Maximize Balance in Tasks and Work Hours: Distributes tasks and hours evenly among agents.

**Note:** Objectives act as levers that adjust optimization to better suit your needs. For example, if Minimize Overtime is set as an objective, Schedule Optimization assigns tasks to agents during normal hours when possible. If that is not possible, tasks are assigned even if overtime is required. For a list of objectives, see [Objectives and constraints used with Schedule Optimization](../reference/hard-soft-constraints.md).

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Policies**.

2.  Select the policy.

3.  Select the **Objective** tab.

4.  Select **New**.

5.  In the **Optimization Features** field, select the Lookup icon \(![Lookup icon.](../../../common/image/List_SearchIcon.png)\) and select the objective to add.

6.  Select **Submit**.


