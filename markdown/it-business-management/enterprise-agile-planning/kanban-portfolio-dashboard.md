---
title: Kanban Portfolio dashboard in EAP
description: The Kanban Portfolio dashboard in Enterprise Agile Planning \(EAP\) provides progress metrics and work item status for your EAP portfolios of the Kanban configuration.
locale: en-US
release: xanadu
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reports and dashboards, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Kanban Portfolio dashboard in EAP

The Kanban Portfolio dashboard in Enterprise Agile Planning \(EAP\) provides progress metrics and work item status for your EAP portfolios of the Kanban configuration.

![Kanban Portfolio dashboard in Enterprise Agile Planning.](../images/eap-dashboard-kanban-portfolio.png)

## Required EAP roles

sn\_apw\_advanced.eap\_read\_only or the sn\_apw\_advanced.eap\_user.

## Access the Kanban Portfolio dashboard

To open the dashboard:

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.
2.  From the Agile structure section of the navigation panel, choose your Kanban EAP Portfolio.
3.  Select the **Home** tab.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_kck_fqh_cfc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

-   Portfolio manager
-   Product manager
-   Team lead
-   Team member

</td><td>

View the active work items assigned to the teams in your portfolio and the distribution of work items.

</td></tr></tbody>
</table>## Reports

<table id="table_byy_x1r_gbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Epics by state

</td><td>

Bar graph

![Epics by state.](../../../use/reporting/image/inline-data-vis-bar-column.png)

</td><td>

sn\_align\_core\_scrum\_epic

</td><td>

Epics assigned to this Kanban portfolio, grouped by their current state.

</td></tr><tr><td>

Work item distribution

</td><td>

Donut

![Work item distribution.](../../../use/reporting/image/inline-data-vis-96px-donut.png)

</td><td>

sn\_align\_core\_scrum\_epic

</td><td>

Distribution of work items for the selected attribute. You can group the data using one of the following options:-   Primary goal
-   Primary goal &gt; Category
-   Strategic program
-   Owner
-   Department

</td></tr></tbody>
</table>