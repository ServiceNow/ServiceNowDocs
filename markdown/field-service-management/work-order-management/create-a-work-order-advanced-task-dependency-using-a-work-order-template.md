---
title: Create advanced task dependency using a work order template
description: You can create work order templates that contain advanced task dependencies.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage work order tasks, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Create advanced task dependency using a work order template

You can create work order templates that contain advanced task dependencies.

## Before you begin

Role required: wm\_qualifier or [qualifier combination role](../../planning-and-policy/reference/r_UserRoleInstallWFieldSrvMgmnt.md)

Plugin required: Field Service Task Dependency \(com.snc.fsm\_task\_dependency\)

## About this task

If a work order contains multiple tasks, you can create advanced dependencies that establish a relationship between the tasks to determine the order in which tasks are performed.

You can create dependencies among tasks of the same work order template.

This table explains the types of advanced task relationships and dependencies that you can create.

|Dependency type|Description|
|---------------|-----------|
|Finish to start|Indicates that the successor \(downstream\) task should be started after finishing its predecessor \(upstream\) task.|
|Start after start|Indicates that the successor \(downstream\) task must be started after starting its predecessor \(upstream\) task.|
|Start together|Indicates that the successor \(downstream\) and predecessor \(downstream\) tasks must be started together.|

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Templates** &gt; **Work Order Template**.

2.  Create a new work order template.

3.  Navigate back to the list of work order templates.

4.  Select the work order template you created.

5.  In the **Service Order Task Template Dependencies** section, fill the form.

<table id="table_b2w_tjb_jdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Successor

</td><td>

Select a task whose start or end date is determined by its predecessor \(upstream\) task.

</td></tr><tr><td>

Dependency type

</td><td>

Select a dependency relationship from the drop down list. The available options are:-   Finish to start
-   Start after start
-   Start together


</td></tr><tr><td>

Use max lag time

</td><td>

Select the check box to allow the maximum lag time between the tasks.

</td></tr><tr><td>

Predecessor

</td><td>

Select a task which determines the start or end time of its successor \(downstream\) task.

</td></tr><tr><td>

Maximum lag time

</td><td>

Enter the maximum delay or waiting time between tasks.Maximum lag time is the maximum delay allowed between the start of predecessor and its successor tasks.

</td></tr><tr><td>

Minimum lag time

</td><td>

Enter the minimum delay or waiting time between tasks.Minimum lag time is the minimum delay allowed between the start of predecessor and its successor task.

</td></tr><tr><td>

Order model

</td><td>

This field displays the order model for the work order. This field can't be edited.

</td></tr></tbody>
</table>6.  Repeat this process for the remaining tasks.

7.  When you have defined the dependencies for all tasks, click **Submit**.

    After the work order task dependencies are defined, you can select the template when [creating a new work order](../../planning-and-policy/task/t_CreateAWorkOrder.md), and the tasks, along with the defined dependencies, will be inherited by the work order.


**Parent Topic:**[Manage work order tasks](../../planning-and-policy/concept/c_WorkOrderTasks.md)

