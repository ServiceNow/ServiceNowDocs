---
title: Qualify a work order
description: When a work order is assigned to you for qualification, review and qualify its tasks to ensure that they contain enough information for the groups that are dispatched to work on them. Qualifying work order tasks is required only when Field Service Management is configured for manual qualification.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Qualify a work order, Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Qualify a work order

When a work order is assigned to you for qualification, review and qualify its tasks to ensure that they contain enough information for the groups that are dispatched to work on them. Qualifying work order tasks is required only when Field Service Management is configured for manual qualification.

## Before you begin

Role required: wm\_qualifier

## About this task

If Field Service Management is configured for automatic qualification, you do not need to complete this process. Work orders are automatically qualified and tasks are automatically created for them. For details on manual and automatic qualification, see [Qualify a work order](../concept/c_QualifyWorkOrders.md).

On the Work Order form, you can qualify tasks from the Work Order Tasks related list. You can qualify a single task or multiple tasks at the same time. While you qualify a single task, you can also qualify any sibling tasks, which are different tasks that are related to the same order.

**Note:** If Field Service Management is configured to automatically assign tasks, you must also select a dispatch group for each work order task. If you do not select a dispatch group, you are prompted to select one before you can qualify the task.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **Awaiting Qualification**, and click a work order.

    If you do not see the **Awaiting Qualification** module, Field Service Management is configured for automatic qualification.

2.  To qualify a single work order task and any of its sibling tasks:

    1.  In the Work Order Tasks related list, click the task.

    2.  On the Work Order Task form, click **Qualified**.

    3.  From the Sibling Tasks related list, qualify any sibling tasks.

        You can either click a single sibling task to qualify, or select multiple sibling tasks from the list to qualify. After you select multiple tasks, select **Qualified** from the **Actions** choice list.

3.  To qualify multiple work order tasks:

    1.  In the Work Order Tasks related list, select the check box next to each task.

    2.  From the **Actions** choice list, select **Qualified**.


