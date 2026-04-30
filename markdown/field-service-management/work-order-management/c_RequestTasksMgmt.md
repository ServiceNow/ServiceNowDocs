---
title: Request task management
description: A request contains one or more tasks. These tasks allow qualifiers to define activities that must be done to complete a request.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
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


**Related topics**  


[Change the location of a request](https://www.servicenow.com/docs/access?context=t_ChangeTheLocationOfARequest&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US)

[Request approvals](https://www.servicenow.com/docs/access?context=c_RequestApprovals&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US)

[Collaborate on a request](https://www.servicenow.com/docs/access?context=t_CollaborateOnARequest&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US)

[Close a request](https://www.servicenow.com/docs/access?context=t_CloseARequest&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US)

