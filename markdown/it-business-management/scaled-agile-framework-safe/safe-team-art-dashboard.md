---
title: SAFe Team Dashboard
description: Visually analyze how a team is progressing on stories over a given period. Gain insight on the overall velocity of the team and helps you plan the team's capacity for the upcoming sprints and program increments \(PIs\). In addition, this dashboard provides details of all the team members.
locale: en-US
release: zurich
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe Team Dashboard

Visually analyze how a team is progressing on stories over a given period. Gain insight on the overall velocity of the team and helps you plan the team's capacity for the upcoming sprints and program increments \(PIs\). In addition, this dashboard provides details of all the team members.

![Work item progress tab of SAFe Team dashboard](../image/safe-team-wip-tab.png "Work item progress tab")

![Sprint performance tab of SAFe Team dashboard](../image/safe-team-sprint-variance.png "Sprint Performance tab")

![Team members tab of SAFe Team dashboard](../image/safe-team-list.png "Team Members tab")

![Cycle Time tab of SAFe Team dashboard](../image/safe-team-cycle-time.png "Cycle Time tab")

![Program Predictability tab of SAFe Team dashboard](../image/safe-team-program-predictability.png "Program Predictability")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|SAFe scrum master: View how your team is progressing on stories.|safe\_scrum\_user|

## Indicators

-   **SAFe: Average Story State Duration**

    Generates data that is displayed in the Average Cycle Time per State report.

-   **SAFe: Story State Duration**

    Generates data that is displayed in the Time in State report.


## Breakdowns

-   SAFe: State
-   SAFe: Team

## Data visualizations

The Team Dashboard visualizations are segregated into the following tabs:

