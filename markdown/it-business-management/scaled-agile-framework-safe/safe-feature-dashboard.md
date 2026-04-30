---
title: SAFe Feature Dashboard
description: The SAFe Feature Dashboard provides a visualization of the changes in scope and the progress of the stories in the feature over a given period.
locale: en-US
release: zurich
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe Feature Dashboard

The SAFe Feature Dashboard provides a visualization of the changes in scope and the progress of the stories in the feature over a given period.

![SAFe Feature Summary](../image/safe-feature-summary.png "Feature Summary tab")

![SAFe Feature Cycle Time tab](../image/safe-feature-cycle-time.png "Cycle Time tab")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|SAFe ART user: View the amount of work that has been completed in a feature. Gauge whether the feature can be completed on time.|SAFe\_scrum\_user|

## Indicators

-   **SAFe: Sum of story points of all stories in the feature**

    Generates the completed line in the Feature Burnup report.

-   **SAFe: Sum of story points of completed stories in feature**

    Generates the scope line in the Feature Burnup report.


## Widgets

-   **Stories**

    Indicates the total number of stories in the feature.

-   **Scope**

    Indicates the scope of the feature which is in story points. This widget lets you see at a glance how much work must be completed in a feature.

-   **Stories Missing Estimates**

    Indicates the number of stories in the feature that are missing estimates.

-   **Blocked Work**

    Indicates the amount of work \(in story points\) in the feature that is blocked.


## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Essential SAFe, then install this dashboard from Solution Library to upgrade its layout and access the following visualizations:

-   Feature Burnup
-   Story Cycle Time

For more information, see [Using Solution Library for Essential SAFe dashboards](../reference/using-solution-library-for-essential-safe-dashboards.md).

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Stories By State

</td><td>

Bar chart![](../../reporting/image/inline-data-vis-96px-bar-vertical.png)

</td><td>

At a single glance, understand the overall progress of a feature seeing all of its stories grouped by state.

</td></tr><tr><td>

Feature Burnup

</td><td>

Line chart![](../../reporting/image/inline-data-vis-96px-line.png)

</td><td>

Indicates the scope changes, if any, and trends of those scope changes. You can estimate when the feature is likely to be completed.

 The Feature Burnup report comprises the following series that can be hidden or displayed based on your preference:

-   **Scope**: Indicates the size of the feature, as the sum of story points defined in this feature.
-   **Scope Forecast**: Predicts the possibility of scope change for the future dates, which is based on historical data.
-   **Completed**: Indicates the amount of work \(in story points\) in the feature that is complete.
-   **Completed Forecast**: Predicts the burnup for the future dates. It indicates whether you can complete the feature on time. This prediction is based on historical data.

**Note:** The point at which the Completed Forecast series intersects with or crosses the Scope Forecast series is a predictor for when the feature might be completed. If the Completed Forecast series and the Scope Forecast series do not appear to ever intersect, it is a warning that scope is being added faster than work is being completed.

</td></tr></tbody>
</table><table id="table_xqh_c1b_ddc"><thead><tr><th>

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

Identify the time taken for each story in the feature to move from an in-progress state to completion.Each bubble on the graph represents a story. The height of the bubble from the x-axis shows how long that story took to move from an in-progress state to completion. The size of the story bubbles are relative to each other based on their story points.

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
</table>You can customize the Burnup report. For more information, see [Customizing Essential SAFe dashboard reports](../concept/customizing-safe-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](pa-content-pack-essential-safe.md)

