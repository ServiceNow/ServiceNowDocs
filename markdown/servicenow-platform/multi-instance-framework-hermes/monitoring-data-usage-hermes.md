---
title: Monitoring data usage in Hermes
description: Monitor data usage in Hermes over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/multi-instance-framework-hermes/monitoring-data-usage-hermes.html
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administer, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Monitoring data usage in Hermes

Monitor data usage in Hermes over time.

Monitor the amount of data that is produced to the Hermes cluster over time in the Hermes Usage Dashboard.

Usage data is calculated by aggregating the size of all messages sent to the cluster. The size for each message is determined by combining the key size, if present, and the actual size of the message sent to the Hermes cluster. For example, if a 100 MB message is sent to the cluster with a 2 MB key size, 102 MB usage is recorded for the message.

## Key benefits

-   Monitor Hermes performance with insights into data inflow in megabytes for a specified time period.
-   Visualize data usage over time for all topics or a single topic.
-   Compare data usage for topics that belong to an application.

\[Omitted image "hermes-usage-dashboard.png"\] Alt text: Hermes Metrics Dashboard.

## Required roles

Either the hermes\_admin or admin role is required to view the Hermes Usage Dashboard.

## Accessing the Hermes Usage Dashboard

View usage by navigating to **All** &gt; **Hermes Messaging Service** &gt; **Usage Dashboard**.

## Use cases

-   Monitor data usage for an application. Determine if usage has increased or decreased over time.
-   View data usage for a specific topic. Determine if usage patterns changed by looking for spikes or drops in usage.
-   Look for decreased usage over time to determine if your application is producing data that isn't supported by Hermes.
-   Compare data usage for topics in a single application or all applications that belong to you.

## Reports

Data displayed in the Hermes Metrics Dashboard is collected from the Hermes usage metrics \[hermes\_usage\_metrics\] table.

-   Metric data is captured hourly, with each collection point reflecting the latest value recorded within that hour.
-   Metric data is aggregated and displayed over time. This means the dashboard enables you to view an overall trend rather than precise moment-to-moment traffic.
-   Metric data displayed on the dashboard is initially aggregated daily. Depending on the date range you select, the dashboard dynamically adjusts its view. For example, for ranges greater than 60 days, it presents the data in monthly summaries. For ranges less than 60 days, it displays daily summaries.
-   Metric data is retained for 12 months.

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Total Megabytes In|Single score|Hermes usage metrics \[hermes\_usage\_metrics\] table|View the aggregated total of data produced to Hermes in megabytes.|
|Usage trends|Trend|Hermes usage metrics \[hermes\_usage\_metrics\] table|Monitor data usage in terms of bytes in for selected topics over time.|
|Topic Usage Data|Bar|Hermes usage metrics \[hermes\_usage\_metrics\] table|Compare data usage for each topic over time.|

**Parent Topic:**[Administering Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-administration.md)

**Related topics**  


[Check the status of and connection to the Hermes Kafka cluster]()

[Tracking message usage in Hermes]()

[Cloning with Hermes Messaging Service enabled]()

[View Hermes Messaging Service log messages]()

