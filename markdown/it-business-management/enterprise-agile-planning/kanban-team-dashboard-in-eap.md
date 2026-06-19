---
title: Kanban Team dashboard in EAP
description: The Kanban Team Dashboard in EAP provides the work item status and progress metrics for the Agile teams following the Kanban configuration in the Enterprise Agile Planning \(EAP\) workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/enterprise-agile-planning/kanban-team-dashboard-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reports and dashboards, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Kanban Team dashboard in EAP

The Kanban Team Dashboard in EAP provides the work item status and progress metrics for the Agile teams following the Kanban configuration in the Enterprise Agile Planning \(EAP\) workspace.

\[Omitted image "eap-dashboard-kanban-team.png"\] Alt text: Kanban team dashboard in Enterprise Agile Planning Workspace.

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

\[Omitted image "inline-data-vis-96px-single-score.png"\] Alt text: Total stories.

</td><td>

rm\_story

</td><td>

Number of stories assigned to this team.

</td></tr><tr><td>

Total story points

</td><td>

Single Score

\[Omitted image "inline-data-vis-96px-single-score.png"\] Alt text: Total story points.

</td><td>

rm\_story

</td><td>

Sum of points of all stories assigned to this team.

</td></tr><tr><td>

Blocked stories

</td><td>

Single Score

\[Omitted image "inline-data-vis-96px-single-score.png"\] Alt text: Blocked stories.

</td><td>

rm\_story

</td><td>

Number of stories that are assigned to this team and that are blocked.

</td></tr><tr><td>

Stories missing estimates

</td><td>

Single Score

\[Omitted image "inline-data-vis-96px-single-score.png"\] Alt text: Stories missing estimates.

</td><td>

rm\_story

</td><td>

Number of stories assigned to this team that don't have story points.

</td></tr><tr><td>

Stories by state

</td><td>

Bar graph

\[Omitted image "inline-data-vis-bar-column.png"\] Alt text: Stories by state.

</td><td>

rm\_story

</td><td>

Stories assigned to this team, grouped by their current state.

</td></tr></tbody>
</table>