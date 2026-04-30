---
title: Create a change task in Service Operations Workspace
description: When you need to engage another team or agent for help, create and assign change task. For example, there can be tasks to plan the change, implement the change, and test, and review the work.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Change Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a change task in Service Operations Workspace

When you need to engage another team or agent for help, create and assign change task. For example, there can be tasks to plan the change, implement the change, and test, and review the work.

## Before you begin

Role required: itil or admin

## Procedure

1.  Open a change request.

2.  On the change record page, Click the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Create Change Task**.

3.  In the Create Change task dialog box, select the task type.

    By default, the following task types are available. To create additional task types, see [Create a task type for problem or change in Service Operations Workspace](create-task-type-sow.md).

    -   Planning
    -   Implementation
    -   Testing
    -   Review
4.  Click **Create**.

5.  On the form, fill in the fields.

<table id="table_blp_xnl_sy"><thead><tr><th>

Name

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

A summary of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td>

Number

</td><td>

Auto-generated identification number for the task.

</td></tr><tr><td>

Change request

</td><td>

Associated change request.

</td></tr><tr><td>

State

</td><td>

State of the change task:-   **Pending**: Open and unassigned
-   **Open**: Open and unassigned
-   **In progress**: Open and actively being worked on
-   **Closed**: Inactive and closed. Requires close code and close notes to be provided.
-   **Canceled**


</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) or service that the change task applies to.

</td></tr><tr><td>

Type

</td><td>

Type of change task, **Planning**, **Implementation**, **Testing**, or **Review**. The default workflow generates tasks in type **Review**.

</td></tr><tr><td>

On hold

</td><td>

Option to indicate whether the change task is on hold. Provide an **On hold reason** if a change task is placed on hold.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group that the change task is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

User that the change task is assigned to. If an assignment rule applies, the change task is automatically assigned to the appropriate user or group.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Planned start date

</td><td>

Date you plan to begin working on the task.

</td></tr><tr><td>

Planned end date

</td><td>

Date the change task is planned to be completed.If the task type is **Implementation**, the **Planned start date** and **Planned end date** values must fall within the planned start and end dates specified in the change request.

</td></tr></tbody>
</table>6.  Click **Save**.


**Parent Topic:**[Change Management in Service Operations Workspace](../concept/change-sow.md)

**Related topics**  


[Create a change request in Service Operations Workspace](create-change-sow.md)

[Work on a change request in Service Operations Workspace](work-on-change-sow.md)

[Standard change catalog](../concept/standard-change-catalog-sow.md)

[Work on a change task in Service Operations Workspace](work-on-change-task-sow.md)

[Create a Change Advisory Board \(CAB\) definition](cm-create-cab-definition-sow.md)

[Create a CAB meeting](cm-create-cab-meeting-sow.md)

[Conduct a CAB meeting in the CAB workbench](cm-manage-cab-meeting-workbench-sow.md)

