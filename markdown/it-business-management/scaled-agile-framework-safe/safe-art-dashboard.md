---
title: SAFe ART Dashboard
description: Visualize how the ART members are progressing on features and program increments \(PIs\) over a given period using the SAFe ART dashboard. Gain insight on the overall velocity of the ART members, historical performance of the ART on the PI objectives so that you can plan the work accordingly for the upcoming program increments.
locale: en-US
release: yokohama
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe ART Dashboard

Visualize how the ART members are progressing on features and program increments \(PIs\) over a given period using the SAFe ART dashboard. Gain insight on the overall velocity of the ART members, historical performance of the ART on the PI objectives so that you can plan the work accordingly for the upcoming program increments.

![SAFe ART Summary tab](../image/safe-ART-summary.png "ART Summary tab")

![SAFe ART cycle time](../image/safe-art-cycle-time.png "Cycle Time tab")

![SAFe ART program predictability.](../image/safe-art-program-predictability.png "Program Predictability Tab")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|SAFe ART user: View how the ART members are progressing on features and PIs.|safe\_scrum\_user|

## Data visualizations

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Essential SAFe, then install this dashboard from Solution Library to upgrade its layout and access the Story Cycle Time report. For more information, see [Using Solution Library for Essential SAFe dashboards](../reference/using-solution-library-for-essential-safe-dashboards.md).

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Feature Progress

</td><td>

Horizontal bar chart![Horizontal bar chart](../../performance-analytics/image/horizontal-bar.png)

</td><td>

View the progress of all the features that the ART members are working on.

</td></tr><tr><td>

Velocity by PI

</td><td>

Bar chart![Bar chart](../../performance-analytics/image/column-icon.png)

</td><td>

View the velocity of the ART across various PIs. Understand if the ART is achieving a stable, predictable velocity.

</td></tr></tbody>
</table><table id="table_fjt_px1_ddc"><thead><tr><th>

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

Identify the time taken for each story in the ART to move from an in-progress state to completion.Each bubble on the graph represents a story. The height of the bubble from the x-axis shows how long that story took to move from an in-progress state to completion. The size of the story bubbles are relative to each other based on their story points.

 Pointing your mouse cursor over a bubble displays the following details about that story:

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
</table><table id="table_q3d_qx1_ddc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ART: Program Predictability

</td><td>

Line chart![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Track the historical performance of the ART on achieving their PI objectives.

 The series in this report show the performance of the ART as whole and also the performance of each team of the ART.

 The horizontal axis shows the completed PIs and the vertical axis shows the range of business value achieved in percentage \(%\).

 Each series is the representation of the business value achieved, which is calculated from the planned and actual business values of the PI objectives. For more information, see [SAFe PI objectives](../../../product/agile-SAFe/concept/safe-pi-objectives.md).

 From the chart, you can see which teams are consistently achieving between 80% and 100% of the set PI objectives, which is the ideal range according to SAFe.

 The Linear \(ART\) dotted-line series on the chart provides a linear regression on the business value achieved for the ART. This series serves as an indication of how the scores of the business value achieved are trending.

 Pointing your mouse cursor at a data point on any of the series gives you the numeric value of business value achieved.

 -   Clicking any of the data points for a PI on the ART series lets you drill down and see the list of PI objectives that are used to plot the chart for the PI which you clicked.

Filtering the list by setting the Type column to **Program** displays the PI objectives only for the ART.

-   Clicking any of the data points for a PI on a team series lets you drill down and see the list of PI objectives that are used to plot the chart for the PI which you clicked.

The objectives shown in this list are only for the selected team.


</td></tr></tbody>
</table>**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](pa-content-pack-essential-safe.md)

