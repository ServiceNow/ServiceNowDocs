---
title: Agile 2.0 Team Dashboard
description: Team Dashboard provides a visualization of the team's progress on stories over a given period. It provides team predictability charts and helps you plan the team's capacity for the upcoming sprints. In addition, it provides details of all the team members.
locale: en-US
release: yokohama
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Performance Analytics Content Pack for Agile 2.0, Agile Development 2.0, Strategic Portfolio Management]
---

# Agile 2.0 Team Dashboard

Team Dashboard provides a visualization of the team's progress on stories over a given period. It provides team predictability charts and helps you plan the team's capacity for the upcoming sprints. In addition, it provides details of all the team members.

Navigate to **All** &gt; **Agile Development** &gt; **Dashboards** and select **Agile 2.0 Team Dashboard**.

![Team work item progress](../image/agile-team-wip-tab.png "Work item progress tab")

![Sprint Variance tab](../image/agile-team-sprint-variance.png "Sprint Performance tab")

![Agile team members](../image/agile-team-members.png "Team Members tab")

![Agile team Cycle Time](../image/team-cycle-time.png "Cycle Time tab")

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Team member: Needs visibility into team's predictability and progress in completing stories

</td><td>

scrum\_user

</td><td>

-   View progress of the team by work items
-   Analyze the time taken for stories to move from one state to another
-   Analyze sprint performance of the team
-   Analyze trends in sprint variance of the team comparing completed work to expected capacity and committed work

</td></tr></tbody>
</table>## Indicators

-   **Scrum: Scrum: Average Story State Duration**

    Generates data that is displayed in the Average Cycle Time per State report.

-   **Scrum: Story State Duration**

    Generates data that is displayed in the Time in State report.

-   **Scrum: Total stories in a sprint**

    Generated data that is displayed in the Active Stories by State report.


## Breakdowns

-   Scrum: Group
-   Scrum: State

## Data visualizations

The Team Dashboard reports are segregated into the following three tabs:

-   Work item progress: Reports of Active Stories by State, Time in State, and Average Cycle Time per State
-   Sprint Performance: Reports of Velocity History and Sprint Variance
-   Team Members: List of all the members of the team

    **Note:** For existing customers who upgrade to the latest version, the list of the team members appears in both the Work item progress and Team Members tabs but only one of these locations would display the accurate information. You can remove this widget from the Work item progress tab to avoid this issue. For more information on how to remove a widget, see [Edit a responsive dashboard](https://www.servicenow.com/docs/access?context=t_EditADashboard&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).


If you are upgrading from version 1.0.2 or earlier of Performance Analytics Content Pack for Agile 2.0, then install this dashboard from Solution Library to upgrade its layout and access the following visualizations:

-   Velocity History
-   Velocity by Type
-   Sprint Variance
-   Story Cycle Time

For more information, see [Upgrading the layout of Agile 2.0 dashboards](../reference/using-solution-library-for-agile-2.0-dashboards.md).

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active Stories by State

</td><td>

Bar chart![Bar chart](../../performance-analytics/image/column-icon.png)

</td><td>

View the total number of stories in each state of a story, for example, testing, work in progress, and testing.

</td></tr><tr><td>

Time in State

</td><td>

Stacked bar chart![Stacked bar chart](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

View the time in hours that the team spends in each state of a story.

</td></tr><tr><td>

Average Cycle Time per State

</td><td>

Line chart ![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

View how the work in progress is trending over time and what are the most significant cycle times.

</td></tr></tbody>
</table><table id="table_ohx_mw1_ddc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Velocity History

</td><td>

Bar chart![Bar chart](../../performance-analytics/image/column-icon.png)

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

 ![Stacked bar chart](../../../reuse/reporting/image/bar-stacked.svg)

</td><td>

Analyze the way your team's velocity changes over time and compare the team's strategic workload with operational or other types of workload.

 The bar charts have two stacks that show the sum of the story points of the following types of completed stories:

-   Regular stories
-   Stories added to the unified backlog from the items in the triage board

 Clicking any bar would take you to its corresponding sprint details.

 Data displayed in this report is of the past 10 sprints with the earliest sprint on the left.

 **Note:** This report is not available by default. You can add it from Scrum custom charts to your dashboard. For more information, see [Edit a responsive dashboard](https://www.servicenow.com/docs/access?context=t_EditADashboard&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Sprint Variance

</td><td>

Bar chart

 ![Bar chart](../../performance-analytics/image/column-icon.png)

</td><td>

Analyze the percentage variance of the team compared to the capacity and committed points, for the past 10 sprints.

 The Team Sprint Variance report comprises the following series per sprint that can be hidden or displayed based on your preference:

-   **Completed to Capacity**: Indicates the percentage of completed work compared to the expected capacity for the sprint.
-   **Completed to Committed**: Indicates the percentage of completed work compared to the committed work of the team for the sprint.

</td></tr></tbody>
</table><table id="table_pcn_nw1_ddc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Team Members

</td><td>

List

</td><td>

View the details of all team members.

</td></tr></tbody>
</table><table id="table_tjv_nw1_ddc"><thead><tr><th>

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

Identify the time taken for each story, which the team has worked on, to move from an in-progress state to completion.Each bubble on the graph represents a story. The height of the bubble from the x-axis shows how long that story took to move from an in-progress state to completion. The size of the story bubbles are relative to each other based on their story points.

 You can compare the cycle times of stories with different story points and analyze the trend in the time taken by the team to complete them. Identify the stories that took longer to complete and analyze the reasons so that you can chart an action plan to reduce the team's cycle time in the future.

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

 **Note:** The stories shown in this chart are the ones that the team has completed in the past 30 days.

</td></tr></tbody>
</table>**Parent Topic:**[Performance Analytics Content Pack for Agile 2.0](pa-content-pack-for-agile-2.0.md)

