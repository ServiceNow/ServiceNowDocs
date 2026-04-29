---
title: Create dependencies between work order tasks
description: If a work order contains multiple tasks, you can create dependencies between the tasks that determine the order in which tasks are performed.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Create dependencies between work order tasks

If a work order contains multiple tasks, you can create dependencies between the tasks that determine the order in which tasks are performed.

## Before you begin

Role required: wm\_qualifier or [qualifier combination role](../reference/r_UserRoleInstallWFieldSrvMgmnt.md)

Activate the Field Service Task Dependency \(com.snc.fsm\_task\_dependency\) plugin to optionally define advanced task dependencies among work order tasks from different or same work order.

## About this task

These dependencies set and enforce the order in which a single agent or multiple agents perform the tasks. For example, on a work order for a new server, one agent might install the server, the upstream task, and a different agent might configure the server after installation is complete, the downstream task.

You can specify multiple dependencies for a single task. The system prevents circular relationships where two tasks are dependent on each other by considering all upstream dependencies when deciding if a task can be auto-assigned.

This table explains the types of task relationships and dependencies that you can create.

<table id="table_hvc_mfb_jdc"><thead><tr><th>

Dependency type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Finish to start

</td><td>

Indicates that the successor \(downstream\) task should be started after finishing its predecessor \(upstream\) task.This is the default dependency type between the tasks.

</td></tr><tr><td>

Start after start

</td><td>

Indicates that the successor \(downstream\) task must be started after starting its predecessor \(upstream\) task.Activate the Field Service Task Dependency \(com.snc.fsm\_task\_dependency\) plugin to define this relationship.

</td></tr><tr><td>

Start together

</td><td>

Indicates that the successor \(downstream\) and predecessor \(downstream\) tasks must be started together.Activate the Field Service Task Dependency \(com.snc.fsm\_task\_dependency\) plugin to define this relationship.

</td></tr></tbody>
</table>**Note:**

Dependencies can be created only when the predecessor and successor tasks are not assigned.

## Procedure

1.  Navigate to a work order.

2.  Open a work order task.

3.  In the **Depends on** or Dependants related list, click **New**.

4.  On the form, fill the fields.

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

</td></tr></tbody>
</table>5.  Click **Submit**.


## Server Installation and Configuration

Consider you have a work order for setting up a new server. There are three work order tasks involved: "Install Server", "Configure Server", and "Administer Server".![task dependency form](../../field-service-management/image/task-dependencies.png)

-   Install Server \(Predecessor or Upstream Task\): This task involves physically installing the server hardware.
-   Configure Server \(Successor or Downstream Task\): This task involves configuring the server software after the installation is complete.
-   Administer Server \(Successor or Downstream Task\): This task involves monitoring the server after installation and configuration.

To set up dependencies:

1.  Open the work order.
2.  Navigate to the work order task related list.
3.  Select the "Configure Server" task.
4.  In the "Depends on" related list, click "New".
5.  Choose "Install Server" as the Predecessor task \(upstream task\).
6.  In the "Dependants" related list, click "New".
7.  Select "Administer Server" as the Successor task \(downstream task\).
8.  Select the dependency type.
9.  \(Optional\) Enter the maximum or minimum lag time.
10. Click "Submit".

With this work order tasks dependency, the system requires the "Install Server" task to be completed before the "Configure Server" task can begin and start the "Administer Server" task after the configuration is complete.

