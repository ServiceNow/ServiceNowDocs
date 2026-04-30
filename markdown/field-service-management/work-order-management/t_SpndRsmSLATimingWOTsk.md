---
title: Suspend and resume SLA timing from a work order task
description: Pause and resume the timing on a work order SLA from a work order task.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SLAs, Templates, Work orders, Work orders and tasks, Configure, Field Service Management]
---

# Suspend and resume SLA timing from a work order task

Pause and resume the timing on a work order SLA from a work order task.

## Before you begin

Role required: wm\_admin, wm\_qualifier, wm\_dispatcher, wm\_agent, or a combination role

## About this task

This is useful for agents because it enables them to suspend the timing on the parent work order if they’re waiting for information or for others to perform actions.

## Procedure

1.  Navigate to a work order task with an SLA using the path visible to your role:

    -   **Field Service** &gt; **Work Order** &gt; **Work Order Tasks with SLAs**
    -   **Field Service** &gt; **Work Order** &gt; **My Work Order Tasks**
    -   **Field Service** &gt; **Work Order** &gt; **Assigned to me**
2.  Select an active work order task.

3.  Add a work note explaining why you’re suspending the work order.

4.  Under **Related Links**, select **Suspend Work Order**.

    The system sets the **Stage** of the SLA to **Paused**.

5.  Select **Resume Work Order** to restart the SLA.

    The system resets the SLA to its previous stage.


