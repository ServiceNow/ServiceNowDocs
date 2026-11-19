---
title: Add objectives to a policy
description: Add objectives to Schedule Optimization policies to achieve additional optimization goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/field-service-management/field-service-scheduling/add-objective-sched-opt-policy.html
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

Objectives set the goals of a Schedule Optimization policy and control how tasks are prioritized during optimization. All policies include the Maximize task assignment and Minimize travel time objectives, and you can't remove them.

Objectives act as levers that adjust optimization to better suit your needs. For example, if you set Minimize Overtime as an objective, Schedule Optimization assigns tasks to technicians during normal hours when possible. If that isn't possible, it assigns tasks even if the technician must work overtime.

Example optional objectives:

-   Maximize High-Priority Task Assignments: Prioritizes urgent tasks.
-   Minimize Under/Over-Skilled Agent Assignments: Matches task complexity with technician skill level.
-   Minimize Number of Shifts with Tasks: Limits the number of tasks per shift.
-   Minimize SLA Violations: Keeps service delivery within agreed time frames.
-   Maximize Balance in Tasks and Work Hours: Distributes tasks and hours evenly among technicians.

For a full list of objectives, see [Objectives and constraints used with Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/field-service-management/hard-soft-constraints.md).

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Policies**.

2.  Select the policy.

3.  Select the **Objective** tab.

4.  Select **New**.

5.  In the **Optimization Features** field, select the Lookup icon \(\[Omitted image "List\_SearchIcon.png"\] Alt text: Lookup icon.\) and select the objective to add.

    **Note:**

    You can enable only one balance objective for each policy record.

6.  In the **Weight** field, enter a value.

    **Note:** Weight values must be integers greater than 0 and less than 100. Schedule Optimization prioritizes higher-numbered weights.

7.  Right-click the form header and select **Insert and Stay**.

    The record saves so you can add another objective.

8.  When you finish adding objectives, select **Submit**.


