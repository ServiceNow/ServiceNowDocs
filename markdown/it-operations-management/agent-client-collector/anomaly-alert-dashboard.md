---
title: Anomaly Alert Dashboard
description: View important anomaly alert reports in a single dashboard. Anomaly Alert Dashboard provides summaries about anomaly alerts and promoted alerts, in relation to Event Management alerts.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Anomaly Alert Dashboard

View important anomaly alert reports in a single dashboard. Anomaly Alert Dashboard provides summaries about anomaly alerts and promoted alerts, in relation to Event Management alerts.

The reports in the Anomaly Alert Dashboard use Performance Analytics indicators and Reporting, and require that Performance Analytics \(com.snc.pa\) is activated.

To access the Anomaly Alert Dashboard, navigate to **Metric Intelligence** &gt; **Reports** &gt; **Anomaly Alert Dashboard**.

Role required to view reports: evt\_mgmt\_user.

## % Daily Alerts are Promoted Anomalies

Shows the percentage of newly promoted alerts, in relation to the overall new IT alerts, for the time period. The change in minutes from the previous report is also available. Click the tile to drill down for more details.

## Avg Resolve Time of Promoted Alerts

Shows the average number of hours it took to resolve anomaly alerts that were promoted to IT alerts within the time range. The percentage point change from the previous report is also available. Click the tile to drill down for more details.

## Number of Anomaly Alerts

Shows the number of anomaly alerts that were created per day in the time range, broken down by promotion to Event Management alerts.

Bars in the chart are broken down into sections which are color coded by the associated alert type:

-   Anomaly alerts that were promoted to Event Management alerts.
-   Anomaly alerts that were not promoted to Event Management alerts.

To view further details:

-   Click **Promoted** or **Not Promoted** in the report legend, to show or hide details for an alert type.
-   Point to a section on a bar to show the date and the number of promoted or not promoted anomaly alerts for the specified day.
-   Click a bar to view a detailed scorecard for the bar.

## Learn

[What is anomaly detection?](https://www.servicenow.com/products/it-operations-management/what-is-anomaly-detection.html)

**Parent Topic:**[Metric Intelligence](operational-metrics.md)

**Related topics**  


[Performance Analytics](https://www.servicenow.com/docs/access?context=pa-overview&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

