---
title: Cancel a work order task
description: The Cancel Task option is appropriate if a work order task is no longer necessary or is a duplicate of another work order task.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Execute work order tasks, Updating task status in web interface, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Cancel a work order task

The **Cancel Task** option is appropriate if a work order task is no longer necessary or is a duplicate of another work order task.

## Before you begin

Role required: wm\_agent

## About this task

Work orders and work order tasks cannot be canceled while in **Closed Complete** or **Closed Incomplete** state. When you cancel a work order task, the ServiceNow system automatically:

-   Cancels all associated transfer orders if the items have not already shipped. If the items have shipped, the system blocks the cancellation of the task until the parts are delivered.
-   Removes all predecessor \(upstream\) and successor \(downstream\) dependencies.
-   Changes the state of the parent work order to **Canceled** if all associated work order tasks are **Canceled**.
-   Removes all part requirements without a transfer order line.
-   Retains all asset usage information.
-   Sends a notification email and SMS to the customer about the cancellation of work order task.

Work order tasks can be canceled by users with these roles:

|Role|Description|
|----|-----------|
|Initiator|Can cancel a work order, which automatically cancels all associated work order tasks.|
|Qualifier|Can cancel work orders and work order tasks.|
|Dispatcher|Can cancel work orders and work order tasks.|
|Agent|Can cancel work order tasks assigned to them.|
|Field Service Management Administrator|Can cancel any active work order or work order task at any time.|

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Orders**.

2.  Open a work order.

3.  Open a work order task.

4.  In **Work notes**, enter a cancellation reason.

5.  Click **Cancel Task**.

    An error message appears if text is not entered into the **Work Notes** field.

    For traceability, auditing, and possible [deletion](t_DeleteAWorkOrder.md), field service administrators need to know the reason why a work order or work order task was canceled.


## Result

The customer receives an SMS and email notification that the work order task is canceled.

**Parent Topic:**[Execute work order tasks](../concept/c_ExecuteWorkOrderTasks.md)

