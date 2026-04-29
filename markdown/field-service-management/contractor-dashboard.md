---
title: Contractor dashboard
description: Use this dashboard to review the status of work order tasks, agents, agent feedback, and appointments of contractor companies.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analytics and reporting, Field Service Management]
---

# Contractor dashboard

Use this dashboard to review the status of work order tasks, agents, agent feedback, and appointments of contractor companies.

![Contractor dashboard with graphical representations organized by work type and state. For the text description, refer to the table in the Reports section.](../image/contractor_dashboard.png)

## Required ServiceNow AI Platform roles

The wm\_contractor\_manager\_int role is needed to track the status of work orders and agents from the contractor companies.

## Use cases

The following use case provides an example of how an internal manager would use this dashboard.

<table id="table_ov2_tj4_2fb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Internal manager

</td><td>

Reviews the work order task progress and agent feedback results based on the selected contractor company and date range. Click any area of a chart to see the corresponding records.

</td></tr></tbody>
</table>## Data visualizations

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Non Compliant Appointments|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Number of appointments not started on time.|
|Task SLA Breach Status|Semi Donut ![](../../reporting/image/icon-semidonut-report.png)|\[Task\_sla\]|Data work order tasks that have breached the task SLA.|
|Closed Complete Tasks|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Number of work order tasks closed by agents.|
|Agents|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[Sys\_user\]|Number of agents associated with the contractor company.|
|Task Rejections|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\_rejection\]|Number of work order tasks rejected by the contractor manager.|
|Average Agent Rating|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_agent\_rating\]|Average rating of all the agents in the company.|
|Work Distribution By Work Type|Pie ![](../../reporting/image/icon-pie-report.png)|\[wm\_task\]|Percentage of work order tasks divided based on the type of work, such as install, break fix, and so on.|
|Work Distribution by state|Pie ![](../../reporting/image/icon-pie-report.png)|\[wm\_task\]|Percentage of work order tasks divided based on their real-time status, such as Assigned, Work in Progress, and so on.|

## Filters

|Name|Filter type|UI control type|Description|
|----|-----------|---------------|-----------|
|Contractor|Reference|Select Single Input|Filter the report results based on a selected contractor company or all.|
|Date Range|Date|Select Single Input|Filter the report results based on the selected date range, such as last 30 days.|

**Parent Topic:**[Analytics and reporting for Field Service Management](../../../product/field-service-management/concept/analytics-reporting-fsm.md)

