---
title: Add constraints to a policy
description: Constraints are requirements for the tasks that Schedule Optimization are assigned to agents.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a policy for Schedule Optimization, Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Add constraints to a policy

Constraints are requirements for the tasks that Schedule Optimization are assigned to agents.

## Before you begin

Role required: wm\_admin

## About this task

Constraints are added to policies and determine the criteria that need to be met for an assignment group to be assigned a task. For a list of the constraints, see [Optimization features used with Schedule Optimization](../reference/hard-soft-constraints.md).

Constraints are mandatory and tasks won't be assigned if the assignment group doesn't fit the constraint. They define the 'must-haves' for agents to even be considered for a task. Constraints are mandatory conditions embedded in policies. If an assignment group fails to meet a constraint, they're out of the running for that task. For example, if "Enable Mandatory Skills" is activated, only assignment groups with agents possessing the required skills will be considered for task assignments.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Policies**.

2.  Select the policy.

3.  Select the **Constraint** tab.

4.  Select **New**.

5.  In the **Optimization Features** field, select the Lookup icon \(![Lookup icon.](../../../common/image/List_SearchIcon.png)\) and select the constraint to add.

6.  Select **Submit**.


