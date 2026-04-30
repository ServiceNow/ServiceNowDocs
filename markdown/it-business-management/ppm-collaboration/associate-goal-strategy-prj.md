---
title: Allocate or modify the strategy and goal percentage for a project
description: Allocate the percentage of a project's total cost, benefit, and budget to help achieve the strategic objectives that the project fulfills. You can also view the breakdown of the project's financial data based on the allocated percentage.
locale: en-US
release: yokohama
product: PPM Collaboration
classification: ppm-collaboration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Strategic spend tracking, Project Portfolio Management, Strategic Portfolio Management]
---

# Allocate or modify the strategy and goal percentage for a project

Allocate the percentage of a project's total cost, benefit, and budget to help achieve the strategic objectives that the project fulfills. You can also view the breakdown of the project's financial data based on the allocated percentage.

## Before you begin

You should have an existing [project](../../project-management/task/t_CreateAProject.md).

Execute the following scheduled jobs:

-   **PPM Strategic Spend Tracking - Update projects and demands with strategy and goal allocations**
-   **PPM Strategic Spend Tracking - Generate Strategy/Goal Allocation Breakdowns for Projects and Demands**

Role required: it\_project\_manager

## Procedure

1.  Navigate to **Project** &gt; **Projects** &gt; **All**.

2.  Select the project to which you want to add or update allocation percentages.

3.  In the **Business Case** tab, add or update the strategies and goals with which the project is associated.

    For more information, see the Business Case field descriptions in the [Create a project](../../project-management/task/t_CreateAProject.md) documentation topic.

4.  Click **Save**.

    The selected strategies and goals appear in the Strategy Allocations and Goal Allocations related lists.

5.  Update strategy and goal allocations.

    1.  In the Strategy Allocations related list, click the **% Allocation** field and enter the percentage that this project contributes towards the selected organizational strategy.

    2.  In the Goal Allocations related list, click the **% Allocation** field and enter the percentage that this project contributes towards the selected organizational goal.

        **Note:** The sum of strategy or goal allocations for a project must not exceed 100%.

6.  Click the **Recalculate Strategy and Goal Allocation** related link to update cost field values in the allocation tabs.

7.  Click **Update**.

8.  In the Strategy or Goal Allocations related list, click the preview icon \(![Preview record icon](../image/preview_icon.png)\), and then click **Open Record** to view the breakdown of the strategy or goal allocation.

9.  View the trends for planned costs, actual costs, and benefits over time using the [Strategic Spend Tracking for PPM dashboard](../../../use/dashboards/application-content-packs/ppm-strategic-spend-tracking-dashboard.md).


**Parent Topic:**[Strategic Spend Tracking for PPM](../concept/ppm-strategic-spend-tracking-overview.md)

