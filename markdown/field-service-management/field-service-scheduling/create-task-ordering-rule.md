---
title: Create a task ordering rule
description: Dynamic scheduling uses task ordering rules to prioritize and arrange tasks effectively. These rules ensure tasks are handled in the right sequence, helping you streamline field service operations.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure dynamic scheduling, Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create a task ordering rule

Dynamic scheduling uses task ordering rules to prioritize and arrange tasks effectively. These rules ensure tasks are handled in the right sequence, helping you streamline field service operations.

## Before you begin

Role required: admin

## About this task

Task ordering rules let you control how tasks are prioritized during scheduling. By defining rules, you can ensure that the most critical tasks are handled first, and tasks are ordered based on your organization’s specific needs. Multiple rules can be created and applied in a sequence, based on execution order, to give you maximum flexibility and precision.

How task ordering rules work:

-   Execution order: Rules are evaluated in order, with the rule having the lowest execution value taking precedence. For instance, you might create a rule that prioritizes tasks by urgency \(P1, P2, P3\). Another rule can be applied to organize tasks with the same priority by their SLA due date.
-   Task dependencies: Task dependencies can override task ordering rules. For example, downstream tasks cannot be assigned until upstream tasks are completed, ensuring proper task flow.
    -   If a task has downstream tasks, it cannot be unassigned.
    -   If an upstream task gets reassigned and a downstream task is assigned, the upstream task is scheduled before the downstream task starts.
    -   If an upstream task is unassigned, the downstream task remains unassigned.
    -   If an upstream task is assigned, the downstream task waits until the upstream task is completed.
    -   If an upstream task has a lower priority, the downstream task waits until the upstream task is assigned.

Types of task ordering rules

-   Simple rule
    -   Sorts tasks based on one selected field from the task table.
    -   Choose either ascending or descending sort order.
-   Advanced rule
    -   Sorts tasks based on selections from two unrelated tables.
    -   Requires a reference field to connect the task table and another table. For example, you can sort work order tasks based on SLAs stored in the Task SLA table.

Priority based ordering rules: Dynamic scheduling provides two priority based ordering rules.

-   Work order task priority: Uses the task's priority to determine task order, with a default execution order of 100.
-   Work order priority: Uses the overall work order's priority to determine task order, with a default execution order of 200.

Real-world use cases:

-   Healthcare: Prioritize equipment maintenance tasks based on the criticality of medical devices.
-   Manufacturing: Sort tasks by the cost of machine downtime per hour to reduce impact on production.
-   Retail: Use advanced rules to prioritize tasks by footfall, ensuring high-traffic stores are serviced first.
-   Utilities: Simple rules can prioritize emergency tasks, like power outages affecting critical infrastructure.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Dynamic Scheduling Configuration**.

2.  In the **Task Ordering Rules** related list, click **New**.

3.  Fill in the fields on the Task Ordering Rule form, as necessary.

    |Field|Description|
    |-----|-----------|
    |Name|The task ordering rule name.|
    |Execution Order|Specify the order in which this rule should be evaluated. The rule with the lowest value will determine the initial task order.|
    |Dynamic Scheduling Config|Select the dynamic scheduling configuration to which this ordering rule applies.|
    |Advanced|Select to create an advanced task ordering rule from different tables.|
    |Sort Table|Choose the table containing the tasks to be sorted.|
    |Sort Field|Select the field that will determine the task order.|
    |Sort Order|Choose ascending \(A-Z\) or descending \(Z-A\) order.|
    |Task Field|Specify the field on which the tasks will be sorted.|
    |Task Table|For an advanced ordering rule, this field displays the table that contains the tasks to be sorted.|
    |Connecting Task Field|For advanced rules, select the field that links the tables together.|
    |Aggregate Function|For advanced rules, choose an aggregate function like MIN, MAX, COUNT, etc.|

4.  Click **Submit**.

    The task ordering rule is created.


## Result

Dynamic scheduling will use this rule to prioritize tasks based on the criteria you’ve defined, ensuring that high-priority tasks are scheduled appropriately.

## What to do next

[Create a task unassignment constraint](create-unassignment-constraint.md)

