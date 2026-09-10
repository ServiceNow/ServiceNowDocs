---
title: Team sprint tracker dashboard in Collaborative Work Management
description: The Team sprint tracker dashboard supports agile use cases with widgets that visualize sprint progress, workload, and trend data for agile teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/collaborative-work-management/cwm-team-sprint-tracker-dashboard.html
release: zurich
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 3
breadcrumb: [Monitor and track work using dashboards in CWM, Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Team sprint tracker dashboard in Collaborative Work Management

The Team sprint tracker dashboard supports agile use cases with widgets that visualize sprint progress, workload, and trend data for agile teams.

This dashboard provides data for active sprints that have started and aren't yet complete.

\[Omitted image "cwm-team-sprint-tracker-dashboard.png"\] Alt text: Team sprint tracker dashboard.

<table id="table_cwm_agile_widgets"><thead><tr><th>

Widget

</th><th>

Description

</th><th>

Chart type

</th></tr></thead><tbody><tr><td>

Sprint progress

</td><td>

Percentage of points completed out of the total scope for the active sprint.**Note:** Scrum tasks aren't considered for the Sprint Progress chart.

</td><td>

Dial score

</td></tr><tr><td>

Sprint tasks missing estimates

</td><td>

Number of tasks, stories, or other work items scheduled for the active sprint that don't have story points set.

</td><td>

Single score

</td></tr><tr><td>

Sprint burnup

</td><td>

Burnup trend comparing the active sprint's ideal pace with the current pace to determine if the scope can be completed before the end of the sprint.The chart shows three lines to depict the completed points, total story points in scope and the ideal pace.

**Note:** To view the Sprint burnup chart, the **CWM Daily Sprint Data Collection** scheduled job must be enabled and its **Run as** and **Run as tz** fields set. After the job is active, data for active sprints is collected daily, and chart data is available starting the day after the job first runs. For more information, see [Activate the sprint data job for burnup and burndown widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-activate-daily-sprint-data-collection-job.md).

</td><td>

Sprint chart

</td></tr><tr><td>

Sprint burndown

</td><td>

Burndown trend comparing the active sprint's remaining work against the total sprint scope to determine if the scope can be completed before the end of the sprint. This tracks the daily progress of the active sprint.The chart shows two lines to depict the actual remaining work and total sprint scope.

**Note:** To view the Sprint burndown chart, the **CWM Daily Sprint Data Collection** scheduled job must be enabled and its **Run as** and **Run as tz** fields set. After the job is active, data for active sprints is collected daily, and chart data is available starting the day after the job first runs. For more information, see [Activate the sprint data job for burnup and burndown widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-activate-daily-sprint-data-collection-job.md).

</td><td>

Sprint chart

</td></tr><tr><td>

Sprint velocity

</td><td>

Trend of story points committed versus story points completed for the last six completed sprints, with a running average velocity line.**Note:** There must be at least one completed sprint for data to be displayed in this widget. If there are more than six completed sprints, it displays data only for the last six sprints.

</td><td>

Sprint chart

</td></tr><tr><td>

Sprint tasks by state

</td><td>

Tasks scheduled for the sprint, grouped by their current states: Open, Work in Progress, Completed and Other. For more information about state buckets, see [Grouping of tasks in status reports of CWM My Work](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/grouping-of-tasks-in-status-reports-of-cwm-my-work.md).

</td><td>

Bar chart

</td></tr><tr><td>

Sprint workload by assignee

</td><td>

Count of all tasks in the active sprint, grouped by assignee. Unassigned tasks are grouped under Unassigned.

</td><td>

Bar chart

</td></tr><tr><td>

Sprint spillover

</td><td>

Total story points carried over from the past sprints into the active sprint.Each bar denotes the total story points spilled over in a sprint.

**Note:**

-   There must be at least one completed sprint for data to be displayed in this widget. If there are more than six completed sprints, it displays data only for the last six sprints.
-   The widget shows accurate data only for sprints completed after the latest version upgrade \(version 11.0.1\) of Collaborative Work Management. Sprints completed in earlier versions show zero spillover as task spillover wasn't tracked earlier.

</td><td>

Bar chart

</td></tr></tbody>
</table>The Team sprint tracker dashboard in My Space is named My sprint tracker.

**Parent Topic:**[Monitor and track work using dashboards in CWM Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-board-dashboards.md)

