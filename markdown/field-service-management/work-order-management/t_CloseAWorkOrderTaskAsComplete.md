---
title: Close a work order task as complete
description: Only agents can close work order tasks assigned to them.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Execute work order tasks, Updating task status in web interface, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Close a work order task as complete

Only agents can close work order tasks assigned to them.

## Before you begin

Role required: wm\_agent

## About this task

If the caller's problem was fixed or resolved, use the **Close Complete** option.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Agent** &gt; **Assigned to me**.

2.  Open a work order task.

3.  Add information to the **Work notes** field.

    The notes should include a description of the work done and any other helpful information.

4.  Enter a date and time earlier than the current date and time in the **Actual Work End** field.

    You cannot add a date and time later than the current date and time.

    If you do not enter a date and time, the ServiceNow system adds the current date and time automatically when you click **Closed Complete**.

5.  Click **Close Complete**.

    -   The status of all unused parts automatically changes to **In-Stock**.
    -   The state of the parent work order automatically changes to **Closed - Complete** if all work order tasks on the work order have a state of **Closed - Complete** or **Canceled**.

## Result

The customer receives SMS and email notification that the work order task is completed.

**Parent Topic:**[Execute work order tasks](../concept/c_ExecuteWorkOrderTasks.md)

