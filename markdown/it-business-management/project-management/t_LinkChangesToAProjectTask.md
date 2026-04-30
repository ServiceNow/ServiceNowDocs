---
title: Link change requests to a project task
description: Link change requests to tasks on the Project Task form. You can link change requests only to project tasks that have no child tasks.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Change requests and project tasks, Project tasks, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Link change requests to a project task

Link change requests to tasks on the Project Task form. You can link change requests only to project tasks that have no child tasks.

## Before you begin

Role required: it\_project\_manager

## About this task

You can link any change request record to a project task, regardless of the change request schedule or state. However, as a good practice, consider:

-   **Change Schedule:** The change request has a schedule that falls within the time frame of the project it links to. Or, it has no values in the **Planned start date** and **Planned end date** fields in the **Schedule** section of the Change Request form.
-   **Change State:** An **Open** or **Pending** state is required when linking a change request. Changes that are already in progress or closed can be stopped and copied to a new change request.

## Procedure

1.  Open a project task that does not have any child tasks.

    Tasks that already have child tasks cannot be linked to change requests.

2.  Click one of the following related links:

    -   **Link an Existing Change Request to Project Task**:

        In the dialog box that appears, enter or select the change that you want to link.

    -   **Create Change and link from Project Task**:

        The Change Request form appears. Enter the information in the form. The short description of the change request is taken from the project task.

    **Note:** These related links are available only when the project task type is waterfall.


## Result

On the Project Task form, a notification appears at the top specifying that the task is linked to one or more change requests.

![screenshot for task with Linked Change](../image/TaskWithLinkedChange "Example for Task designated for linked change requests in the related list")

**Parent Topic:**[Change requests and project tasks](../concept/c_ChangeRequestsAndProjectTasks.md)

