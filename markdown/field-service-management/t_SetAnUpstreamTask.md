---
title: Create dependencies between work order tasks
description: If a work order contains multiple tasks, you can create dependencies between the tasks that determine the order in which tasks are performed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing work order tasks, Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Create dependencies between work order tasks

If a work order contains multiple tasks, you can create dependencies between the tasks that determine the order in which tasks are performed.

## Before you begin

Role required: wm\_qualifier or [qualifier combination role](../reference/r_UserRoleInstallWFieldSrvMgmnt.md)

## About this task

These dependencies set and enforce the order in which a single agent or multiple agents perform the tasks. For example, on a work order for a new server, one agent might install the server, the upstream task, and a different agent might configure the server after installation is complete, the downstream task.

You can specify multiple dependencies, both upstream and downstream, for a single task. The system prevents circular relationships where two tasks are dependent on each other by considering all upstream dependencies when deciding if a task can be auto-assigned.

-   Setting a work order task as an upstream task means that this task must be completed before any downstream tasks can be started.
-   Setting a work order task as a downstream task means that this task cannot be started until any upstream tasks have been completed.

**Note:** Dependencies can only be set for work order tasks in the **Draft** state.

## Procedure

1.  Navigate to a work order.

2.  Open a work order task in the **Draft** state.

3.  In the **Depends on** related list, click **New**.

4.  Select either **Upstream task** or **Downstream task**.

    Only tasks for the same work order are listed.

5.  Click **Submit**.


## Server Installation and Configuration

Consider you have a work order for setting up a new server. There are two work order tasks involved: "Install Server" and "Configure Server".

-   Install Server \(Upstream Task\): This task involves physically installing the server hardware.
-   Configure Server \(Downstream Task\): This task involves configuring the server software after the installation is complete.

To set up dependencies:

1.  Open the work order.
2.  Navigate to the work order task related list.
3.  Select the "Configure Server" task.
4.  In the "Depends on" related list, click "New".
5.  Select "Upstream Task" and choose "Install Server" as the upstream task.
6.  Click "Submit".

With this work order tasks dependency, the system requires the "Install Server" task to be completed before the "Configure Server" task can begin.

**Parent Topic:**[Managing work order tasks](../concept/c_WorkOrderTasks.md)

