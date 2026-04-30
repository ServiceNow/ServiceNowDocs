---
title: SAFe Prior Sprint Dashboard
description: The SAFe Prior Sprint Dashboard provides data visualization on scope, actual burnup and burndown, and forecast trends of previous sprints. Analyze the data and plan the work for upcoming sprints.
locale: en-US
release: yokohama
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe Prior Sprint Dashboard

The SAFe Prior Sprint Dashboard provides data visualization on scope, actual burnup and burndown, and forecast trends of previous sprints. Analyze the data and plan the work for upcoming sprints.

![SAFe prior sprint dashboard widgets.](../image/safe-prior-sprint-widgets.png "SAFe prior sprint dashboard widgets")

![Agile 2.0 prior sprint dashboard burndown report.](../image/safe-prior-sprint-burndown.png "SAFe prior sprint dashboard burndown report")

![Agile 2.0 prior sprint dashboard burnup report.](../image/safe-prior-sprint-burnup.png "SAFe prior sprint dashboard burnup report")

**Note:** Canceled stories are not included in any of this data.

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

SAFe scrum master: Analyze data on scope, actual burnup and burndown, and forecast trends of previous sprints.

</td><td>

SAFe\_scrum\_user

</td><td>

-   Analyze sprint burndown and burnup trends
-   Use the data to plan for upcoming sprints

</td></tr></tbody>
</table>## Indicators

-   **SAFe: Sum of story points of all stories in the current sprint**

    Generates the scope series in the SAFe Sprint Burndown report.

-   **SAFe: Sum of story points of active stories in the current sprint**

    Generates the actual burndown series in the SAFe Sprint Burndown report.


## Breakdowns

-   SAFe: Sprint
-   SAFe: Prior Sprint

## Widgets

-   **Committed points**

    Indicates the committed scope \(in number of story points\) of the sprint.

-   **Stories**

    Indicates the total number of stories that were completed in the previous sprint.

-   **Completed**

    Indicates the amount of work \(in story points\) that was completed in the previous sprint.

-   **Stories Missing Estimates**

    Indicates the total number of stories in the previous sprint that were missing estimates.


## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Essential SAFe, then install this dashboard from Solution Library to upgrade its layout and access the Sprint Burnup report. For more information, see [Using Solution Library for Essential SAFe dashboards](../reference/using-solution-library-for-essential-safe-dashboards.md).

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

Shows the scope and rate of scope change, the ideal rate for work completion, and the actual rate of work completion. Analyze the burndown trends and accordingly plan the workload for an upcoming sprint.

 The Sprint Burndown report comprises the following series that can be hidden or displayed based on your preference:

-   **Scope**: Indicates the amount of work that is planned for the sprint.
-   **Ideal Burndown**: Indicates how the team needs to progress on stories to complete the sprint on time.
-   **Remaining**: Indicates the amount of work left for completion in the sprint.

If Remaining is above the Ideal Burndown, it implies that there is more work left than originally estimated. The team is running behind the schedule of the sprint.

If the Remaining is below Ideal Burndown, it implies that there is less work left than originally estimated. The team is running ahead of the schedule of the sprint.


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
</table>You can customize the Burnup and Burndown reports. For more information, see [Customizing Essential SAFe dashboard reports](../concept/customizing-safe-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](pa-content-pack-essential-safe.md)

