---
title: EAP Solution Train dashboard
description: The Solution Train dashboard provides a snapshot of teams' work assignment status such as capabilities, work items, and team performance.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reports and dashboards, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# EAP Solution Train dashboard

The Solution Train dashboard provides a snapshot of teams' work assignment status such as capabilities, work items, and team performance.

![Solution train inline dashboard](../images/eap-solution-train-dashboard.png)

You can use a default dashboard or you can configure a custom dashboard and associate it with your Agile configuration. For more information, see [Configuring custom dashboards in EAP](configuring-eap-dashboard.md).

## Required EAP roles

The EAP read-only \(sn\_apw\_advanced.eap\_read\_only\) role is required to view the dashboard.

## Access the Solution Train dashboard

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.
2.  From the Agile structure section of the navigation panel, choose your EAP Solution Train.
3.  Select the **Home** tab.

## Use cases

<table id="table_wxy_x1r_gbc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

-   Portfolio Manager
-   Product Manager
-   Team Lead
-   Team Member

</td><td>

View the state of capabilities assigned to the teams in your Solution Train, distribution of work items, and team performance.

</td></tr></tbody>
</table>## Reports and data visualizations

<table id="table_byy_x1r_gbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Capabilities by state

</td><td>

Bar graph

![Capabilities grouped by their current state.](../../../use/reporting/image/inline-data-vis-bar-column.png)

</td><td>

sn\_align\_core\_capability

</td><td>

Capabilities assigned to this Solution Train, grouped by their current state.

</td></tr><tr><td>

Work item distribution

</td><td>

Donut

![Distribution of work items.](../../../use/reporting/image/inline-data-vis-96px-donut.png)

</td><td>

sn\_align\_core\_capability

</td><td>

Distribution of work items for the selected attribute. You can group the data using one of the following options:-   Primary goal
-   Primary goal &gt; Category
-   Strategic program
-   Owner
-   Department

</td></tr><tr><td>

Team performance

</td><td>

List

![Evaluating child teams progress.](../../../use/reporting/image/inline-data-vis-list.png)

</td><td>

sn\_apw\_advanced\_eap\_iteration

</td><td>

Evaluate child teams progress and help them enhance their performance.

 You can choose and rearrange the columns of the report by selecting the ![Rearrange the columns.](../../../reuse/icons/product-icons/gear-outline-24.svg) icon.

</td></tr></tbody>
</table>