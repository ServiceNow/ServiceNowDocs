---
title: SAFe Sprint Dashboard
description: Track the progress of your SAFe stories in the current sprint and forecast sprint completion using the SAFe Sprint Dashboard.
locale: en-US
release: xanadu
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe Sprint Dashboard

Track the progress of your SAFe stories in the current sprint and forecast sprint completion using the SAFe Sprint Dashboard.

![SAFe sprint dashboard widgets.](../image/safe-sprint-dashboard-widgets.png "SAFe sprint dashboard widgets")

![SAFe sprint dashboard burndown report.](../image/safe-sprint-burndown.png "SAFe sprint dashboard burndown report")

![SAFe sprint dashboard burnup report.](../image/safe-sprint-burnup.png "SAFe sprint dashboard burnup report")

![SAFe sprint dashboard cumulative flow diagram report.](../image/safe-sprint-cfd.png "SAFe sprint dashboard cumulative flow diagram")

The dashboard:

-   Displays important details of the sprint such as percentage of work that is complete, time elapsed, and total number of stories that are missing estimates.
-   Displays the number of stories of the sprint in their current state and their progress.
-   Indicates the scope changes, if any, and trends of those scope changes.
-   Indicates how the team needs to progress on stories to achieve the sprint goal.
-   Forecasts data showing the likelihood of completing the sprint as planned.

**Note:** Canceled stories are not included in any of this data.

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

SAFe scrum master: Reviews the sprint burndown trends. Resolves any bottlenecks and targets to complete the sprint on time.

</td><td>

safe\_scrum\_user

</td><td>

-   Analyse the scope changes for the sprint
-   View current states and analyse the time in each state for the stories of the sprint
-   Estimate sprint completion dates

</td></tr></tbody>
</table>## Indicators

-   **SAFe: Sum of story points of all stories in the current sprint**

    Generates the scope series in the Sprint Burndown report. The scope series indicates the amount of work in story points that is planned for the sprint.

-   **SAFe: Sum of story points of active stories in the current sprint**

    Generates the actual burndown series in the Sprint Burndown report. The actual burndown series indicates the amount of work left \(in story points\) for completion.

-   **SAFe: Sum of story points of completed stories in current sprint**

    Generates the percentage of stories completed for the current sprint.

-   **SAFe: Time elapsed in sprint**

    Calculates the time to be displayed in the Time Elapsed widget.

-   **SAFe: Count of stories in the current sprint**

    Generates the area series in the Sprint Cumulative Flow Diagram report. It indicates the number of stories in the current sprint.


## Breakdowns

-   SAFe: Sprint
-   SAFe: Current Sprint
-   SAFe: State

## Widgets

-   **Scope**

    Indicates the amount of work in story points that is planned for the sprint. This widget lets you see at a glance how much work must be completed to achieve the sprint goal. It also lets you drill down to detail on the stories planned into the sprint.

-   **Percent Completed**

    Indicates the percentage of work that has been completed in the sprint using story points. This widget lets you see at a glance how much work has been completed in the sprint. Together with the adjacent Time Elapsed widget, these widgets lets you easily see whether you are completing work at a rate consistent with achieving the sprint goal on schedule.

-   **Time Elapsed**

    Indicates the percentage of time that has elapsed between the start date and planned end date of the sprint. Together with the adjacent Percent Completed widget, these widgets let you easily see whether you are completing work at a rate consistent with achieving the sprint goal on schedule.

-   **Committed Points**

    Indicates the committed scope \(in number of story points\) of the sprint. Together with the adjacent Scope widget, these widgets let you see difference between the scope committed at the start of the sprint and the current scope of the sprint.

    **Note:** This widget is not visible by default. You can add it from Reports to your dashboard. For more information, see [Edit a responsive dashboard](https://www.servicenow.com/docs/access?context=t_EditADashboard&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

-   **Blocked Work**

    Indicates the amount of work \(in story points\) in the sprint that is blocked.

-   **Stories Missing Estimates**

    Indicates the total number of stories in the sprint that are missing estimates. It is required that you use estimates for the other indicators, widgets, and reports on this dashboard to be meaningful.

    **Note:** If you do not estimate stories, enter a "1" in the **Story Points** field. The other indicators, widgets, and reports will then effectively function by count.


## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Essential SAFe, then install this dashboard from Solution Library to upgrade its layout and access the following visualizations:

-   Sprint Burnup
-   Sprint Cumulative Flow Diagram

For more information, see [Using Solution Library for Essential SAFe dashboards](../reference/using-solution-library-for-essential-safe-dashboards.md).

<table id="table_mbk_ndk_k3b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sprint Burndown

</td><td>

Line chart ![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Indicates the scope changes, if any, and trends of those scope changes. Indicates the ideal pace of work, how much work is remaining, and if the scope is likely to be completed before the end of the sprint. The Sprint Burndown report comprises the following series that can be hidden or displayed based on your preference:

-   **Scope**: Indicates the amount of work that is currently planned for the sprint. This can vary if stories are added to or removed from the sprint after it is started.
-   **Scope Forecast**: Predicts the possibility of scope change for the future dates based on historical changes in the current sprint.
-   **Ideal Burndown**: Indicates how the team needs to progress on stories to complete the sprint on time.
-   **Remaining**: Indicates the amount of work left for completion in the sprint.

If the actual burndown \(Remaining\) is above the ideal burndown, it implies that there is more work left than originally estimated. The team is running behind the schedule of the sprint. If the actual burndown \(Remaining\) is below the ideal burndown, it implies that there is less work left than originally estimated. The team is running ahead of the schedule of the sprint.

-   **Remaining Forecast**: Predicts the burndown for the future dates based on historical changes in the current sprint.

</td></tr><tr><td>

Sprint Burnup

</td><td>

Line chart ![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Shows the sprint burnup trend indicating scope changes. Forecasts future changes in scope and the trend of work completion.

 The Sprint Burnup report comprises the following series that can be hidden or displayed based on your preference:

-   **Scope**: Indicates the amount of work that is planned for the sprint.
-   **Scope Forecast**: Predicts the possibility of scope change for the future dates, which is based on historical data.
-   **Completed**: Indicates the amount of work completed in the sprint.
-   **Completed Forecast**: Predicts the burnup for the future dates. It indicates whether you can complete the sprint on time. The prediction is based on historical data.

</td></tr><tr><td>

Sprint Cumulative Flow Diagram

</td><td>

Area chart![Area chart](../image/icon-area-report.png)

</td><td>

Monitor the progress of all the stories of your sprint between its actual start and end dates.

 View the number of stories in each state by their arrival to a state, time in this state, and its departure from this state.

 The Sprint Cumulative Flow Diagram report comprises the following areas that can be hidden or displayed based on your preference:

-   **Ready**: Indicates the number of stories in the sprint that are ready to start work on.
-   **Work in Progress**: Indicates the number of stories in the sprint that are in development.
-   **Ready for Testing**: Indicates the number stories in the sprint that are ready to be tested.
-   **Testing**: Indicates the number of stories in the sprint that are currently being tested.
-   **Complete**: Indicates the number of stories in the sprint that are complete.

 **Note:** Stories in Ready and Cancelled states are not included in this report.

</td></tr></tbody>
</table>You can customize the Burnup, Burndown, and Cumulative Flow Diagram reports. For more information, see [Customizing Essential SAFe dashboard reports](../concept/customizing-safe-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](pa-content-pack-essential-safe.md)

