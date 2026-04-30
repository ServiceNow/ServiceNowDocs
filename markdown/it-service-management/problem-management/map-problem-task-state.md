---
title: Map problem task states
description: Define how problem task records are updated when you migrate the records.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Migration job, Migration Utility, Configuring Problem Management, Problem Management, IT Service Management]
---

# Map problem task states

Define how problem task records are updated when you migrate the records.

## Before you begin

Role required: admin

## Procedure

1.  Provide the information for the mandatory fields at this stage.

    The mandatory field values are used when you apply new states to the existing problem task records.

    **Note:**

    -   The **Assigned to** field is used when the new state is beyond **151 - New** and the problem task is not already assigned to a user.
    -   If you have activated the problem state model plugin, you can assign only users with the problem\_task\_analyst, problem\_coordinator, problem\_manager or problem\_admin role.
    -   The $\{current.state\} variable is replaced with the current state value and label.
2.  Map all current problem task states to the new states.

    The following table provides an example of state mapping for the base system version of the problem task records:

    |Current state|New state|
    |-------------|---------|
    |-5 - Pending|151 - New|
    |1 - Open|151 - New|
    |2 - Work in Progress|154 - Work in Progress|
    |3 - Closed Complete|157 - Closed as Complete|
    |4 - Closed Incomplete|157 - Closed as Canceled|
    |7 - Closed Skipped|157 - Closed as Canceled|

3.  Click **Detect Unmapped States** to verify whether any state is not mapped.

    If any state is not mapped, you must provide a mapping.


## What to do next

[Activate Problem Management Best Practice — Madrid — State Model](activate-plugin-problem-management.md).

