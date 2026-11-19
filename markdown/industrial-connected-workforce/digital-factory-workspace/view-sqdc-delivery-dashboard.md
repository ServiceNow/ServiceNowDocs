---
title: View the SQDC Analytics Delivery dashboard
description: Open the Delivery dashboard on a functional location record to track IGT and CIL completion, action SLAs, deviations, downtime, breakdowns, waste, and root cause analysis aging.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/view-sqdc-delivery-dashboard.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-05-17"
reading_time_minutes: 2
keywords: [SQDC Analytics, Delivery dashboard, IGT completion, CIL, deviations, root cause analysis]
breadcrumb: [Industrial Analytics and Reporting, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# View the SQDC Analytics Delivery dashboard

Open the Delivery dashboard on a functional location record to track IGT and CIL completion, action SLAs, deviations, downtime, breakdowns, waste, and root cause analysis aging.

## Before you begin

You have access to the functional location record in the Digital Factory Workspace.

Role required: sn\_icw\_report.user

## About this task

The Delivery dashboard is an inline page on the functional location record that displays delivery performance for the selected location. Use this dashboard to monitor task completion, deviation aging, downtime drivers, and waste during a delivery performance review.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Factory Workspace**.

2.  Open the functional location record for the area you want to analyze.

3.  In the left sidebar, select **Delivery**.

    The Delivery dashboard appears with the current production shift selected by default.

4.  Review the task and action KPI cards at the top of the dashboard.

    The Delivery dashboard displays the following single-score indicators:

    -   **IGT completion**: percentage of Industrial Guided Tasks completed within the selected period.
    -   **CIL completion**: percentage of Cleaning, Inspection, and Lubrication tasks completed within the selected period.
    -   **Action completion SLA**: average time to close actions in the period.
    -   **Planned vs. Actual production**: Percentage of actual production quantity against the planned target.
5.  Review the deviation and loss visualizations.

    The middle section of the dashboard displays the following visualizations:

    -   **Deviations**: A multi-axis chart that shows found, scheduled, fixed, and closed deviations as bars, with average age of open and fixed deviations as lines.
    -   **Loss by period**: Stacked column chart that displays daily loss duration, broken down by loss category.
    -   **Unplanned downtime**: Stacked column chart that displays daily unplanned downtime duration, broken down by subcategory, with minimum and maximum reference lines.
    -   **Total waste and scrap**: Combo chart with stacked columns for waste quantity in kilograms and a line for cost impact.
6.  Review the breakdown and root cause aging visualizations.

    The lower section of the dashboard displays the following visualizations:

    -   **Breakdown by state**: Donut chart that shows the distribution of breakdowns by lifecycle state \(Open, Scheduled, Fixed, Closed\).
    -   **Root cause analysis aging**: Average age of open root cause analysis \(RCA\) records, in days.
    -   **Breakdown analysis aging**: Average age of open breakdown analysis records, in hours.
    -   **Average RCA aging per state**: Multi-line time-series chart that shows average RCA aging in hours, broken down by RCA state.
7.  Adjust the period selector to refresh the dashboard for a different range.

    For more information, see the related task on filtering SQDC dashboards.


**Parent Topic:**[Using Industrial Analytics and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/using-industrial-analytics-and-reporting.md)

