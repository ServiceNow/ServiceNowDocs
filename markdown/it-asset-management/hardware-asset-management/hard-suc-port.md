---
title: Success portal view in Hardware Asset Workspace
description: Use the Success portal view in Hardware Asset Workspace to track the progress of your Hardware Asset Management \(HAM\) application with success goals, assign activities to track the success of your goals, and mature your HAM program with predefined maturity items.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Success portal view in Hardware Asset Workspace

Use the Success portal view in Hardware Asset Workspace to track the progress of your Hardware Asset Management \(HAM\) application with success goals, assign activities to track the success of your goals, and mature your HAM program with predefined maturity items.

Success portal helps you perform the following actions:

-   **Track the progress of your HAM application through success goals**

    Success goals help you analyze the value that you get out of your hardware assets and calculate your projected savings. Create success goals for the assets that you want to track. For more information about creating a success goal, see [Create a success goal for Hardware Asset Management](../task/create-suc-goal.md).

-   **Track the progress of your success goals**

    Track the success of your goals by creating success activities for the goals. For more information, see [Create success activities for HAM success goals](../task/create-suc-act-hw.md).

-   **Mature your HAM program with predefined maturity items**

    The program maturity is categorized into Crawl, Walk, and Run stages to help you improve the value return of your HAM application within your organization. You can link these maturity items to success goals and use the HAM application efficiently. For more information, see [View all maturity items for Hardware Asset Management](../task/view-ham-maturity-items.md).

    **Important:** The HAM maturity program is available with the Hardware Asset Management 10.0.0 version or later.


Email notifications are sent when the following conditions are met:

-   To a group, when a success goal is assigned to that group.
-   To an owner, when a success goal is assigned to that owner.
-   To an owner, when a success goal is marked as Pending Review.
-   To an assigned user or an assignment group, when a success activity is assigned.

Access the Success portal by navigating to **Hardware Asset Workspace** &gt; **Success portal**.

The Success portal supports domain separation when the Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\) is activated. To filter the data by domain, select a domain at the top of the dashboard.

![Hardware asset success portal view in Hardware Asset Workspace.](../image/hw-asset-suc-port.png)

To narrow down your results, you can filter by time period.

<table id="table_whp_cqv_1tb"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HAM maturity

</td><td>

Current stage of your HAM program maturity such as the Crawl, Walk, or Run stage.View the maturity items of each stage by selecting **View all maturity items**. For more information, see [View all maturity items for Hardware Asset Management](../task/view-ham-maturity-items.md).

</td></tr><tr><td>

Completed success goals

</td><td>

Total number of completed success goals.

</td></tr><tr><td>

Total success savings

</td><td>

Actual savings from the completed success goals.

</td></tr><tr><td>

Projected savings

</td><td>

Anticipated savings from the success goals are grouped by the status and category of the goal.

</td></tr><tr><td>

All goals

</td><td>

Complete list of success goals with one of the following statuses:-   Draft
-   In Progress
-   Pending Review

</td></tr><tr><td>

Projected vs actual count by category

</td><td>

Comparison between the projected and actual success goals count with status as **Draft**, **In Progress**, or **Pending Review**.

</td></tr><tr><td>

Open activities

</td><td>

Open success goal activities.

</td></tr></tbody>
</table>**Important:** The **HAM maturity**, **Total success savings**, **Projected savings**, and **All goals** fields are available with the Hardware Asset Management 10.0.0 version or later.

