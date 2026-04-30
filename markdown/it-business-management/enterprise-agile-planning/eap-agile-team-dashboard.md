---
title: EAP Agile Team dashboard
description: The Agile Team dashboard provides you with sprint progress and team performance details for an Agile team in the Enterprise Agile Planning \(EAP\) workspace.
locale: en-US
release: yokohama
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reports and dashboards, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# EAP Agile Team dashboard

The Agile Team dashboard provides you with sprint progress and team performance details for an Agile team in the Enterprise Agile Planning \(EAP\) workspace.

![Agile Team dashboard showing various data visualizations and team performance reports.](../images/eap-agile-team-dashboard.png)

You can use a default dashboard or you can configure a custom dashboard and associate it with your Agile configuration. For more information, see [Configuring custom dashboards in EAP](configuring-eap-dashboard.md).

## Required EAP roles

The EAP read-only \(sn\_apw\_advanced.eap\_read\_only\) role is required to view the dashboard.

## Access the Agile Team dashboard

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.
2.  From the Agile structure section of the navigation panel, choose your EAP team.
3.  Select the **Home** tab.

## Use cases

<table id="table_wxy_x1r_gbc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

-   Portfolio manager
-   Product manager
-   Team lead
-   Team member

</td><td>

View the progress and status of your sprint goals, stories, overall progress, and team performance.

</td></tr></tbody>
</table>## Reports

<table id="table_dw3_bj5_gbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sprint progress

</td><td>

Gauge

![Sprint progress.](../../../use/reporting/image/inline-data-vis-96px-speedometer.png)

</td><td>

sn\_apw\_advanced\_eap\_iteration

</td><td>

Percentage of points completed out of the total scope for this sprint.

</td></tr><tr><td>

Total stories

</td><td>

Single Score

![Total stories.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

rm\_story

</td><td>

Number of stories that are scheduled for this sprint.

</td></tr><tr><td>

Blocked stories

</td><td>

Single Score

![Blocked stories.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

rm\_story

</td><td>

Number of stories that are blocked for this sprint.

</td></tr><tr><td>

Total story points

</td><td>

Single Score

![Total story points.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

rm\_story

</td><td>

Sum of points of all stories that are scheduled for this sprint.

</td></tr><tr><td>

Stories missing estimates

</td><td>

Single Score

![Stories missing estimates.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

rm\_story

</td><td>

Number of stories that are scheduled for this sprint that don't have story points.

</td></tr><tr><td>

Stories by state

</td><td>

Bar graph

![Stories by state.](../../../use/reporting/image/inline-data-vis-bar-column.png)

</td><td>

rm\_story

</td><td>

Stories that are scheduled for this sprint, grouped by their current state.

</td></tr><tr><td>

What does the team plan to achieve in this iteration?

</td><td>

List

![Goals list.](../../../use/reporting/image/inline-data-vis-list.png)

</td><td>

sn\_gf\_goal

</td><td>

Status and progress of your sprint's goals.

 You can rearrange the columns of the report by selecting the Settings icon \(![Settings icon.](../../../reuse/icons/product-icons/gear-outline-24.svg)\).

</td></tr><tr><td>

Sprint burndown by story points

</td><td>

Trend

![Sprint burndown by story points.](../../../use/reporting/image/inline-data-vis-trend.png)

</td><td>

This trend uses the following indicators:-   EAP: Sum of story points of all stories in the current iteration.
-   EAP: Sum of story points of active stories in the current iteration.

</td><td>

Burndown trend comparing the sprint's ideal pace with the current pace. This report can help you analyze if the scope can be completed before the end of the sprint.

</td></tr><tr><td>

Sprint burnup by story points

</td><td>

Trend

![Sprint burnup by story points.](../../../use/reporting/image/inline-data-vis-trend.png)

</td><td>

This trend uses the following indicators:-   EAP: Sum of story points of completed stories in the current iteration.
-   EAP: Sum of story points of all the stories in the current iteration

</td><td>

Burnup trend comparing the sprint's ideal pace with the current pace. This report can help you analyze if the scope can be completed before the end of the sprint.

</td></tr><tr><td>

Avg velocity per sprint

</td><td>

Single Score

![Avg velocity per sprint.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

sn\_apw\_advanced\_eap\_iteration

</td><td>

Number of story points the team can complete per sprint. Using this metric, you can evaluate the team's average performance.

</td></tr><tr><td>

Velocity

</td><td>

Trend

![Velocity.](../../../use/reporting/image/inline-data-vis-trend.png)

</td><td>

sn\_apw\_advanced\_eap\_iteration

</td><td>

Trend of story points completed by this team in the past 90 days.

</td></tr><tr><td>

Story cycle time

</td><td>

Bubble chart

![Bubble chart representation.](../../../use/reporting/image/inline-data-vis-96px-bubble.png)

</td><td>

sn\_apw\_advanced\_story\_cycle\_time

</td><td>

Time taken for each story to move from an in-progress state to completion.Each bubble on the graph represents a story and the graph shows stories completed in the past 30 days. The height of the bubble from the x-axis shows the time \(in days\) to move from an in-progress state to completion. The size of the story bubbles is relative to each other based on their story points.

Pointing your cursor to a bubble on that chart shows story data such as story points, duration in days to complete, and name.

You can compare the cycle times of stories with different story points and analyze the trend in the time taken by the team to complete them.

**Note:** The cycle time chart currently doesn't support selecting the story bubble to drill down into the stories.

</td></tr></tbody>
</table>