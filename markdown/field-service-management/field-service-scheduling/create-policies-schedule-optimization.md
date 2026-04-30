---
title: Create a policy for Schedule Optimization
description: Create policies to promote factors like the travel time and an agent's availability. Policies determine how to optimize an agent’s schedule based on defined objectives or constraints.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create a policy for Schedule Optimization

Create policies to promote factors like the travel time and an agent's availability. Policies determine how to optimize an agent’s schedule based on defined objectives or constraints.

## Before you begin

Role required: wm\_admin

## About this task

This video demonstrates how to create a policy for Schedule Optimization. 

Policies help achieve your optimization goals by combining objectives and constraints. Understanding your goals lets you customize optimization strategies.

For instance, if you have 20 technicians working in a city, you can set a policy to minimize travel time. By running optimization before the day begins, tasks are organized efficiently, reducing commute time. You can adjust existing policies by adding objectives and constraints to prioritize tasks and specify criteria for task assignment groups. For more information on objectives and constraints, see [Optimization features used with Schedule Optimization](../reference/hard-soft-constraints.md).

To use capacity with Schedule Optimization, you must enable **Capacity** in the constraint. For more information, see [Optimization features used with Schedule Optimization](../reference/hard-soft-constraints.md)

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

7.  Add an objective.

    1.  Select the **Objective** tab.

    2.  Select **New**.

    3.  In the **Optimization feature** field, select the Lookup using list icon \(![Lookup using list icon.](../../../common/image/List_SearchIcon.png)\) and select the objective to add.

    4.  Select **Submit**.

8.  Select **Update**.


## Result

You have now created a schedule optimization policy.

## What to do next

[Create a batch for Schedule Optimization](create-an-optimization-batch.md#).

