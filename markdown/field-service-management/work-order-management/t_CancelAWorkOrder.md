---
title: Cancel a work order
description: Cancel a work order if the work is no longer necessary or if it is a duplicate of another work order.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Cancel a work order

Cancel a work order if the work is no longer necessary or if it is a duplicate of another work order.

## Before you begin

Role required: Work orders can be canceled by users with different roles during specific states in the work order life cycle.

## About this task

When you cancel a work order, all associated work order tasks are also canceled.

Work orders and work order tasks cannot be canceled while in **Closed Complete** or **Closed Incomplete** state.

Work orders and work order tasks can be canceled by users with these roles:

|Role|Description|
|----|-----------|
|Initiator|Can cancel a work order, which automatically cancels all associated work order tasks.|
|Qualifier|Can cancel work orders and work order tasks.|
|Dispatcher|Can cancel work orders and work order tasks.|
|Agent|Can cancel work order tasks assigned to them.|
|Field Service Management Administrator|Can cancel any active work order or work order task at any time.|

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **All Work Orders**.

2.  Click the work order.

3.  In the **Work notes** field, enter a reason for canceling the work order.

    A reason is required for canceling work orders. If you do not provide a reason, an error message prompts you to enter one in the **Work notes** field.

4.  Click **Cancel**.


