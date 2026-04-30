---
title: SAFe PI Dashboard
description: The SAFe PI Dashboard allows you to track the progress of your features in the current program increment \(PI\).
locale: en-US
release: xanadu
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe PI Dashboard

The SAFe PI Dashboard allows you to track the progress of your features in the current program increment \(PI\).

![SAFe PI Summary tab](../image/safe-PI-summary.png "PI Summary tab")

![SAFe PI Cycle time](../image/safe-PI-cycle-time.png "Cycle Time tab")

The SAFe PI dashboard provides the following details:

-   Displays important details of the PI such as percentage of work that is complete, time elapsed, and total number of stories that are missing estimates.
-   Displays the number of stories of the PI in their current state and their progress.
-   Indicates the scope changes, if any, and trends of those scope changes.
-   Indicates the pace at which the ART members are completing features that are planned for the PI.
-   Forecasts data showing the likelihood of completing the PI as planned.
-   Shows time elapsed for the stories of the PI to go from an in-progress state to a completed state.

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|SAFe ART user: Track the progress of your stories that are planned for the PI. Resolve any bottlenecks and target to complete the PI on time.|safe\_scrum\_user|

## Indicators

-   **SAFe: Count of all stories in the current PI**

    Generates the area series the PI Cumulative Flow Diagram report, which indicates the number of stories of the current PI by state.

-   **SAFe: Sum of story points of all stories in the current PI**

    Generate the scope series in the PI Burndown report. This series indicates the amount \(in story points\) of work planned for the PI.

-   **SAFe: Sum of story points of completed stories in the current PI**

    Generates the actual burndown series in the PI Burndown report, and the completed series in the PI Burnup report. These series indicate the amount of work \(in story points\) that has been completed for the PI.

-   **SAFe: Sum of story points of active stories in the current PI**

    Generates the scope series in the PI Burndown and PI Burnup reports. The scope series indicates the amount of work \(in story points\) that is planned for the PI.

-   **SAFe: Time elapsed in the PI**

    Calculates the time to be displayed in the Time Elapsed widget.


## Breakdowns

-   SAFe: PI
-   SAFe: State

## Widgets

-   **Scope**

    Indicates the amount of work in story points that is planned for the PI. This widget lets you see at a glance how much work must be completed to achieve the PI goal. It also lets you drill down to detail on the stories that are planned for completion in the PI.

-   **Percent Completed**

    Indicates the percentage of work that has been completed in the PI using story points. This widget lets you see at a glance how much work has been completed in the PI. Together with the adjacent Time Elapsed widget, these widgets let you easily see whether you are completing work at a rate consistent with achieving the PI goal on schedule.

-   **Time Elapsed**

    Indicates the percentage of time that has elapsed between the start date and planned end date of the PI. Together with the adjacent Percent Completed widget, these widgets let you easily see whether you are completing work at a rate consistent with achieving the PI goal on schedule.

-   **Features**

    Indicates the total number of features that are planned for completion in the PI.

-   **Features Released**

    Indicates the total number of features in the PI that have been completed.

-   **Stories Missing Estimates**

    Indicates the total number of stories in the PI that are missing estimates. It is required that you use estimates for the other indicators, widgets, and reports on this dashboard to be meaningful.

    **Note:** If you do not estimate stories, enter a "1" in the **Story Points** field. The other indicators, widgets, and reports will then effectively function by count.

-   **Blocked Work**

    Indicates the amount of work \(in story points\) in the PI that is blocked.


## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Essential SAFe, then install this dashboard from Solution Library to upgrade its layout and access the following visualizations:

-   PI Cumulative Flow Diagram
-   Story Cycle Time

For more information, see [Using Solution Library for Essential SAFe dashboards](../reference/using-solution-library-for-essential-safe-dashboards.md).

<table id="table_enf_b2k_k3b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PI Burndown

</td><td>

