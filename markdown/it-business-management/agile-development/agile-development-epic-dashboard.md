---
title: Agile 2.0 Epic Dashboard
description: Visually analyze the progress of the stories of an epic over a given period using the Epic Dashboard.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Performance Analytics Content Pack for Agile 2.0, Agile Development 2.0, Strategic Portfolio Management]
---

# Agile 2.0 Epic Dashboard

Visually analyze the progress of the stories of an epic over a given period using the Epic Dashboard.

Navigate to **All** &gt; **Agile Development** &gt; **Dashboards** and select **Agile 2.0 Epic Dashboard**.

![Epic Summary](../image/agile-epic-summary.png "Epic Summary tab")

![Epic cycle time report](../image/agile-epic-cycle-time.png "Cycle Time tab")

The Agile 2.0 Epic Dashboard provides the following information:

-   Displays the number of stories that are complete, and number of stories that are missing estimates for an epic.
-   Displays the number of stories of the epic in their current state and their progress.
-   Indicates the scope changes, if any, and trends of those scope changes.
-   Indicates the pace at which the team is working on stories in the epic.
-   Forecasts when the epic is likely to be completed based on scope change and completion rate trends.
-   Shows time elapsed for the stories of an epic to go from an in-progress state to a completed state.

Canceled stories are not included in any of this data.

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Scrum master: Needs clear visibility into real-time progress of team stories and the changes in scope for the epic to complete the epic on time.

</td><td>

scrum\_user

</td><td>

-   View current states and time in each state for the stories of the epic
-   View epic burnup trend
-   Estimate epic completion dates
-   Identify outlier stories that took longer than expected

</td></tr></tbody>
</table>## Indicators

-   **Scrum: Sum of story points of all stories in epics**

    Generates the scope series in the Epic Burnup report, which indicates the size of the epic.

-   **Scrum: Sum of story points of completed stories in epics**

    Generates the completed series in the Epic Burnup report, which indicates the amount of work that has been completed in the epic.

-   **Scrum: Count of all stories in the current epic**

    Generates the area series the Epic Cumulative Flow Diagram report, which indicates the number of stories of the current epic by state.


## Breakdowns

-   Scrum: Epic
-   Scrum: State

## Widgets

-   **Total Story Count**

    Indicates the total number of stories in the epic.

-   **Stories Completed**

    Indicates the number of stories in the epic that are complete.

-   **Missing Estimates**

    Indicates the number of stories in the epic that are missing estimates.


## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Agile 2.0, then install this dashboard from Solution Library to upgrade its layout and access the following data visualizations:

-   Epic Cumulative Flow Diagram
-   Story Cycle Time

For more information, see [Upgrading the layout of Agile 2.0 dashboards](../reference/using-solution-library-for-agile-2.0-dashboards.md).

<table id="table_fcx_vdk_k3b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Epic Burnup

</td><td>

Line chart![Line chart](../../performance-analytics/image/line-icon.png)

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

Area chart![Area chart](../image/icon-area-report.png)

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
</table><table id="table_gdq_np1_ddc"><thead><tr><th>

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

Identify the time taken for each story in the epic to move from an in-progress state to completion.Each bubble on the graph represents a story. The height of the bubble from the x-axis shows how long that story took to move from an in-progress state to completion. The size of the story bubbles are relative to each other based on their story points.

 Hovering your mouse cursor over a bubble displays the following details about that story:

-   Story points
-   Date that the story is moved to completion
-   Total cycle time \(in days\) of the story
-   Number of days that the story was in the **Work in progress** state
-   Number of days that the story was in the **Ready for testing** state
-   Number of days that the story was in the **Testing** state

From the Story State section towards the right of the report, you can filter the report to view the cycle time of the stories for the selected states. The chart displays the cycle time for each story as the cumulative sum of all duration of the selected states.

 If there are too many stories at any area of the chart and the bubbles appear crowded on the report, you can zoom in that particular area of the report for a clearer view.

![Cycle Time Zoom](../image/cycle-time-zoom.gif)

</td></tr></tbody>
</table>You can customize the Burnup and Cumulative Flow Diagram reports. For more information, see [Customizing Agile 2.0 dashboard reports](../concept/customizing-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Agile 2.0](pa-content-pack-for-agile-2.0.md)

