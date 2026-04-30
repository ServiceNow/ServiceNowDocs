---
title: Add objectives to a policy
description: Add objectives to the default objectives in Schedule Optimization policies to achieve additional goals.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a policy for Schedule Optimization, Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Add objectives to a policy

Add objectives to the default objectives in Schedule Optimization policies to achieve additional goals.

## Before you begin

Role required: wm\_admin

## About this task

Objectives serve as the compass that guides task prioritization in Schedule Optimization. Objectives set the goals of a Schedule Optimization policy. Each objective is weighted and Schedule Optimization prioritizes higher-numbered weights. For default settings, apply a weight of 1, and for more important factors, such as Maximizing high-priority task assignments, apply a weight of 2.The following are the default and optional objectives in Schedule Optimization.

Default objectives

-   Maximize task assignment- Focused on ensuring as many tasks as possible are scheduled. Adds as many tasks as possible to agent schedules to maximize productivity.
-   Minimize travel time- Targeted at reducing agent travel time. Limits the travel time between tasks for all agents.

**Note:** These objectives are default and cannot be removed from your policies.

Optional objectives

-   Maximize High-Priority Task Assignments: Prioritizes urgent tasks.
-   Minimize Under/Over-Skilled Agent Assignments: Matches task complexity with agent skill level.
-   Minimize Number of Agents with Assignments: Limits the number of tasks per agent per shift.
-   Minimize SLA Violations: Keeps service delivery within agreed timeframes.
-   Minimize Overtime: Caps agent work hours within standard time ranges.
-   Maximize Balance in Tasks &amp; Work Hours: Distributes tasks and hours evenly among agents.

**Note:** Objectives are optional but act as levers, adjusting your optimization to better suit your needs. For example, if Minimize overtime is set as an objective, Schedule Optimization will try to assign tasks to agents during normal hours. If that's not possible, tasks will be assigned to agents even if it will require overtime. For a list of the objectives, see [Optimization features used with Schedule Optimization](../reference/hard-soft-constraints.md).

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Policies**.

2.  Select the policy.

3.  Select the **Objective** tab.

4.  Select **New**.

5.  In the **Optimization Features** field, select the Lookup icon \(![Lookup icon.](../../../common/image/List_SearchIcon.png)\) and select the objective to add.

6.  Select **Submit**.


