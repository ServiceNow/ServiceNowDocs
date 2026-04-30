---
title: Field Service Territory Capacity Analytics dashboard
description: Use the Field Service Territory Capacity Analytics dashboard to track capacity trends with interactive charts and graphs, perform gap analysis with a customizable pivot table, and apply filters for targeted data viewing and informed decision-making.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Analytics and reporting for Field Service Management, Field Service Management]
---

# Field Service Territory Capacity Analytics dashboard

Use the Field Service Territory Capacity Analytics dashboard to track capacity trends with interactive charts and graphs, perform gap analysis with a customizable pivot table, and apply filters for targeted data viewing and informed decision-making.

![Dashboard showing interactive charts and graphs for tracking capacity trends, a customizable pivot table for gap analysis by territory and demand channel, and filter options to view data.](../image/field-service-capacity-analytics-dashboard.jpg)

## Required ServiceNow AI Platform roles

-   The fsm\_territory\_manager, fsm\_territory\_planner roles are required to access the dashboard.
-   The fsm\_resource\_manager role is required to view data related to their respective territories.

## Access the Field Service Territory Capacity Analytics dashboard in the configurable workspace

To open the dashboard, navigate to **Field Service** **&gt; Workspaces** **&gt;CSM/FSM Configurable Workspace****&gt;Home****&gt;Territory capacity** tab.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_mbt_rks_lbc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Territory Planner

</td><td>

Manages and optimizes field service resources. This involves tracking capacity trends, analyzing capacity gaps through a customizable pivot table, and applying filters for targeted data analysis.

 The planner adjusts resource allocation based on insights to minimize downtime and improve service levels, handles special events by overriding standard capacity settings, and collaborates with team members to ensure smooth field service operations.

</td></tr><tr><td>

Territory Manager

</td><td>

Optimizes performance within specific geographic areas. Monitors capacity trends with interactive charts, conduct gap analysis using a customizable pivot table, and apply filters for targeted insights.

 The manager adjusts capacity settings for special events, ensures efficient resource allocation, and drills down into detailed data on capacity usage to manage and respond to mismatches effectively.

</td></tr></tbody>
</table>## Reports

<table id="table_rbt_rks_lbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Capacity gap trend

</td><td>

Line chart

</td><td>

wm\_demand\_for\_capacity, wm\_task

</td><td>

Uses a line chart to compare allocated capacity and actual work demand over time. Allocated capacity is the assigned resources, while work demand is the actual task volume. This report identifies discrepancies to improve resource planning and optimization.

</td></tr><tr><td>

Capacity usage

</td><td>

Bar chart

</td><td>

wm\_demand\_for\_capacity

</td><td>

Uses a bar chart to display used versus unused capacity. This provides insights into resource utilization, aiding in the optimization of planning and operations.

</td></tr><tr><td>

Capacity gap analysis

</td><td>

Report

</td><td>

wm\_demand\_for\_capacity

</td><td>

The Capacity Gap Analysis report identifies gaps between allocated and actual work demand. The pivot table breaks down data by territory and demand channel, showing allocated, assigned, and unused capacity.

This helps address planning and resource allocation issues.

</td></tr></tbody>
</table>## Filters

<table id="table_tbt_rks_lbc"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date range

</td><td>

Date

</td><td>

Filter the results based on the selected date range, such as This month or This week.

</td></tr><tr><td>

Frequency

</td><td>

Reference

</td><td>

Filter the results based on the frequency such as, Daily, Weekly, Monthly, or Yearly.

</td></tr><tr><td>

Capacity by

</td><td>

Reference

</td><td>

Filter the results based on the frequency such as, hours or tasks.

</td></tr><tr><td>

Territories

</td><td>

Reference

</td><td>

Filter the results based on a selected territory and other filter selections such as Frequency, Capacity By etc.

</td></tr><tr><td>

Demand channel

</td><td>

Reference

</td><td>

Filter the results based on a selected demand channel and other filter selections such as Territory, Frequency, Capacity By etc.

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and reporting for Field Service Management](../../../product/field-service-management/concept/analytics-reporting-fsm.md)

