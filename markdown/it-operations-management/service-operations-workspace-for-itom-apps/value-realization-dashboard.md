---
title: AIOps Value Realization dashboard
description: The AIOps Value Realization dashboard uses Performance Analytics to offer comprehensive visibility into the business outcomes of alerts, events, and incidents. It features metrics such as noise reduction \(events to alerts compression\), average MTTR for incidents created by Event Management\[var.event-mgmt\], and the most critical services impacted by hours.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [AIOps Dashboards in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# AIOps Value Realization dashboard

The AIOps Value Realization dashboard uses Performance Analytics to offer comprehensive visibility into the business outcomes of alerts, events, and incidents. It features metrics such as noise reduction \(events to alerts compression\), average MTTR for incidents created by Event Management\[var.event-mgmt\], and the most critical services impacted by hours.

The AIOps Value Realization dashboard includes a calendar feature that enables users to select various date ranges such as custom dates, the last 3 months, the last 30 days, the last 6 months, the last 7 days, the last year, today, and year-to-date \(YTD\). You can specify a custom start and end date and apply these selections to view reports specifically for the chosen date range. This feature facilitates tailored analysis and reporting based on specific time periods of interest.

![AIOps Value Realization dashboard date range selection](../image/aiops-value-realization-dashboard-calendar.png "AIOps Value Realization dashboard date range selection")

The AIOps Value Realization dashboard offers key insights and metrics crucial for operational efficiency and business impact assessment. It includes features such as noise reduction to enhance focus on critical issues by reducing event-to-alert conversions. Tracking average MTTR for incidents and measuring downtime on critical services aids in improving operational efficiency and prioritizing resolutions. Categorized into Operational Excellence and Business Impact sections, the dashboard provides detailed coverage on alerts grouping, swift resolution of critical incidents reported by users, and quantifying service impacts by severity to optimize operational stability.

Run the \[PA EM\] Historic Data Collection job once to enable the partial collection of historical Event Management data:

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.
2.  Select \[PA EM\] Historic Data Collection.
3.  Select **Execute Now**.

![Value realization dashboard.](../image/aiops-value-realization-dashboard.png "AIOps Value Realization dashboard key features overview")

## Prerequisites

Ensure that the Event Management application is installed.

## Required ServiceNow AI Platform roles

-   evt\_mgmt\_admin
-   evt\_mgmt\_operator

## Access the AIOps Value Realization dashboard

To open the dashboard, use one of the following methods:

-   Navigate to **All** &gt; **AIOps Dashboards** &gt; **AIOps Value** &gt; **Value Realization**.
-   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the AIOps Dashboards icon \(![AIOps Dashboards icon.](../../health-log-analytics-admin/image/aiops-operational-icon.png)\), then, from the **AIOps Operational** drop-down menu, select **AIOps Value Realization**.

## Use cases

For examples of how different people in your organization would use this dashboard, refer to these use cases.

|User|Dashboard use|
|----|-------------|
|evt\_mgmt\_admin or admin|Edit the dashboard and grant view and share permissions.|
|evt\_mgmt\_operator or admin|View the dashboard and review record details to visualize and track the business impact of alerts, events, and incidents.|

## Breakdowns

Breakdowns available in the AIOps Value Realization dashboard are:

-   Operational Excellence
-   Business Impact

## Reports

|Title|Type|Description|
|-----|----|-----------|
|Noise reduction \(events to alerts compression\)|Line graph|The compression rate from events to alert creation: a higher number indicates fewer alerts are being created.|
|Average MTTR incidents created by Event Management|Line graph|The average Mean Time to Repair \(MTTR\) of an incident created by Event Management: a lower number indicates greater efficiency of your IT team.|
|Most critical services impacted, in hours|Line graph|The total time your organization's most critical business services are impacted: a higher number indicates more time critical services are affected by open alerts.|
|Alerts grouping coverage|Line graph|The percentage of total alerts that are grouped: a higher number indicates more alerts are being correlated and grouped within an alert group.|
|Number of affected services, by severity|Line graph|The number of services impacted by alerts, grouped by severity, such as the count of services experiencing critical issues per day.|
|Number of new P1 incidents on monitored services created by users|Line graph|The number of incidents created on services monitored by Event Management: a lower number indicates fewer users are being impacted by a service outage or performance degradation.|

