---
title: Contractor dashboard in the configurable workspace
description: Use this dashboard to review the status of work order tasks, agent rating, and work distribution by type and state.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Analytics and reporting for Field Service Management, Field Service Management]
---

# Contractor dashboard in the configurable workspace

Use this dashboard to review the status of work order tasks, agent rating, and work distribution by type and state.

![Field Service Contractor dashboard displaying work order task information, average agent rating, and non-compliant appointments. Additionally, graphical representations of work distribution by work type and state are displayed.](../image/seismic-dashboard.png)

## Required ServiceNow AI Platform roles

-   The wm\_contractor\_manager\_int role is needed to track the status of work orders and agents from the contractor companies.
-   The wm\_dispatcher role is needed to view work orders.

## Access the contractor dashboard in the configurable workspace

To open the dashboard, navigate to **Field Service** **&gt; Workspaces** **&gt; CSM/FSM Configurable Workspace**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_nk1_lwl_hsb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Internal Manager

</td><td>

Reviews the work order task progress and agent feedback results based on the selected contractor company and date range. Click any area of a chart to see the corresponding records.

</td></tr></tbody>
</table>## Data visualizations

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Non compliant appointments|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Number of appointments not started on time.|
|Task rejects|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\_rejection\]|Number of work order tasks rejected by the contractor manager.|
|Close completed tasks|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_task\]|Number of work order tasks closed by agents.|
|Agents|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[sys\_user\]|Number of agents associated with the contractor company.|
|Average Agent Rating|Single Score ![](../../reporting/image/icon-single-score-report.png)|\[wm\_agent\_rating\]|Average rating of all the agents in the company.|
|Task SLA breached|Semi Donut ![](../../reporting/image/icon-semidonut-report.png)|\[task\_SLA\]|Data work order tasks that have breached the task SLA.|
|Work distribution by work type|Pie ![](../../reporting/image/icon-pie-report.png)|\[wm\_task\}|Percentage of work order tasks divided based on the type of work, such as install, break fix, and so on.|
|Work distribution by state|Pie ![](../../reporting/image/icon-pie-report.png)|\[wm\_task\]|Percentage of work order tasks divided based on their real-time status, such as Assigned, Work in Progress, and so on.|

## Filters

|Name|Type|Description|
|----|----|-----------|
|Contractor|Reference|Filter the report results based on a selected contractor company or all.|
|Date Range|Date|Filter the report results based on the selected date range, such as last 30 days.|

**Parent Topic:**[Analytics and reporting for Field Service Management](../../../product/field-service-management/concept/analytics-reporting-fsm.md)

