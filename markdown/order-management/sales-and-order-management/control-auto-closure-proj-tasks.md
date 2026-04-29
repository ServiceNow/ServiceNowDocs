---
title: Control automatic closure of project tasks
description: Manage the automatic closure of projects in the SPM integration by using the sn\_ind\_tmt\_orm.project.task.auto.closure system property.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Strategic Portfolio Management integration, Order Management integration with Strategic Portfolio Management, Integrate, Sales and Order Management]
---

# Control automatic closure of project tasks

Manage the automatic closure of projects in the SPM integration by using the **sn\_ind\_tmt\_orm.project.task.auto.closure** system property.

## Before you begin

Role required: admin

## About this task

In the SPM integration, Order Management closes project tasks automatically when all associated order tasks are completed and there are no open child tasks that have project task dependencies. If a project task has open child tasks, Order Management doesn’t automatically close the project task. You can use the **sn\_ind\_tmt\_orm.project.task.auto.closure** property to suppress or reactivate the automatic closure of project tasks.

## Procedure

1.  Navigate to **All** and in the filter, enter `sys_properties.list` and press **Enter**.

2.  Search for and open the **sn\_ind\_tmt\_orm.project.task.auto.closure** property.

3.  In the **Value** field, set the value for the property.

    -   To suppress automatic project task closure, enter `false`.
    -   To reactivate automatic project task closure, enter `true`.
4.  Select **Update**.

    Automatic project task closure in the SPM integration is immediately suppressed or reactivated based on the value that you entered. If automatic closure is suppressed, any order task-to-project task updates occur only when order tasks are in an in-progress state.


