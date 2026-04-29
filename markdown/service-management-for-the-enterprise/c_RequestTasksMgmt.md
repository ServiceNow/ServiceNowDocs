---
title: Request task management
description: A request contains one or more tasks. These tasks allow qualifiers to define activities that must be done to complete a request.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Request Management in a Service Management application, Service Management]
---

# Request task management

A request contains one or more tasks. These tasks allow qualifiers to define activities that must be done to complete a request.

Administrators can create multiple tasks under a single request.

Splitting a request into separate tasks, when necessary, enables qualifiers to do the following:

-   Assign different aspects of a request to different staff members.
-   Assign tasks to staff members who have different set of skills, or are in different locations.
-   Schedule tasks so they are either done one after another, or at the same time by different staff members.
-   Schedule additional tasks, if necessary, to complete the request.

**Note:** If you have the Request life cycle is request driven configuration option activated, you can manually add tasks as needed. If you have Request life cycle is task driven activated, an initial task is automatically created when the request record is created.

## Configuration Overview

Optionally, set up one or more additional request task management configurations:

-   [Task windows](../reference/r_TaskWindows.md)

    Set a task window to define the time period for performing the task by specifying the start and end dates.

-   [Create a task template for common task requests](../task/t_UseTaskTempForMultReqTemp.md)

    Create task templates to efficiently manage frequently repeated tasks across multiple jobs. By reusing these templates in various request templates, you save time and ensure consistency. Task templates can also be used in Work Order requests to automatically include common information, streamlining the process and minimizing errors.

-   [Clone a request task](../task/t_CloneARequestTask.md)

    Clone an existing task to save time and ensures consistency by allowing administrators to quickly replicate tasks while reducing errors and enabling easy customization.


-   **[Create request tasks](../task/t_CreateRequestTasks.md)**  
Tasks are created in support of requests.
-   **[Request task states](../reference/r_SMRequestTaskStates.md)**  
Like requests, the associated request tasks follow a specific life cycle and move through a series of states, which are displayed in the **State** field on the task record.
-   **[Task windows](../reference/r_TaskWindows.md)**  
A task window is the time period, bordered by start and end times, in which a task is performed.
-   **[Create a task template for common task requests](../task/t_UseTaskTempForMultReqTemp.md)**  
If you have tasks that are often repeated across multiple jobs, you can create and reuse a task template in multiple request templates. You can also use it on a Work order request to pull common and repeatable information into a request.
-   **[Clone a request task](../task/t_CloneARequestTask.md)**  
Existing tasks can be cloned to create tasks with the same populated fields.

**Parent Topic:**[Request Management in a Service Management application](rm-sm-application.md)

**Related topics**  


[Change the location of a request](../task/t_ChangeTheLocationOfARequest.md)

[Request approvals](c_RequestApprovals.md)

[Collaborate on a request](../task/t_CollaborateOnARequest.md)

[Close a request](../task/t_CloseARequest.md)

