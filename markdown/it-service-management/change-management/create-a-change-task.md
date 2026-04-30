---
title: Create a change task
description: You can create change tasks for a change request. A change task is a piece of work related to the change request. For example, there can be tasks to plan the change, implement the change, and test, and review the work.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a change request, Using Change Management, Change Management, IT Service Management]
---

# Create a change task

You can create change tasks for a change request. A change task is a piece of work related to the change request. For example, there can be tasks to plan the change, implement the change, and test, and review the work.

## Before you begin

Role required: itil, admin, or sn\_change\_write

## About this task

Change tasks can be created manually or from a workflow. The Change Request form has a **Change Tasks** related list, which includes all manual and workflow change tasks. From this related list, you can edit existing tasks or create tasks. Workflow change tasks are generated automatically in **Review** task type.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Select the change request to add a change task.

3.  In the **Change Tasks** related list, click **New**.

4.  Fill in the fields, as appropriate.

<table id="table_blp_xnl_sy"><thead><tr><th>

Name

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Configuration item

</td><td>

The configuration item \(CI\) or service that the change task applies to.

</td></tr><tr><td>

Planned start date

</td><td>

The date you plan to begin working on the task.

</td></tr><tr><td>

Planned end date

</td><td>

The date the change task is planned to be completed.If the task type is **Implementation**, the **Planned start date** and **Planned end date** values must fall within the planned start and end dates specified in the change request.

</td></tr><tr><td>

Type

</td><td>

The type of change task, **Planning**, **Implementation**, **Testing**, or **Review**. The default workflow generates tasks in type **Review**.

</td></tr><tr><td>

State

</td><td>

The state of the change task:-   **Pending**: Open and unassigned
-   **Open**: Open and unassigned
-   **In progress**: Open and actively being worked on
-   **Closed**: Inactive and closed. Requires close code and close notes to be provided.
-   **Canceled**


</td></tr><tr><td>

On hold

</td><td>

The **On hold** check box indicates whether the change task is on hold. Provide an **On hold reason** if a change task is placed on hold.

</td></tr><tr><td>

Assignment group

</td><td>

The group that the change task is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

The user that the change task is assigned to. If an assignment rule applies, the change task is automatically assigned to the appropriate user or group.

</td></tr><tr><td>

Short description

</td><td>

A summary of the task.

</td></tr><tr><td>

Description

</td><td>

A detailed description of the task.

</td></tr></tbody>
</table>5.  To enter work notes for the change task, click the **Notes** tab.

6.  To enter notes on why the task was closed, click the **Closure Information** tab.

7.  Click **Submit**.

    The change task is added to the change request. The assigned user receives a notification that a task was assigned to them.


**Parent Topic:**[Create a change request](t_CreateAChange.md)

**Related topics**  


[Create a change request from a configuration item \(CI\)](t_CreateAChangeFromACI.md)

[Create a standard change request from the catalog](t_RaiseNewStdCngeFmTempl.md)

[Copy a change request](copy-a-change-request.md)

[Unauthorized change request](../concept/unauthorized-change-request.md)

