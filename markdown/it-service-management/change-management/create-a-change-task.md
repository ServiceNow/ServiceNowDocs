---
title: Create a change task
description: You can create change tasks for a change request. A change task is a piece of work related to the change request. For example, there can be tasks to plan the change, implement the change, and test, and review the work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/change-management/create-a-change-task.html
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a change request, Using Change Management, Change Management, IT Service Management]
---

# Create a change task

You can create change tasks for a change request. A change task is a piece of work related to the change request. For example, there can be tasks to plan the change, implement the change, and test, and review the work.

## Before you begin

Before creating a change task, confirm you have the required roles. If not, contact your administrator to request access.

Role required: itil, admin, or sn\_change\_write

## About this task

Change tasks can be created manually or from a workflow. The **Change Tasks** related list is displayed by default and includes all manual and workflow-generated change tasks.

To edit existing tasks or create tasks, from the **Related Links** section, select the **Change Tasks** tab and then select **New**.

If the Change task related list is not visible, scroll down the change form or verify that your role has permission to view it. If the list is still not visible, contact your IT administrator to verify your permissions and form configuration.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Select the change request to add a change task.

3.  In the **Related Links** section, select **Change Tasks** tab and then, select **New**.

4.  To associate an existing change task with the change request, open the change task record and update the **Change** field to the target change request and save the record.

    **Note:** The **New** button creates a change task and doesn't attach an existing change task. To carry tasks to the new change request, [Copy a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/copy-a-change-request.md)

5.  Fill in the fields, as appropriate.

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

The type of change task, **Planning**, **Implementation**, **Testing**, or **Review**. The default workflow generates tasks in type **Planning**.

</td></tr><tr><td>

State

</td><td>

The state of the change task:-   **Pending**: Not yet ready to be worked on. Waiting for a predecessor task to complete or for the scheduled start time.
-   **Open**: Ready to be worked but not yet started.
-   **In progress**: Actively being worked on.
-   **Closed**: Inactive and closed. Set the **Close code** and **Close notes** fields before you move the task to **Closed**.
-   **Canceled**: No longer required. The task is closed without being completed.


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
</table>6.  To enter work notes for the change task, select the **Notes** tab.

7.  To record the reasons for closing a task, select the **Closure Information** tab and set the **Close code** and **Close notes** fields.

    Each change task is closed individually. The **Close code** applies to the current change task and not to other change tasks on the change request.

    **Important:**

    Close codes and close notes apply to individual change tasks only and do not affect other change tasks on the change request. Once you submit or close a change task, you cannot revert it to an earlier state, such as **Open** or **In Progress**.

8.  Select **Submit**.

    The change task is added to the change request. The assigned user receives a notification that a task was assigned to them.


**Parent Topic:**[Create a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/t_CreateAChange.md)

**Related topics**  


[Create a change request from a configuration item \(CI\)]()

[Create a standard change request from the catalog]()

[Copy a change request]()

[Unauthorized change request]()

