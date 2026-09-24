---
title: Monitoring data usage in Hermes
description: Monitor data usage in Hermes over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/monitoring-data-usage-hermes.html
release: brazil
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Administer, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Monitoring data usage in Hermes

Monitor data usage in Hermes over time.

Monitor the amount of data that is produced to and consumed from the Hermes cluster over time in the Hermes Usage Dashboard.

Usage data is calculated by aggregating the size of all messages sent to the cluster. The size of the message is determined by the total payload present in Kafka, including key, header, value, and overhead. If compression is enabled, the dashboard reports the compressed payload size, which includes key, header, and message.

## Key benefits

-   Monitor Hermes performance with insights into data inflow and data outflow in megabytes for a specified time period.
-   Visualize data usage over time for all topics, a single topic, or multiple applications.
-   Compare data usage for topics that belong to an application.

\[Omitted image "hermes-usage-dashboard.png"\] Alt text: Hermes Metrics Dashboard.

## Required roles

The hermes\_admin role is required to view the Hermes Usage Dashboard.

## Accessing the Hermes Usage Dashboard

View usage by navigating to **All** &gt; **Hermes Messaging Service** &gt; **Usage Dashboard**.

## Multi-select for Application ID filter

The Application ID filter displays full descriptive names alongside application identifiers. This makes it easier to identify and select the application you want to monitor without needing to know internal shorthand codes. Only applications with active metrics collection appear in the filter.

|Application ID|Display Name|
|--------------|------------|
|idr|Instance Data Replication|
|cnc|ITSM DEX|
|sn\_streamconnect|Stream Connect|
|sn\_logstoanalytics|Log Export Service|

The Application ID filter now supports selecting multiple applications simultaneously. Previously, you could only view one application at a time. With multi-select option, you can do the following:

-   Compare data usage across multiple applications in a single view.
-   View aggregate Total MB In and MB Out across all selected applications.
-   View Topic Usage Data table with a separate row per selected application.

For example, you can select both IDR – Instance Data Replication and Stream Connect to view their combined and individual usage side by side.

## Use cases

-   Monitor data usage for an application. Determine if usage has increased or decreased over time.
-   View data usage for a specific topic. Determine if usage patterns changed by looking for spikes or drops in usage.
-   Compare data usage for topics in a single application or all applications that belong to you.
-   Analyze total bytes in and bytes out based on the source.
    -   **Instance**

        Total bytes sent to and consumed from a topic by the instance. For example, select **Instance** to view log volume produced to a topic by Log Export Service.

    -   **Customer**

        Total bytes sent to and consumed from a topic by an external customer application. For example, select **Customer** to view log volume consumed from a topic by an external application.

    -   **Other**

        Total bytes sent to and consumed from a topic by an internal ServiceNow application.

    -   **All**

        Aggregation of all Consumer, Instance, and Other values.


## Reports

Data displayed in the Hermes Metrics Dashboard is collected from the Hermes usage metrics \[hermes\_usage\_metrics\] table.

-   Metric data is captured hourly, with each collection point reflecting the latest value recorded within that hour.
-   Metric data is aggregated and displayed over time. This means the dashboard enables you to view an overall trend rather than precise moment-to-moment traffic.
-   Metric data displayed on the dashboard is initially aggregated daily. The dashboard automatically determines the best aggregation based on the date range selected:
    -   Previous months: Data is displayed using monthly aggregates, giving you a clean summary of usage for each completed month.
    -   Current month: Data is displayed using daily aggregates, so you can see up-to-date usage as it accumulates throughout the month.
    -   Today: When your end date is today, hourly data is included, giving you the most current view of usage activity.
-   Metric data is retained for 12 months.

    If your selected date range spans both past and current months, the dashboard combines monthly summaries for the historical portion with daily and hourly data for the current period. For example, querying January 1 – April 9 \(today is April 9\).

    |Period|Aggregation|
    |------|-----------|
    |January|Monthly|
    |February|Monthly|
    |March|Monthly|
    |April 1 – April 8|Daily|
    |April 9 \(today\)|Hourly|

    The line graph has also been updated to display monthly trends when viewing extended date ranges, making it easier to identify long-term usage patterns.


|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Total Megabytes In|Single score|Hermes usage metrics \[hermes\_usage\_metrics\] table|View the aggregated total of data produced to Hermes in megabytes.|
|Total Megabytes Out|Single score|Hermes usage metrics \[hermes\_usage\_metrics\] table|View the aggregated total of data consumed from Hermes in megabytes.|
|Usage trends|Trend|Hermes usage metrics \[hermes\_usage\_metrics\] table|Monitor data usage in terms of bytes in and bytes out for selected topics over time.|
|Topic Usage Data|Table|Hermes usage metrics \[hermes\_usage\_metrics\] table|Monitor data usage \(bytes in and bytes out\) for all topics or specific topics.|

## Topic usage data

View data usage \(bytes in and bytes out\) by source based on the combination of application ID, service ID, and topic that you select.

The Topic Usage Data table displays only topics associated with a recognized application. Topics that were created without an Application ID no longer appear in the table or in the Hermes Topic filter.

The following are the available options in the Hermes Topic filter:

-   **All - Summary** — Displays one aggregated total row per selected application. Use this for a quick snapshot of overall usage.
-   **All - Detailed** — Displays individual rows per topic. Use this to identify which specific topics are driving the most data usage. The sum of all rows in All - Detailed equals the All - Summary total.

|Application ID|Hermes Topic Option|What You See|How You Might Use It|
|--------------|-------------------|------------|--------------------|
|All|All - Summary|One aggregate row per selected application.|Quickly compare total data usage across applications.|
|All|All - Detailed|Individual topic rows for all applications, excluding aggregate entries.|Identify which specific topics are driving the most usage across your organization.|
|Single App|All - Summary|One aggregate row for that application.|Get a total usage snapshot for a specific application.|
|Single App|All - Detailed|One row per individual topic for that application.|Drill into topic-level usage for a specific application.|
|Multiple Apps|All - Summary|One aggregate row per each selected application.|Compare total usage side by side across selected applications.|
|Multiple Apps|All - Detailed|One row per topic for each selected application.|Analyze topic-level breakdown across multiple applications simultaneously.|
|Any|Specific Topic|One row for that topic.|Focus on usage patterns for a single topic.|

**Parent Topic:**[Administering Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-administration.md)

**Related topics**  


[Managing Hermes settings]()

[Check the status of and connection to the Hermes Kafka cluster]()

[Tracking message usage in Hermes]()

[Cloning with Hermes Messaging Service enabled]()

[View Hermes Messaging Service log messages]()

