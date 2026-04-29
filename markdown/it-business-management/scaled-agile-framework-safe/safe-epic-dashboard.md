---
title: SAFe Epic Dashboard
description: The SAFe Epic Dashboard provides a visualization of how the features of an epic are progressing over a given period of time.
locale: en-US
release: australia
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe Epic Dashboard

The SAFe Epic Dashboard provides a visualization of how the features of an epic are progressing over a given period of time.

![SAFe Epic Summary tab](../image/safe-epic-summary-dashboard.png "Epic Summary tab")

![epic cycle time](../image/safe-epic-cycle-time.png "Cycle Time tab")

The SAFe epic dashboard displays such as total number of features that are complete, and number of stories that are missing estimates. It also indicates the pace at which the ART members are completing the features in the epic.

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

SAFe ART user: View the progress of every feature in the epic.

</td><td>

safe\_scrum\_user

</td></tr></tbody>
</table>## Indicators

-   **SAFe: Sum of story points of all stories in epics**

    Generates the scope series in the Epic Burnup report.

-   **SAFe: Sum of story points of completed stories in epics**

    Generates the complete series in the Epic Burnup report. This series indicates the amount of work that has been completed in the epic.

-   **SAFe: Count of all stories in current epic**

    Generates the area series the Epic Cumulative Flow Diagram report, which indicates the number of stories of the current epic by state.


## Breakdowns

-   SAFe: Epic
-   SAFe: State

## Widgets

-   **Features**

    Indicates the total number of features in the epic.

-   **Features Released**

    Indicates the number of features in the epic that have been completed.

-   **Stories Missing Estimates**

    Indicates the number of stories in the epic that are missing estimates.


## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Essential SAFe, then install this dashboard from Solution Library to upgrade its layout and access the following visualizations:

-   Epic Burnup
-   Epic Cumulative Flow Diagram
-   Story Cycle Time

For more information, see [Using Solution Library for Essential SAFe dashboards](../reference/using-solution-library-for-essential-safe-dashboards.md).

<table id="table_fcx_vdk_k3b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Feature Progress

</td><td>

Horizontal bar chart

 ![](../../reporting/image/inline-data-vis-96px-bar-horizontal.png)

</td><td>

View the progress of every feature in an epic.

</td></tr><tr><td>

Epic Burnup

</td><td>

Line chart![](../../reporting/image/inline-data-vis-96px-line.png)

</td><td>

Shows the epic burnup trends. You can estimate when the epic is likely to be completed.

 The Epic Burnup report comprises the following series that can be hidden or displayed based on your preference:

-   **Scope**: Indicates the size of the epic.
-   **Scope Forecast**: Predicts the possibility of scope change for the future dates, which is based on historical data.
-   **Completed**: Indicates the amount of work in the epic that is complete.
-   **Completed Forecast**: Predicts the burnup for the future dates. It indicates whether you can complete the epic on time. This prediction is based on historical data.

**Note:** The point at which the Completed Forecast series intersects with or crosses the Scope Forecast series is a predictor for when the epic might be completed. If the Completed Forecast series and the Scope Forecast series do not appear to ever intersect, it is a warning that scope is being added faster than work is being completed.

</td></tr><tr><td>

Epic Cumulative Flow Diagram

</td><td>

Area chart![](../../reporting/image/inline-data-vis-96px-area.png)

</td><td>

Monitor the progress of all the stories of your epic between its actual start and end dates.

 View the number of stories in each state by their arrival to a state, time in this state, and its departure from this state.

 The Epic Cumulative Flow Diagram report comprises the following areas that can be hidden or displayed based on your preference:

-   **Ready**: Indicates the number of stories of the epic that are ready to start work on.
-   **Work in Progress**: Indicates the number of stories of the epic that are in development.
-   **Ready for Testing**: Indicates the number stories of the epic that are ready to be tested.
-   **Testing**: Indicates the number of stories of the epic that are currently being tested.
-   **Complete**: Indicates the number of stories that are complete.

 **Note:** Stories in Ready and Cancelled states are not included in this report.

</td></tr></tbody>
</table><table id="table_vwn_bs1_ddc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Story Cycle Time

</td><td>

Bubble chart![](../../reporting/image/inline-data-vis-96px-bubble.png)

</td><td>

Identify the time taken for each story in the epic to move from an in-progress state to completion.Each bubble on the graph represents a story. The height of the bubble from the x-axis shows how long that story took to move from an in-progress state to completion. The size of the story bubbles are relative to each other based on their story points.

Hovering your mouse cursor over a bubble displays the following details about that story:

-   Story points
-   Date on which the story is moved to completion
-   Total cycle time \(in days\) of the story
-   Number of days that the story was in the **Work in progress** state
-   Number of days that the story was in the **Ready for testing** state
-   Number of days that the story was in the **Testing** state

 From the Story State section towards the right of the report, you can filter the report to view the cycle time of the stories for the selected states. The chart displays the cycle time for each story as the cumulative sum of all duration of the selected states.

If there are too many stories at any area of the chart and the bubbles appear crowded on the report, you can zoom in that particular area of the report for clearer view.

 ![Cycle Time Zoom](../image/cycle-time-zoom.gif)

</td></tr></tbody>
</table>You can customize the Burnup and Cumulative Flow Diagram reports. For more information, see [Customizing Essential SAFe dashboard reports](../concept/customizing-safe-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](pa-content-pack-essential-safe.md)

