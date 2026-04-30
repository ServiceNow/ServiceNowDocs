---
title: Create a DevOps Change request and associate existing DevOps data — Workspace
description: Create a DevOps change request and associate existing DevOps data through the Workspace UI.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Accelerate your DevOps change process, DevOps Change Velocity, IT Service Management]
---

# Create a DevOps Change request and associate existing DevOps data — Workspace

Create a DevOps change request and associate existing DevOps data through the Workspace UI.

## Before you begin

Role required: sn\_devops.admin

## About this task

For more information on using Change features, see [Create a Change](../../change-management/task/t_CreateAChange.md).

**Important:** You can update the associated data after you create a request, but you cannot edit a change request if it is in one of the following states:

-   Implement
-   Post-Implement
-   Cancelled

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change** &gt; **Applications \(![Applications icon.](../image/icon-devops-applications.png)\)**.

2.  Select an application from **Applications** list.

3.  In the Recommended actions panel, select **Create manual change**.

4.  In the **Category** list, select DevOps and then select **Save**.

5.  Select **Add DevOps data** to add supporting data to the change request.

6.  Complete the Add DevOps data pages.

    1.  Specify the following values on the **Select data type and associations** page:

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data type

</td><td>

The type of data to associate with the change request.

 -   Artifact version
-   Release version
-   Build number


</td></tr><tr><td>

Data associations

</td><td>

The specific data to associate with the change request. You can select multiple artifact versions and build numbers.

 If you select Build number as the **Data type**, then you must also specify the application name and corresponding pipelines and build numbers.

</td></tr></tbody>
</table>    2.  Select **Next** to open the Verify data associations page.

    3.  Navigate the tabs to verify that the associated data is mapped accurately.

        Update settings as needed.

        -   Work Items
        -   Commits
        -   Pull Requests
        -   Test Summaries
        -   Artifact Versions
        -   Software Quality Summaries
        -   Security Scan Summaries
    4.  Select **Submit**.

    The Change request form is updated.

7.  Configure other settings as needed.

    For example, specify the schedule.

    **Note:** For more information on configuring settings, see [Create a Change](../../change-management/task/t_CreateAChange.md).

8.  Select **Save**.


## What to do next

To modify the data that is associated to the change request, select **Edit DevOps data**. Verify the associated data that you added or removed in the **Additions**/**Removal** tabs in the **Add DevOps Data** modal.

**Parent Topic:**[Accelerating your DevOps change process](../concept/dev-ops-change-acceleration.md)

