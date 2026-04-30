---
title: Create a scope for Schedule Optimization
description: A scope defines the scheduling attribute configuration, horizon offset, horizon range, and qualifiers for an optimization run. Scopes are required for batch optimization to run.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create a scope for Schedule Optimization

A scope defines the scheduling attribute configuration, horizon offset, horizon range, and qualifiers for an optimization run. Scopes are required for batch optimization to run.

## Before you begin

Role required: wm\_admin

## About this task

This video demonstrates how to create a scope for Schedule Optimization 

When Territory Planning plugin is installed and the Territory Model is active, qualifiers are automatically set to territories and scopes for assignment groups are no longer possible. For more information, see .

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Scopes**.

2.  Select **New**.

3.  Enter a name in the **Name** field.

4.  Select a scheduling attribute configuration in the **Scheduling attribute** field.

5.  Set the **Assignment horizon offset** to specify the delay after the batch run before task assignments begin.

    **Note:** The assignment horizon offset determines the window start value on the work order task record.

6.  Set the **Assignment horizon range** to determine the span of time during which the tasks are assigned to the agents.

7.  Enter a priority in the **Rank** field to determine scope priority when tasks or tasks are shared between scopes.

    Lower numbers indicate a higher priority.

8.  Right-click the menu bar and select **Save**.

9.  In the **Qualifiers** related list, add assignment groups or territories to the scope.

    **Note:** Each assignment group must have a unique set of technicians. A technician cannot belong to more than one assignment group. Territory-based optimization supports overlapping technicians; assignment group-based optimization does not.

10. Select **Submit**.

    A Schedule Optimization scope is created.