Line chart![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Indicates the scope changes, if any, and trends of those scope changes. Indicates the ideal pace of work, how much work is remaining, and if the scope is likely to be completed before the end of the PI. The PI Burndown report comprises the following series that can be hidden or displayed based on your preference:-   **Scope**: Indicates the amount of work that is planned for the PI.
-   **Scope Forecast**: Predicts the possibility of scope change for the future dates in the PI. This prediction is based on historical data.
-   **Ideal Burndown**: Indicates how the ART members need to progress on stories to deliver the PI on time.
-   **Remaining**: Indicates the amount of work completed in the PI.
-   **Remaining Forecast**: Predicts the burndown for the future dates in the release. It indicates whether you can deliver the PI on time.

</td></tr><tr><td>

PI burnup

</td><td>

Line chart![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Analyse the burnup trends, and estimate when the PI work is likely to be completed. The PI burnup report comprises the following series that can be hidden or displayed based on your preference:-   **Scope**: Indicates the amount of work that is planned for the PI.
-   **Scope Forecast**: Predicts the possibility of scope change for the future dates. This prediction is based on historical data.
-   **Completed**: Indicates the amount of work in the PI that is complete.
-   **Completed Forecast**: Predicts the burnup for the future dates in the PI. It indicates whether you can complete the PI on time.

 **Note:** The point at which the Completed Forecast series intersects with or crosses the Scope Forecast series is a predictor for when the PI might be completed. If the Completed Forecast series and the Scope Forecast series do not appear to ever intersect, it is a warning that scope is being added faster than work is being completed.

</td></tr><tr><td>

PI Feature Progress

</td><td>

Horizontal bar chart![Horizontal bar chart](../../performance-analytics/image/horizontal-bar.png)

</td><td>

Analyse the progress of every feature of the PI, by viewing the count of the stories segregated by their state.

</td></tr><tr><td>

Velocity by Sprint

</td><td>

Bar chart![Bar chart](../../performance-analytics/image/column-icon.png)

</td><td>

View the velocity of the ART members across PIs. Understand if the ART members are achieving a stable, predictable velocity over sprints, and meeting the commitments.

</td></tr><tr><td>

PI Cumulative Flow Diagram

</td><td>

Area chart![Area chart](../image/icon-area-report.png)

</td><td>

Monitor the progress of all the stories of your PI between its actual start and end dates.

 View the number of stories in each state by their arrival to a state, time in this state, and its departure from this state.

 The PI Cumulative Flow Diagram report comprises the following areas that can be hidden or displayed based on your preference:

-   **Ready**: Indicates the number of stories of the PI that are ready to start work on.
-   **Work in Progress**: Indicates the number of stories of the PI that are in development.
-   **Ready for Testing**: Indicates the number stories of the PI that are ready to be tested.
-   **Testing**: Indicates the number of stories of the PI that are currently being tested.
-   **Complete**: Indicates the number of stories that are complete.

 **Note:** Stories in Ready and Cancelled states are not included in this report.

</td></tr></tbody>
</table><table id="table_tcb_2v1_ddc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Story Cycle Time

</td><td>

Bubble chart![Bubble chart](../../performance-analytics/image/bubble-icon.png)

</td><td>

Identify the time taken for each story in the PI to move from an in-progress state to completion.Each bubble on the graph represents a story. The height of the bubble from the x-axis shows how long that story took to move from an in-progress state to completion. The size of the story bubbles are relative to each other based on their story points.

 Hovering your mouse cursor over a bubble displays the following details about that story:

-   Story points
-   Date on which the story is moved to completion
-   Total cycle time \(in days\) of the story
-   Number of days that the story was in the **Work in progress** state
-   Number of days that the story was in the **Ready for testing** state
-   Number of days that the story was in the **Testing** state

 From the Story State section towards the right of the report, you can filter the report to view the cycle time of the stories for the selected states. The chart displays the cycle time for each story as the cumulative sum of all duration of the selected states.

 If there are too many stories at any area of the chart and the bubbles appear crowded on the report, you can zoom in that particular area of the report for a clearer view.

 ![Cycle Time Zoom](../image/cycle-time-zoom.gif)

</td></tr></tbody>
</table>You can customize the Burnup, Burndown, and Cumulative Flow Diagram reports. For more information, see [Customizing Essential SAFe dashboard reports](../concept/customizing-safe-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](pa-content-pack-essential-safe.md)

