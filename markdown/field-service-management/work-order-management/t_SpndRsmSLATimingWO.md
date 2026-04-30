---
title: Suspend and resume SLA timing from a work order
description: Pause and resume the timing on a work order SLA from the work order.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SLAs, Templates, Work orders, Work orders and tasks, Configure, Field Service Management]
---

# Suspend and resume SLA timing from a work order

Pause and resume the timing on a work order SLA from the work order.

## Before you begin

Role required: wm\_admin, wm\_initiator, wm\_qualifier, wm\_dispatcher, or a combination role

## About this task

This is useful if a qualifier or dispatcher is waiting for information from the caller or for other actions to take place before continuing the work order.

**Note:** Initiators can’t view the SLAs attached to the work orders they suspend or resume.

## Procedure

1.  Navigate to a work order with an SLA using the path visible to your role:

    -   **Field Service** &gt; **Work Order** &gt; **Work Order SLAs**
    -   **Field Service** &gt; **Work Order** &gt; **Awaiting Qualification**
    -   **Field Service** &gt; **Work Order** &gt; **Draft Work Orders**
2.  Select an active work order.

3.  On the work order record, add a work note explaining why the work order is suspended.

4.  Select **Suspend**.

    ![suspend work order button](../../field-service-management/image/suspend-order.png)

    The system sets the **Stage** of the SLA to **Paused**.

5.  Select **Resume** to restart the SLA.

    The system resets the SLA to its previous stage.


