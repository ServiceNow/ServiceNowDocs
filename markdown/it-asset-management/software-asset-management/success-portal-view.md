---
title: Success portal view in Software Asset Workspace
description: Use the Success portal view in Software Asset Workspace to track the progress of your Software Asset Management \(SAM\) application with success goals, assign activities to track the success of your goals, run health checks on your software, maximize the usage of your SAM capabilities, and mature your SAM program with predefined maturity items.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Success portal view in Software Asset Workspace

Use the Success portal view in Software Asset Workspace to track the progress of your Software Asset Management \(SAM\) application with success goals, assign activities to track the success of your goals, run health checks on your software, maximize the usage of your SAM capabilities, and mature your SAM program with predefined maturity items.

Success portal helps you perform the following actions:

-   **Track the progress of your SAM application through success goals**

    Success goals help you analyze the value that you get out of your software licenses and calculate your projected savings. Create success goals for the licenses that you want to track. For more information about creating a success goal, see [Create success goals for Software Asset Management](../task/create-success-goals.md).

-   **Track the progress of your success goals**

    Track the success of your goals by creating success activities for the goals. For more information, see [Create success activities for Software Asset Management](../task/create-success-activity.md).

-   **Perform a health check on your software**

    Run health checks to review the health of licenses, permissions, and configurations to get the best out of each software suite. For more information, see [Health check](health-check-dboard.md).

-   **Keep your software up to date using Value builder tasks**

    Get an overview of which software upgrades, publisher packs, and integrations you must set up with Value builder tasks. These tasks are created automatically, but you can create your own as necessary. For more information, see [Value builder](sam-value-builder.md).

-   **Mature your SAM program with predefined maturity items**

    The program maturity is categorized into Crawl, Walk, and Run stages to help you improve the value return of your SAM program, including processes, features, functionalities, and capabilities within your organization. You can link these maturity items to Success goals and Value builder tasks to track and report on the improvements of your SAM application over time. For more information, see [View all maturity items for Software Asset Management](../task/view-maturity-items.md).


Email notifications are sent when the following conditions are met:

-   To a group, when a success goal is assigned to that group.
-   To an owner, when a success goal is assigned to that owner.
-   To an owner, when a success goal is marked as Pending Review.
-   To an assigned user or an assignment group, when a success activity is assigned.

Access the Success portal view by navigating to **Software Asset Workspace** &gt; **Success portal**.

The Success portal supports domain separation when the Performance Analytics - Domain Support plugin \(com.snc.pa.domain\_support\) is activated. To filter the data by domain, select a domain at the top of the dashboard.

![Success portal view in Software Asset Workspace.](../image/success-portal.png "Success portal view")

<table id="table_whp_cqv_1tb"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SAM maturity

</td><td>

Current stage of your SAM program maturity such as the Crawl, Walk, or Run stage.View the maturity items of each stage by selecting **View all maturity items**. For more information, see [View all maturity items for Software Asset Management](../task/view-maturity-items.md).

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

All success goals grouped by the following statuses:-   Draft
-   In Progress
-   Pending Review
-   Completed
-   Canceled

</td></tr><tr class="sub-head"><td>

Health check and value builder data

</td><td>

 

</td></tr><tr><td>

Health checks passed

</td><td>

Percentage of successful health checks.

</td></tr><tr><td>

Completed value builder tasks

</td><td>

Number of value builder tasks that are completed.

</td></tr><tr><td>

Open activities

</td><td>

Open success goal activities.

</td></tr></tbody>
</table>