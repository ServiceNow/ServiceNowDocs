---
title: Map problem states
description: Define how problem records are updated when you migrate the records.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migration job, Migration Utility, Configuring Problem Management, Problem Management, IT Service Management]
---

# Map problem states

Define how problem records are updated when you migrate the records.

## Before you begin

Role required: admin

## Procedure

1.  Provide information for all the mandatory fields at this stage.

    The required field values are used when you apply new states to the existing problem records.

    **Note:**

    -   The **Assigned to** field is used when the new state is beyond **101 - New** and the problem is not already assigned to a user.
    -   If you have activated the problem state model plugin, the **Assigned to** field is filtered to users with the problem\_coordinator, problem\_manager or problem\_admin role.
    -   The $\{current.state\} variable is replaced with the current state value and label.
2.  Map all current problem states to the new states.

    The following table provides an example of state mapping for the base system version of the problem records:

    |Current state|New state|
    |-------------|---------|
    |1 - Open|101 - New|
    |2 - Known Error|107 - Closed as Risk Accepted|
    |3 - Pending Change|104 - Fix in Progress|
    |4 - Closed/Resolved|107 - Closed as Fix Applied|

3.  Click **Detect Unmapped States** to verify whether any state is not mapped.

    If any state is not mapped, you must provide a mapping.


## What to do next

[Map problem task states](map-problem-task-state.md).

