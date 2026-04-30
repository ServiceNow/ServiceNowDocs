---
title: Field Service Territory Performance Analytics dashboard
description: Use this dashboard to view and analyze performance analytics such as open work order tasks, agent utilization on work order tasks, and average travel time across territories.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Analytics and reporting for Field Service Management, Field Service Management]
---

# Field Service Territory Performance Analytics dashboard

Use this dashboard to view and analyze performance analytics such as open work order tasks, agent utilization on work order tasks, and average travel time across territories.

![Field Service Performance Analytics dashboard showing work order and work order task information with tiles containing line graphs.](../../../product/field-service-management/image/territory-performance-analytics.png)

## Required ServiceNow AI Platform roles

The wm\_admin role is needed to manage work orders.

## Access the Field Service Territory Performance Analytics dashboard

To open the dashboard, navigate to **Workspaces** **&gt; Platform Analytics Workspace** **&gt; Dashboards** **&gt; Field Service Territory Performance Analytics**.

## Use cases

For examples of how different people in your organization would use this dashboard, see the following use cases.

<table id="table_ov2_tj4_2fb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

FSM Territory Planner

</td><td>

Can create new territories and see how the territories are being used for better allocation of field service resources and take actions based on the data shown.

</td></tr><tr><td>

FSM Territory Manager

</td><td>

Can manage territories, create new child territories and see how the territories are being used for better allocation of field service resources and take actions based on the data shown.

</td></tr></tbody>
</table>## Data visualizations

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Open Work Order Tasks|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Number of open work order tasks.|
|Mean Time to resolve work order tasks|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Average Closing time of work.|
|% Productive time for Work Order Tasks|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Number of hours agents spent working on the tasks in the last 60 days.|
|% Agent utilization for work order tasks|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Number of agents assigned to work on the tasks in the last 60 days.|
|Average Travel Time for Work order tasks order tasks shown territory wise|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Average Travel time for work order tasks shown territory wise.|
|Total WOT per Territory|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Number of Work Order Tasks per territory.|

## Filters

|Name|Filter type|UI control type|Description|
|----|-----------|---------------|-----------|
|Territory|Reference|Multi select Input|Filter the report results based on a selected territory.|
|Date|Date|Single select date|Filter the report based on the selected date.|

**Parent Topic:**[Analytics and reporting for Field Service Management](../../../product/field-service-management/concept/analytics-reporting-fsm.md)

