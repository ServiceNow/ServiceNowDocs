---
title: HLA Operational dashboard
description: The Health Log Analytics Operational dashboard uses Performance Analytics to enable you to monitor log data, alerts, and error rate information in Service Operations Workspace and address issues as they occur in the system.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [AIOps Dashboards in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# HLA Operational dashboard

The Health Log Analytics Operational dashboard uses Performance Analytics to enable you to monitor log data, alerts, and error rate information in Service Operations Workspace and address issues as they occur in the system.

![HLA Operational dashboard](../../../product/health-log-analytics-admin/image/hla-operational-dashboard2.png)

## Prerequisites

Ensure that the Health Log Analytics application is installed.

## Required ServiceNow AI Platform roles

-   evt\_mgmt\_admin
-   evt\_mgmt\_operator

## Access the HLA Operational dashboard

To open the dashboard, use one of the following methods:

-   Navigate to **All** &gt; **AIOps Dashboards** &gt; **AIOps Operational** &gt; **HLA Operational**.
-   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the AIOps Dashboards icon \(![AIOps Dashboards icon.](../../../product/health-log-analytics-admin/image/aiops-operational-icon.png)\), then display the HLA Operational dashboard.

## Use cases

These use cases provide examples of how different people in your organization would use this dashboard.

|User|Dashboard use|
|----|-------------|
|evt\_mgmt\_admin|Edits the dashboard and grants view and share permissions.|
|evt\_mgmt\_operator or evt\_mgmt\_admin|Monitors the dashboard to visualize and track HLA log and alerts data, error rates, and other relevant information.|

## Breakdowns

Breakdowns available in the HLA Operational dashboard are:

-   HLA Overview
-   Error rate

## Reports

<table id="table_dnj_5rx_byb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logs processed

</td><td>

Bar chart

</td><td>

The number of logs that were processed and analyzed in the selected period. By default, the dashboard visualizes log data that was ingested in the last 24 hours.

</td></tr><tr><td>

Active alerts created by logs

</td><td>

Table

</td><td>

Detailed data on all currently active alerts.

</td></tr><tr><td>

Endpoints streamed

</td><td>

Line graph

</td><td>

The number of endpoints \(IPs, networks, and devices\) that are streaming into Health Log Analytics, by application service.

</td></tr><tr><td>

Logs by level state

</td><td>

Bar chart

</td><td>

The severity level of the logs for the streaming sources.

</td></tr><tr><td>

Logs per application service

</td><td>

Line graph

</td><td>

The number of logs streamed for each application service in the selected period.

 Monitor this data to ensure that log data is streaming as expected for each application service.

</td></tr><tr><td>

Logs per host

</td><td>

Line graph

</td><td>

The number of processed logs for each host in the selected period.

 Monitor this data to detect hosts that are logging more or less data than expected.

</td></tr><tr><td>

Error rate per application service

</td><td>

Line graph

</td><td>

The number of logs with errors for each application service analyzed in the selected period.

 Monitor this data to further investigate the errors.

**Note:** Health Log Analytics automatically creates alerts for Error anomalies.

</td></tr><tr><td>

Error rate per component

</td><td>

Line graph

</td><td>

The number of logs with errors for each component analyzed in the selected period.

 Monitor this data to ensure that the error rate for each component is normal.

</td></tr></tbody>
</table>