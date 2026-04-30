---
title: Configure the Scheduled state
description: Administrators can optionally choose to enable the Scheduled state flow for work orders and work order tasks.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring work order tasks, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Configure the Scheduled state

Administrators can optionally choose to enable the Scheduled state flow for work orders and work order tasks.

## Before you begin

Role required: wm\_admin

## Procedure

1.  Navigate to **Field Service** &gt; **Administration** &gt; **Configuration**.

2.  Select the **Assignment** tab.

3.  Select **Use scheduled state**.

    **Note:** When **Dispatch queue** is turned off, Use scheduled state is automatically turned off. ​When **Dispatch queue** is enabled, Use scheduled state is NOT automatically enabled.

4.  Select **Save**.

5.  Navigate to **Field Service** &gt; **Administration** &gt; **Properties**.

6.  Scroll down to the **Update task state from Scheduled to Assigned when the scheduled start is within specified hours from current time** property and modify this property to define when a work order task should be dispatched \(move from Scheduled to Assigned\).

    The default number is 12, which means any task scheduled within the next 12 hours is in the Assigned state.

7.  Select **Save**.


## Result

-   On a work order form, the following occurs:
    -   A new state Scheduled appears between Ready For Dispatch and Assigned if qualification isn’t enabled.
    -   A new state Scheduled appears between Qualified and Assigned if qualification is enabled.
-   On a work order task form, a new state Scheduled appears between Pending Dispatch and Assigned.

**Note:** If you turn the **Use scheduled state** property off, a warning appears indicating that tasks have moved from Scheduled to Assigned. Consequently, all work order tasks that are in the Scheduled state are moved to the Assigned state.​

