---
title: Core Business Suite Analytics overview
description: The Core Business Suite \(CBS\) Analytics dashboard provides a unified view of performance metrics and resolution trends across all Business Units in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/cbs-analytics-overview.html
release: australia
product: Core Business Suite
classification: core-business-suite
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 3
keywords: [CBS Analytics, Core Business Suite Analytics, Performance Analytics, dashboard, resolution rate]
breadcrumb: [View Core Business Suite Analytics, Use, Core Business Suite]
---

# Core Business Suite Analytics overview

The Core Business Suite \(CBS\) Analytics dashboard provides a unified view of performance metrics and resolution trends across all Business Units in your organization.

## Dashboard data points

\[Omitted image "cbs-dashboard-pa.png"\] Alt text: Core Business Suite Analytics dashboard showing the main tab with performance metrics and resolution trends.

The CBS Analytics dashboard organizes data across a set of tabs and metric sections. The following data points are available on the main **Core Business Suite** tab.

|Data point|Description|
|----------|-----------|
|Dashboard summary|A summary section at the top of the dashboard. Select **Generate Summary** to produce an AI-generated overview of current dashboard data. Review the output carefully, as AI-generated content may not reflect all context and requires human verification before use.|
|Performance trends|Tracks resolution rates over a selected period. Use this section to identify trends, spot emerging bottlenecks, and evaluate whether process changes are having an effect. Adjust the date range filter to compare periods and surface patterns that a daily snapshot does not show.|
|Date range filter|Controls the time window applied to the Performance trends section. Adjust the filter to compare different periods and surface longer-term patterns.|
|AI \(Now Assist\) Resolution Rate|Displays the percentage of requests resolved by AI \(Now Assist\) over the selected date range, shown as a trend line chart with an average value for the period. This metric reflects AI-assisted resolution and should be reviewed alongside human-handled resolution data for a complete picture. AI-generated values may not reflect all context — apply human review before acting on this data.|

## Core Business Suite Analytics roles

The following roles control access to the CBS Analytics dashboard and its Performance Analytics data.

<table><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_cbs\_analytics.dashboard\_editor**

</td><td>

Grants complete access to the CBS Analytics dashboard. Users assigned this role can view and edit metric placement and configuration across all business units in the CBS Analytics dashboard.

</td></tr><tr><td>

**sn\_cbs\_analytics.dashboard\_viewer**

</td><td>

Grants read-only access to the CBS Analytics dashboard. Users assigned this role can only view metrics across all Business Units in the CBS Analytics dashboard.

</td></tr></tbody>
</table>## Business unit-specific data

BU-level data is available on the individual BU-specific tabs: **Human Resources**, **Legal**, **Health &amp; Safety**, **Workplace Services**, **Finance**, **Procurement**, **Accounts Payable Operations**, and **Supplier Lifecycle Operations**.

-   **[Human Resources analytics on the CBS dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/hr-analytics-cbs-dashboard.md)**  
The **Human Resources** tab on the Core Business Suite Analytics dashboard tracks open case volume and resolution trends for HR requests, helping managers assess workload distribution and identify staffing gaps.
-   **[Legal analytics on the CBS dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/legal-analytics-cbs-dashboard.md)**  
The **Legal** tab on the Core Business Suite Analytics dashboard tracks open legal case volume and resolution trends, helping managers identify unassigned cases and monitor legal request activity over time.
-   **[Health &amp; Safety analytics on the CBS dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/health-safety-analytics-cbs-dashboard.md)**  
The **Health &amp; Safety** tab on the Core Business Suite Analytics dashboard tracks open case volume and resolution trends for health and safety requests, helping managers monitor incident activity and staffing coverage.
-   **[Workplace Services analytics on the CBS dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/workplace-analytics-cbs-dashboard.md)**  
The **Workplace Services** tab on the Core Business Suite Analytics dashboard tracks open case volume and resolution trends for workplace service requests, helping managers monitor facility demand and staffing coverage.
-   **[Finance analytics on the CBS dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/finance-analytics-cbs-dashboard.md)**  
The **Finance** tab on the Core Business Suite Analytics dashboard tracks open case volume and resolution trends for finance requests, helping managers assess workload distribution and monitor finance case activity over time.
-   **[Procurement analytics on the CBS dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/procurement-analytics-cbs-dashboard.md)**  
The **Procurement** tab on the Core Business Suite Analytics dashboard tracks open case volume and resolution trends for procurement requests, helping managers monitor purchasing activity and identify staffing gaps.
-   **[Accounts Payable Operations analytics on the CBS dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/apo-analytics-cbs-dashboard.md)**  
The **Accounts Payable Operations** tab on the Core Business Suite Analytics dashboard tracks open case volume and resolution trends for accounts payable requests, helping managers monitor invoice and payment activity.
-   **[Supplier Lifecycle Operations analytics on the CBS dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/slo-analytics-cbs-dashboard.md)**  
The **Supplier Lifecycle Operations** tab on the Core Business Suite Analytics dashboard tracks open case volume and resolution trends for supplier requests, helping managers monitor supplier activity and identify staffing gaps.

**Parent Topic:**[View Core Business Suite Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/view-cbs-analytics.md)

