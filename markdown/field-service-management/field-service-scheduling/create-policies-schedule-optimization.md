---
title: Create a policy for Schedule Optimization
description: Create policies to promote factors like the travel time and an agent's availability. Policies determine how to optimize an agent’s schedule based on defined objectives or constraints.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create a policy for Schedule Optimization

Create policies to promote factors like the travel time and an agent's availability. Policies determine how to optimize an agent’s schedule based on defined objectives or constraints.

## Before you begin

Role required: wm\_admin

## About this task

This video demonstrates how to create a policy for Schedule Optimization. 

A policy defines the rules and priorities that guide Schedule Optimization. Policies are built from objectives and constraints, which work together to determine how tasks are assigned to agents. Objectives control how tasks are prioritized during optimization, while constraints define the mandatory conditions an assignment group must meet to be considered for a task. See [Optimization Features](../reference/hard-soft-constraints.md) for the full list of objectives and constraints.

You can use different policies for different batch or intraday configurations.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Policies**.

2.  Select **New**.

3.  On the policy record form, provide a name and description.

4.  Select **Submit**.

5.  Select the policy you created.

6.  Add a constraint.

    1.  Select the **Constraint** tab.

    2.  Select **New**.

    3.  In the **Optimization feature** field, select the Lookup using list icon \(![Lookup using list icon.](../../../common/image/List_SearchIcon.png)\) and select the constraint to add.

    4.  Select **Submit**.

7.  Add additional objectives.

    Policies include default objectives that cannot be removed. You can add optional objectives to further customize optimization behavior.

    1.  Select the **Objective** tab.

    2.  Select **New**.

    3.  In the **Optimization feature** field, select the Lookup using list icon \(![Lookup using list icon.](../../../common/image/List_SearchIcon.png)\) and select the objective to add.

    4.  Select **Submit**.

    5.  In the **Objectives** list, double-click \(or use the keyboard shortcut\) the **Weight field** for the objective you added and enter an integer value.

    Schedule Optimization prioritizes higher-numbered weights. For default settings, apply a weight of 1. For more important factors, apply a weight of 2 or higher.

8.  Select **Update**.


## Result

You have now created a schedule optimization policy.

## What to do next

[Create a batch for Schedule Optimization](create-an-optimization-batch.md#).

**Related topics**  


[Add objectives to a policy](add-objective-sched-opt-policy.md)

[Add constraints to a policy](add-constraint-schedule-optimization-policy.md)

