---
title: Create a DevOps change request and associate existing DevOps data — Classic
description: Create a DevOps change request and associate existing DevOps data through the Classic UI.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Create a DevOps change request and associate existing DevOps data — Classic

Create a DevOps change request and associate existing DevOps data through the Classic UI.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.app\_owner

## About this task

Create a DevOps change request and associate existing DevOps data. You can modify the associated details after you have created a DevOps change and associated data with it.

**Important:** If the Change request is in one of the following states, the **Edit DevOps Data** button is inactive:

-   Implement
-   Post-Implement
-   Cancelled

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Create New** &gt; **Create Normal Change**.

    **Note:** For more information on using the Change module, see [Create a Change](../../change-management/task/t_CreateAChange.md).

2.  From the **Category** list, select DevOps or Other.

3.  Select the **DevOps Change** option, if you have selected Other in the **Category** field.

4.  Click the **Add DevOps Data** button on the form header.

    **Note:** The **Add DevOps Data** button appears only if you have selected DevOps as the category, or Other as the category and selected the **DevOps Change** option.

    The **Add DevOps Data** modal displays.

5.  In the **Select data type and associations** section, select the data type and the related data associations.

    1.  Select any of the following options from the **Data Type** list.

        -   Artifact Version
        -   Release Version
        -   Build Number
        **Note:** You can select multiple Artifact versions and Build Numbers.

    2.  Select the data you want to associate with the change from the **Artifact Version**, **Release Version** or **Build Number** field.

        **Important:** If you select Build Number as the **Data Type**, you must also specify the application name, and corresponding pipelines and build numbers. You can search for build numbers by the branch name as well.

6.  Click **Next**.

7.  Verify that the associated data for the following fields is mapped accurately.

    -   Work Items
    -   Commits
    -   Pull Requests
    -   Test Summaries
    -   Artifact Versions
    -   Software Quality Summaries
    -   Security Scan Summaries
8.  Click **Submit**.

    The Change Request form displays.

9.  Select the **Assignment group** to which this change request is assigned.

10. Configure the change window for the change request from the Schedule tab.

    **Note:** For more information on configuring the schedule, see [Create a Change](../../change-management/task/t_CreateAChange.md).

11. Click **Submit**.


## What to do next

To modify the associated DevOps data to the change request, click the **Edit DevOps Data** button. Verify the associated data that you added or removed in the **Additions**/**Removal** tabs in the **Add DevOps Data** modal.

**Parent Topic:**[Accelerating your DevOps change process](../concept/dev-ops-change-acceleration.md)

