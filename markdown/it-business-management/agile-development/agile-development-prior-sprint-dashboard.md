---
title: Agile 2.0 Prior Sprint Dashboard
description: Prior Sprint Dashboard provides data visualization on scope, actual burndown and burnup, and forecast trends of previous sprints. Analyze the data and plan the work for upcoming sprints.
locale: en-US
release: yokohama
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Performance Analytics Content Pack for Agile 2.0, Agile Development 2.0, Strategic Portfolio Management]
---

# Agile 2.0 Prior Sprint Dashboard

Prior Sprint Dashboard provides data visualization on scope, actual burndown and burnup, and forecast trends of previous sprints. Analyze the data and plan the work for upcoming sprints.

Navigate to **All** &gt; **Agile Development** &gt; **Dashboards** and select **Agile 2.0 Prior Sprint Dashboard**.

![Agile 2.0 prior sprint dashboard widgets.](../image/agile-prior-sprint-widgets.png "Agile 2.0 prior sprint dashboard widgets")

![Agile 2.0 prior sprint dashboard burndown report.](../image/agile-prior-sp-burndown.png "Agile 2.0 prior sprint dashboard burndown visualization")

![Agile 2.0 prior sprint dashboard burnup report.](../image/agile-prior-sprint-burnup.png "Agile 2.0 prior sprint dashboard burnup visualization")

**Note:** Canceled stories are not included in any of this data.

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Scrum master and sprint planner: Need visibility into actual changes in scope and forecast trends of the previous sprints.

</td><td>

scrum\_user

</td><td>

-   Analyze sprint burndown and burnup trends
-   Use the data to plan for upcoming sprints

</td></tr></tbody>
</table>## Indicators

The following are the indicators which are used to generate the data for the reports of this dashboard.

-   **Scrum: Sum of story points of all stories in the current sprint**

    Generates the scope series in the Sprint Burndown and Sprint Burnup reports.

-   **Scrum: Sum of story points of active stories in the current sprint**

    Generates the completed series in the Sprint Burndown and Sprint Burnup reports.


## Breakdowns

The following are the breakdowns used by the indicators.

-   Scrum: Sprint
-   Scrum: Prior Sprint

## Widgets

-   **Committed points**

    Indicates the committed scope \(in number of story points\) of the sprint.

-   **Stories Completed**

    Indicates the total number of stories that were completed in the previous sprint.

-   **Completed**

    Indicates the amount of work \(in story points\) that was completed in the previous sprint.

-   **Missing Estimates**

    Indicates the total number of stories in the previous sprint that were missing estimates.


## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Agile 2.0, then install this dashboard from Solution Library to upgrade its layout and access the Sprint Burnup visualization. For more information, see [Upgrading the layout of Agile 2.0 dashboards](../reference/using-solution-library-for-agile-2.0-dashboards.md).

<table id="table_mbk_ndk_k3b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sprint Burndown

</td><td>

Line chart![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Indicates the scope changes, if any, and trends of those scope changes. Indicates the ideal pace of work, how much work is remaining, and if the scope is likely to be completed before the end of the sprint.

 The Sprint Burndown report comprises the following series that can be hidden or displayed based on your preference:

-   **Scope**: Indicates the amount of work that is planned for the sprint.
-   **Ideal Burndown**: Indicates how the team needs to progress on stories to complete the sprint on time.
-   **Remaining**: Indicates the amount of work left for completion in the sprint.

If Remaining is above the Ideal Burndown, it implies that there is more work left than originally estimated. The team is running behind the schedule of the sprint.

If Remaining is below Ideal Burndown, it implies that there is less work left than originally estimated. The team is running ahead of the schedule of the sprint.


 Analyze the burndown trends and accordingly plan the workload for an upcoming sprint.

</td></tr><tr><td>

Sprint Burnup

</td><td>

Line chart![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Shows the previous sprint burnup trend indicating scope changes. Analyze future changes the trend of team's work completion.

 The Sprint Burnup report comprises the following series that can be hidden or displayed based on your preference:

-   **Scope**: Indicates the amount of work that is planned for the sprint.
-   **Completed**: Indicates the amount of work completed in the sprint.

</td></tr></tbody>
</table>You can customize the Burnup and Burndown reports. For more information, see [Customizing Agile 2.0 dashboard reports](../concept/customizing-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Agile 2.0](pa-content-pack-for-agile-2.0.md)

