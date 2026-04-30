---
title: Track a certification task
description: Use the certification task state to track the progress of a task.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data certification performance, Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Track a certification task

Use the certification task state to track the progress of a task.

## Before you begin

Role required: admin

## About this task

The available task states are Work in Progress, Closed Complete, Closed Incomplete, and Cancelled.

When the state of a certification task changes, the certification instance state also changes in the following cases:

-   If any certification task is in Work in Progress state, the certification instance is placed in Work in Progress state.
-   If all certification tasks are in Cancelled state, the certification instance is placed in Cancelled state.
-   If all certification tasks are in Cancelled or Closed Complete state, the instance is placed in a Closed Complete state. For example, if three certification tasks are Cancelled, and one task is Closed Complete, the instance state is changed to Closed Complete.
-   When one certification task is Closed Incomplete and the remainder of the tasks are Cancelled or Closed Complete, the instance is placed in Closed Incomplete.

To view the state of certification tasks:

## Procedure

1.  Navigate to **All** &gt; **Data Certification** &gt; **Tasks** and select **My Tasks** or **All Tasks**.

2.  View the State column for each task.


