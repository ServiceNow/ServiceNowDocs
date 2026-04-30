---
title: Agile 2.0 Release Dashboard
description: Track the progress of your stories and analyze scope changes in the current release using Agile 2.0 Release Dashboard.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Performance Analytics Content Pack for Agile 2.0, Agile Development 2.0, Strategic Portfolio Management]
---

# Agile 2.0 Release Dashboard

Track the progress of your stories and analyze scope changes in the current release using Agile 2.0 Release Dashboard.

Navigate to **All** &gt; **Agile Development** &gt; **Dashboards** and select **Agile 2.0 Release Dashboard**.

![Release summary](../image/agile-release-summary.png "Release Summary tab")

![Release cycle time](../image/agile-release-cycle-time.png "Cycle Time tab")

The dashboard:

-   Displays important details of the release such as percentage of work that is complete, time elapsed, and total number of stories that are missing estimates.
-   Displays the number of stories of the release in their current state and their progress.
-   Indicates the scope changes, if any, and trends of those scope changes.
-   Indicates the pace at which the team is completing stories that are planned for the release.
-   Forecasts data showing the likelihood of completing the release as planned.
-   Shows time elapsed for the stories of a release to go from an in-progress state to a completed state.

**Note:** Canceled stories are not included in any of this data.

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Product owner: Needs visibility into scope changes, team's pace, and real-time progress of the stories for the release.

</td><td>

scrum\_user

</td><td>

-   Track progress of your stories that are planned for a release
-   Resolve any bottlenecks to deliver the release on time
-   Identify outlier stories that took longer than expected

</td></tr></tbody>
</table>## Indicators

-   **Scrum: Sum of story points of completed stories in the active releases**

    Generates the Completed series in the Release Burndown and Burnup reports. These series indicate the amount of work in story points that has been completed for the release.

-   **Scrum: Sum of story points of active stories in the current releases**

    Generates the scope series in the Release Burndown and Release Burnup reports. The scope series indicates the amount of work in story points that is planned for the release.

-   **Scrum: Time elapsed in the release**

    Calculates the time to be displayed in the Time Elapsed widget.

-   **Scrum: Count of all stories in the current release**

    Generates the area series in the Release Cumulative Flow Diagram report, which indicates the number of stories of the current release by state.


## Breakdowns

-   Scrum: Release
-   Scrum: State

## Widgets

-   **Percent Completed**

    Indicates the percentage of work \(in story points\) that has been completed in the release. This widget lets you see at a glance how much work has been completed in the release. Together with the adjacent Time Elapsed widget, these widgets let you easily see whether you are completing work at a rate consistent with achieving the release goal on schedule.

-   **Scope**

    Indicates the amount of work in story points that is planned for the release. This widget lets you see at a glance how much work must be completed to achieve the releaser goal. It also lets you drill down to detail on the stories planned into the release.

-   **Time Elapsed**

    Indicates the percentage of time that has elapsed between the start date and planned end date of the release. Together with the adjacent Percent Completed widget, these widgets let you easily see whether you are completing work at a rate consistent with achieving the Release goal on schedule.

-   **Blocked Work**

    Indicates the total number of stories in the release that are missing estimates. It is required that you use estimates for the other indicators, widgets, and reports on this dashboard to be meaningful.

    **Note:** If you do not estimate stories, enter a "1" in the **Story Points** field. The other indicators, widgets, and reports will then effectively function by count.

-   **Blocked Work**

    Indicates the number of stories in the release that are missing estimates.


## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Agile 2.0, then install this dashboard from Solution Library to upgrade its layout and access the following visualizations:

-   Release Cumulative Flow Diagram
-   Story Cycle Time

For more information, see [Upgrading the layout of Agile 2.0 dashboards](../reference/using-solution-library-for-agile-2.0-dashboards.md).

<table id="table_enf_b2k_k3b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Release Burnup

</td><td>

Line

 ![Line graph](../../performance-analytics/image/line-icon.png)

</td><td>

