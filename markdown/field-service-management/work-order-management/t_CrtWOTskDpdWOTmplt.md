---
title: Create task dependency using a work order template
description: In addition to creating work order task dependencies that are inherited from the associated work orders, you can also create work order templates that contain task dependencies.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage work order tasks, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Create task dependency using a work order template

In addition to creating work order task dependencies that are inherited from the associated work orders, you can also create work order templates that contain task dependencies.

## Before you begin

Role required: wm\_qualifier or [qualifier combination role](../reference/r_UserRoleInstallWFieldSrvMgmnt.md)

## About this task

Like work order tasks created from work orders, the dependencies inherited from the template enforce the order in which a single agent or multiple agents perform the tasks.

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Templates** &gt; **Work Order Template**.

2.  Create a new work order template.

3.  Create the work order tasks.

4.  Open one of the tasks.

    -   If other tasks are dependent on this task; that is, this task must be completed before other tasks can be completed, click **Dependents** &gt; **New** and select the dependent tasks.
    -   If this task is dependent on other tasks; that is, other tasks must be completed before this task can be completed, click **Depends on** &gt; **New** and select the tasks to which this task is dependent.
5.  Repeat this process for the remaining tasks.

6.  When you have defined the dependencies for all tasks, click **Update**.

    After the work order task dependencies are defined, you can select the template when [creating a new work order](t_CreateAWorkOrder.md), and the tasks, along with the defined dependencies, will be inherited by the work order.


**Parent Topic:**[Manage work order tasks](../concept/c_WorkOrderTasks.md)

