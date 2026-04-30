---
title: Add workstation users to a Task Mining project
description: Select workstation users you want to collect activity data from and create data requests.
locale: en-US
release: yokohama
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2025-06-12"
reading_time_minutes: 1
breadcrumb: [Defining the scope of projects, Use, Task Mining, Platform Analytics]
---

# Add workstation users to a Task Mining project

Select workstation users you want to collect activity data from and create data requests.

## Before you begin

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

All data requests to collect data for the workstation users for a project must be approved before the project can begin.

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the name of the project you want to add workstation users to.

3.  Select the **Workstation users** tab.

    If the workstation user list is empty, no workstation users have been added to this project.

4.  Remove any users who were previously associated with the project that you no longer want to be included.

    1.  Select the workstation user.

    2.  Select the More Actions icon \(![More Actions icon](../../process-mining/image/po-ellipsis-purple.png)\).

    3.  Select **Delete**.

5.  Select **Add users**.

6.  Filter the user list by location or department.

7.  Select the workstation users that you want to add to this project, and select **Add**.

8.  Select **Save**.

9.  Obtain permission to collect a workstation user's data if no data request has been approved for that user.

    **Note:**

    If you want the request to be for a time period independent from a project, request workstation user data through an Employee Center data request. For more information, see [Requesting workstation user data](../concept/requesting-workstation-user-data.md).

    1.  In the list of workstation users, select any user for whom the **Data request status** is **Required**.

        If a workstation user's data request status is **Requested**, consider reviewing the request details and contacting the approver to urge action on the data request before the project is set to begin. For more information, see [Follow data request progress](manage-data-log-requests.md).

    2.  Select **Request data**.


## Result

A data request is sent to all managers of every workstation user. Once a data request is approved, **Approved** shows in the **Data request status** field and you can work with the workstation user data.

## What to do next

Group actions as a task for an Activity analysis. For more information, see [Define user actions for task logging](mine-data.md).