Analyse the burnup trends, and estimate when the release work is likely to be completed. The release burnup report comprises the following series that can be hidden or displayed based on your preference:

 -   **Scope**: Indicates the amount of work that is planned for the release.
-   **Scope Forecast**: Predicts the possibility of scope change for the future dates. This prediction is based on historical data.
-   **Completed**: Indicates the amount of release work that is complete.
-   **Completed Forecast**: Predicts the burnup for the future dates in the release. It indicates whether you can deliver the release on time.

 **Note:** The point at which the Completed Forecast series intersects with or crosses the Scope Forecast series is a predictor for when the release might be completed. If the Completed Forecast series and the Scope Forecast series do not appear to ever intersect, it is a warning that scope is being added faster than work is being completed.

</td></tr><tr><td>

Release Burndown

</td><td>

Line

 ![Line graph](../../performance-analytics/image/line-icon.png)

</td><td>

Indicates the scope changes, if any, and trends of those scope changes. Indicates the ideal pace of work, how much work is remaining, and if the scope likely to be completed before the end of the sprint. The Release Burndown report comprises the following series that can be hidden or displayed based on your preference:

 -   **Scope**: Indicates the amount of work that is planned for the release.
-   **Scope Forecast**: Predicts the possibility of scope change for the future dates in the release. This prediction is based on historical data.
-   **Ideal Burndown**: Indicates how the team needs to progress on stories to deliver the release on time.
-   **Remaining**: Indicates the amount of work that is completed.

If Remaining is above the ideal burndown, it implies that there is more work left than originally estimated. The team is running behind the schedule of the release. If the Remaining is below the ideal burndown, it implies that there is less work left than originally estimated. The team is running ahead of the schedule of the release.

-   **Completed Forecast**: Predicts the burndown for the future dates in the release. It indicates whether you can deliver the release on time.

</td></tr><tr><td>

Release Cumulative Flow Diagram

</td><td>

Area![Area chart](../image/icon-area-report.png)

</td><td>

Monitor the progress of all the stories of your release between its actual start and end dates.

 View the number of stories in each state by their arrival to a state, time in this state, and its departure from this state.

 The Release Cumulative Flow Diagram report comprises the following areas that can be hidden or displayed based on your preference:

-   **Ready**: Indicates the number of stories in the release that are ready to start work on.
-   **Work in Progress**: Indicates the number of stories in the release that are in development.
-   **Ready for Testing**: Indicates the number stories in the release that are ready to be tested.
-   **Testing**: Indicates the number of stories in the release that are currently being tested.
-   **Complete**: Indicates the number of stories in the release that are complete.

 **Note:** Stories in Ready and Cancelled states are not included in this report.

</td></tr></tbody>
</table><table id="table_r2z_c51_ddc"><thead><tr><th>

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

Identify the time taken for each story in the release to move from an in-progress state to completion.Each bubble on the graph represents a story. The height of the bubble from the x-axis shows how long that story took to move from an in-progress state to completion. The size of the story bubbles are relative to each other based on their story points.

 Hovering your mouse cursor over a bubble displays the following details about that story:

-   Story points
-   Date the story is moved to completion
-   Total cycle time \(in days\) of the story
-   Number of days that the story was in the **Work in progress** state
-   Number of days that the story was in the **Ready for testing** state
-   Number of days that the story was in the **Testing** state

 From the Story State section towards the right of the report, you can filter the report to view the cycle time of the stories for the selected states. The chart displays the cycle time for each story as the cumulative sum of all duration of the selected states.

 If there are too many stories at any area of the chart and the bubbles appear crowded on the report, you can zoom in that particular area of the report for a clearer view.

 ![Cycle Time Zoom](../image/cycle-time-zoom.gif)

</td></tr></tbody>
</table>You can customize the Burnup, Burndown, and Cumulative Flow Diagram reports. For more information, see [Customizing Agile 2.0 dashboard reports](../concept/customizing-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Agile 2.0](pa-content-pack-for-agile-2.0.md)

