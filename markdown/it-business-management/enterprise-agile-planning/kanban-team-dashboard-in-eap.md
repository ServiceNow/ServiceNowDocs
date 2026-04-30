---
title: Kanban Team dashboard in EAP
description: The Kanban Team Dashboard in EAP provides the work item status and progress metrics for the Agile teams following the Kanban configuration in the Enterprise Agile Planning \(EAP\) workspace.
locale: en-US
release: xanadu
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reports and dashboards, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Kanban Team dashboard in EAP

The Kanban Team Dashboard in EAP provides the work item status and progress metrics for the Agile teams following the Kanban configuration in the Enterprise Agile Planning \(EAP\) workspace.

![Kanban team dashboard in Enterprise Agile Planning Workspace.](../images/eap-dashboard-kanban-team.png)

## Required EAP roles

sn\_apw\_advanced.eap\_read\_only or the sn\_apw\_advanced.eap\_user.

## Access the Kanban Team dashboard

To open the dashboard:

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.
2.  From the Agile structure section of the navigation panel, choose your Kanban EAP Portfolio.
3.  Select the **Home** tab.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

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

View the progress and status of the work items assigned to your Kanban team.

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

Total stories

</td><td>

Single Score

![Total stories.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

rm\_story

</td><td>

Number of stories assigned to this team.

</td></tr><tr><td>

Total story points

</td><td>

Single Score

![Total story points.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

rm\_story

</td><td>

Sum of points of all stories assigned to this team.

</td></tr><tr><td>

Blocked stories

</td><td>

Single Score

![Blocked stories.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

rm\_story

</td><td>

Number of stories that are assigned to this team and that are blocked.

</td></tr><tr><td>

Stories missing estimates

</td><td>

Single Score

![Stories missing estimates.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

rm\_story

</td><td>

Number of stories assigned to this team that don't have story points.

</td></tr><tr><td>

Stories by state

</td><td>

Bar graph

![Stories by state.](../../../use/reporting/image/inline-data-vis-bar-column.png)

</td><td>

rm\_story

</td><td>

Stories assigned to this team, grouped by their current state.

</td></tr></tbody>
</table>