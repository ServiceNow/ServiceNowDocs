---
title: Display the task assignment debug log
description: Display information from the task assignment debug log in the Confirm Assignment pop-up window.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Assigning work order tasks to agents using dynamic scheduling, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Display the task assignment debug log

Display information from the task assignment debug log in the Confirm Assignment pop-up window.

## Before you begin

Role required: admin

## About this task

System administrators can enable the **com.snc.dynamic.scheduling.showlogs** system property to display debug logs in the Confirm Assignment pop-up window. This information is displayed below each task. Collapse or expand the debug log by clicking on the task.

The task assignment debug log information is stored in the Log \[syslog\] table.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Go to the **com.snc.dynamic.scheduling.showlogs** property.

3.  Set the **Value** to **true**.

4.  Click **Update**.

    The Confirm Assignment pop-up window displays the debug logs for each of the selected tasks. Click the task to collapse or expand this information.


**Parent Topic:**[Assigning work order tasks to agents using dynamic scheduling](../concept/using-dynamic-scheduling.md)

