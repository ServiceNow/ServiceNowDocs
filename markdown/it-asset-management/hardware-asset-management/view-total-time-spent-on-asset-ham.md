---
title: View the total time worked on all tasks related to a hardware asset
description: Use the Asset task time summary report to see the details of the time spent on all tasks for an asset and its child assets, grouped by task category.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage and monitor hardware asset performance, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# View the total time worked on all tasks related to a hardware asset

Use the Asset task time summary report to see the details of the time spent on all tasks for an asset and its child assets, grouped by task category.

## Before you begin

Role required: asset

## About this task

Asset task time refers to the total time spent on all tasks related to an asset. The total time spent includes the sum of time worked on all related tasks for the asset and its child assets.

**Note:**

Time spent on tasks related to child assets is rolled up to the parent asset only if the tasks were created and closed after the **last\_used** date on the child assets. The total time from these tasks is then aggregated and added to the parent asset's time spent.

When a child asset is removed from a parent asset, the total time spent on the parent asset remains the same. Therefore, the time spent lines associated with the parent asset will be available even after the child asset is removed.

The time worked on a task is tracked after you start working on it and select **Start Timer** until you close the task. The timer automatically stops when you close the task, and the total duration is updated. You can also pause the timer when you aren't working on the task by selecting **Pause**, and then select **Resume** when you continue to work on the task. You can also add time worked details to the task manually by selecting **Record Time**. The time worked on a task is stored in the Time worked \[task\_time\_worked\] table.

After a task is closed on a parent or child asset, a time spent line is generated and stored in the Time spent line table \[sn\_itam\_common\_time\_spent\_line\]. Each time spent line includes the time worked on the asset task. The sum of the time spent values in these time spent lines gives the total asset task time. If a task involves multiple assets, the total time spent is equally divided among them. This equally distributed time is then aggregated to the parent asset if there are any child assets involved.

**Note:** When you upgrade to Hardware Asset Management version 13.0.0, the **Calculate asset time spent** fix script creates time spent lines for asset tasks that have already been completed and closed.

The total time spent is grouped by the following task categories:

-   **Purchase - Asset**: Includes the following tasks
    -   All tasks in the Refresh flow except the Reclaim aged asset task.
    -   All tasks in the Zero touch refresh flow
    -   Replacement task in the Return Merchandise Authorization \(RMA\) flow
    -   Replacement task in the Recall flow
-   **Labor - Maintenance**
-   **Labor - Repair**: Includes tasks in the following workflows:
    -   Repair order
    -   RMA order
    -   Incident
-   **Labor - General**: Includes tasks in the following workflows:
    -   Asset reclamation
    -   Asset donation
    -   Resale
    -   Disposal
    -   Lease return
    -   Transfer order
    -   Loaner
    -   Asset onboarding
    -   Asset refresh flow \(only the Reclaim aged asset task\)
    -   Asset request \(Pick task\)
    -   Drop off and Receive task
    -   Change

**Note:** Total time spent on an asset task isn't calculated for pallets, consumables, and bundle assets. Therefore, the Asset task time summary report isn't available for these assets.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset estate**.

2.  Select the **All assets** tab.

3.  Select the asset record for which you want to view the details of the total time spent on the tasks.

4.  On the contextual sidebar, select the Asset task time summary icon ![](../../enterprise-asset-management/image/asset-task-summary-icon.png).

    **Total time spent by task category** report is displayed.

    ![Asset task time summary](../image/asset-task-summary-ham.png)

    The Asset task time summary report includes the following details:

    -   **Total time spent**: Total time worked on all related tasks for the asset, including tasks on child assets.
    -   Breakdown of total time spent: Total time worked on all related tasks, divided and shown separately for each task category. This visualization helps you to see how much time was spent on tasks within each task category.
    -   Legends for the task categories: Legends shown are based on the actual asset tasks and their task categories. The legends include the following:
        -   **Purchase - Asset**
        -   **Labor - Maintenance**
        -   **Labor - Repair**
        -   **Labor - General**
5.  To view the details of the time spent on all tasks within a specific task category, select the corresponding task category section in the report.

    The list of time spent lines is displayed, with each line showing the following details:

    -   **Source asset**: Display name of the asset, including both parent and child assets, for which time was spent on the task.
    -   **Task**: Task number
    -   **Task type**: Type of the task, such as the Hardware RMA Order Line task.
    -   **Task name**: Name of the task, such as Prepare or On-site repair.
    -   **Time spent**: Time worked on the asset task.
    -   **Short description**: A brief description of the task.
    -   **Closed**: The date and time when the asset task was closed.
    -   **Task category**: Category to which the task belongs.