-   Work item progress: Reports of Active Stories by State, Time in State, and Average Cycle Time per State
-   Sprint Performance: Reports of Velocity History and Sprint Variance
-   Team Members: List of all the members of the team

    **Note:** For existing customers who upgrade to the latest version, the list of the team members appears in both the Work item progress and Team Members tabs but only one of these locations would display the accurate information. You can remove this widget from the Work item progress tab to avoid this issue. For more information on how to remove a widget, see [Edit a responsive dashboard](https://www.servicenow.com/docs/access?context=t_EditADashboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

-   Cycle Time: Report of the story cycle for the team.
-   Program Predictability: Report of the team's historical performance in meeting the PI objectives.

If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Essential SAFe, then install this dashboard from Solution Library to upgrade its layout and access the following reports:

-   Velocity History
-   Velocity by Type
-   Sprint Variance
-   Story Cycle Time

For more information, see [Using Solution Library for Essential SAFe dashboards](../reference/using-solution-library-for-essential-safe-dashboards.md).

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active Stories By State

</td><td>

Bar chart![](../../reporting/image/inline-data-vis-96px-bar-vertical.png)

</td><td>

View the total number of stories in each state of a story, for example, testing, work in progress, and testing.

</td></tr><tr><td>

Time in State

</td><td>

Bar chart![](../../reporting/image/inline-data-vis-96px-bar-vertical.png)

</td><td>

View the time in hours that the team spends in each state of a story.

</td></tr><tr><td>

Average Cycle Time per State

</td><td>

Line chart ![](../../reporting/image/inline-data-vis-96px-line.png)

</td><td>

View how the work in progress is trending over time and what are the most significant cycle times.

</td></tr></tbody>
</table><table id="table_fl3_my1_ddc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Velocity History

</td><td>

Grouped bar chart

 ![](../../reporting/image/inline-data-vis-96px-bar-column.png)

</td><td>

Gain an insight on the overall velocity of the team for the past 10 sprints. Understand if the team is achieving a stable, predictable velocity, and is meeting the commitments.

 The Team Velocity History report comprises the following series per sprint that can be hidden or displayed based on your preference:

-   **Team Capacity**: Indicates the team capacity \(in story points\) for the sprint.
-   **Committed Story Points**: Indicates the number of story points committed by the team for the sprint.
-   **Completed Story Points**: Indicates the number of story points completed by the team for the sprint.
-   **Average Completed Points**: Indicates the average number of story points completed by the team for the sprint.
-   **Linear \(Actual\)**: Indicates if the amount of completed work is trending up, trending down, or relatively stable over sprints.

</td></tr><tr><td>

Velocity by Type

</td><td>

Stacked bar chart

 ![](../../reporting/image/inline-data-vis-96px-bar-vertical.png)

</td><td>

Analyze the way your team's velocity changes over time and compare the team's strategic workload with operational or other types of workload.

 The bar charts have two stacks that show the sum of the story points of the following types of completed stories:

-   Regular stories
-   Stories added to the unified backlog from the items in the triage board

 Clicking any bar would take you to its corresponding sprint details.

 Data displayed in this report is of the past 10 sprints with the earliest sprint on the left.

 **Note:** This report is not available by default. You can add it from Scrum custom charts to your dashboard. For more information, see [Edit a responsive dashboard](https://www.servicenow.com/docs/access?context=t_EditADashboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Sprint Variance

</td><td>

Grouped bar chart

 ![](../../reporting/image/inline-data-vis-96px-bar-column.png)

</td><td>

Analyze the percentage variance of the team compared to the capacity and committed points, for the past 10 sprints.

 The Team Sprint Variance report comprises the following series per sprint that can be hidden or displayed based on your preference:

-   **Completed to Capacity**: Indicates the percentage of completed work compared to the expected capacity for the sprint.
-   **Completed to Committed**: Indicates the percentage of completed work compared to the committed work of the team for the sprint.

</td></tr></tbody>
</table><table id="table_qxr_my1_ddc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Team Members

</td><td>

List![](../../reporting/image/inline-data-vis-96px-list.png)

</td><td>

View the details of all team members.

</td></tr></tbody>
</table><table id="table_sq1_ny1_ddc"><thead><tr><th>

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

Identify the time taken for each story, which the team has worked on, to move from an in-progress state to completion.Each bubble on the graph represents a story. The height of the bubble from the x-axis shows how long that story took to move from an in-progress state to completion. The size of the story bubbles are relative to each other based on their story points.

 You can compare the cycle times of stories with different story points and analyze the trend in the time taken by the team to complete them. Identify the stories that took longer to complete and analyze the reasons so that you can chart an action plan to reduce the team's cycle time in the future.

 Pointing your cursor over a bubble displays the following details about that story:

-   Story points
-   Date on which the story is moved to completion
-   Total cycle time \(in days\) of the story
-   Number of days that the story was in the **Work in progress** state
-   Number of days that the story was in the **Ready for testing** state
-   Number of days that the story was in the **Testing** state

 From the Story State section toward the right of the report, you can filter the report to view the cycle time of the stories for the selected states. The chart displays the cycle time for each story as the cumulative sum of all duration of the selected states.

 If there are too many stories at any area of the chart and the bubbles appear crowded on the report, you can zoom in that particular area for a clearer view.

 ![Cycle Time Zoom](../image/cycle-time-zoom.gif)

 **Note:** The stories shown in this chart are the ones that the team has completed in the past 30 days.

</td></tr></tbody>
</table><table id="table_it3_ny1_ddc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Team: Program Predictability

</td><td>

Line chart![](../../reporting/image/inline-data-vis-96px-line.png)

</td><td>

Track the historical performance of the team on achieving their PI objectives.

 The series in this report show the performance of the team, and the ART that this team belongs to, over multiple PIs.

 The horizontal axis shows the completed PIs and the vertical axis shows the range of business value achieved in percentage \(%\).

 Each series is the representation of the business value achieved, which is calculated from the planned and actual business values of the PI objectives. For more information, see [SAFe PI objectives](../../../product/agile-SAFe/concept/safe-pi-objectives.md).

 From the chart, you can if the team is consistently achieving between 80% and 100% of the set PI objectives, which is the ideal range according to SAFe.

 The Linear \(Team\) dotted-line series on the chart provides a linear regression on the business value achieved for the team. This series serves as an indication of how the scores of the business value achieved are trending.

 Pointing your cursor at a data point on any of the series gives you the numeric value of business value achieved.

 -   Clicking any of the data points for a PI on the ART series lets you drill down and see the list of PI objectives that are used to plot the chart for the PI that you clicked.

Filtering the list by setting the Type column to **Program** displays the PI objectives only for the ART.

-   Clicking any of the data points for a PI on a team series lets you drill down and see the list of PI objectives that are used to plot the chart for the PI that you clicked.

The objectives shown in this list are only for the selected team.


</td></tr></tbody>
</table>**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](pa-content-pack-essential-safe.md)

