---
title: View the SQDC Analytics Overview dashboard
description: Open the Overview dashboard on a functional location record to review Overall Equipment Effectiveness \(OEE\), safety incidents, standard task completion, Planned vs. Actual production, and loss analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/view-sqdc-overview-dashboard.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-05-17"
reading_time_minutes: 1
keywords: [SQDC Analytics, Overview dashboard, OEE, safety incidents, losses]
breadcrumb: [Industrial Analytics and Reporting, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# View the SQDC Analytics Overview dashboard

Open the Overview dashboard on a functional location record to review Overall Equipment Effectiveness \(OEE\), safety incidents, standard task completion, Planned vs. Actual production, and loss analysis.

## Before you begin

You have access to the functional location record in the Digital Factory Workspace.

Role required: sn\_icw\_report.user

## About this task

The Overview dashboard is an inline page on the functional location record that displays SQDC performance for the selected location. Use this dashboard to review overall equipment effectiveness, safety incidents, task completion, production attainment, and loss trends during cadence reviews or shift handovers.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Factory Workspace**.

2.  Locate and open the functional location record for the area you want to analyze.

    Use the equipment hierarchy or search to find the functional location. To open the dashboard for your assigned functional location in one step, select **My work area** on the landing page.

3.  In the left sidebar, select **Overview**.

    The Overview dashboard appears with the current production shift selected by default. A breadcrumb at the top of the page shows the equipment hierarchy for the selected location.

4.  Review the KPI cards at the top of the dashboard.

    The Overview dashboard displays the following single-score indicators:

    -   **OEE**: Current Overall Equipment Effectiveness percentage with a 70% target.
    -   **Safety incidents**: Total incidents for the period with a trend indicator.
    -   **Standard task completion**: Percentage of Industrial Guided Tasks \(IGT s\) completed out of those created.
5.  Review the production and loss charts in the lower section of the dashboard.

    The lower section contains the following visualizations:

    -   **Products planned vs. Actual**: time-based column chart that compares planned production, actual production, and calculated loss per day.
    -   **Losses by category**: Pareto chart that ranks loss categories in descending order by total loss.
    -   **Losses by period**: stacked column chart that displays loss duration in minutes, broken down by loss category, with minimum and maximum reference lines.
6.  Adjust the period selector to refresh the dashboard for a different range.

    For more information, see the related task on filtering SQDC dashboards.


**Parent Topic:**[Using Industrial Analytics and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/using-industrial-analytics-and-reporting.md)

