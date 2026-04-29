---
title: Monitoring data usage in Hermes
description: Monitor data usage in Hermes over time.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Monitoring data usage in Hermes

Monitor data usage in Hermes over time.

Monitor the amount of data that is produced to and consumed from the Hermes cluster over time in the Hermes Usage Dashboard.

Usage data is calculated by aggregating the size of all messages sent to the cluster. The size of the message is determined by the total payload present in Kafka, including key, header, value, and overhead. If compression is enabled, the dashboard reports the compressed payload size, which includes key, header, and message.

## Key benefits

-   Monitor Hermes performance with insights into data inflow and data outflow in megabytes for a specified time period.
-   Visualize data usage over time for all topics or a single topic.
-   Compare data usage for topics that belong to an application.

![Hermes Metrics Dashboard.](../images/hermes-usage-dashboard.png "Hermes Usage Dashboard")

## Required roles

The hermes\_admin is required to view the Hermes Usage Dashboard.

## Accessing the Hermes Usage Dashboard

View usage by navigating to **All** &gt; **Hermes Messaging Service** &gt; **Usage Dashboard**.

## Use cases

-   Monitor data usage for an application. Determine if usage has increased or decreased over time.
-   View data usage for a specific topic. Determine if usage patterns changed by looking for spikes or drops in usage.
-   Look for decreased usage over time to determine if your application is producing data that isn't supported by Hermes.
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
-   Metric data displayed on the dashboard is initially aggregated daily. Depending on the date range you select, the dashboard dynamically adjusts its view. For example, for ranges greater than 60 days, it presents the data in monthly summaries. For ranges less than 60 days, it displays daily summaries.
-   Metric data is retained for 12 months.

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Total Megabytes In|Single score|Hermes usage metrics \[hermes\_usage\_metrics\] table|View the aggregated total of data produced to Hermes in megabytes.|
|Total Megabytes Out|Single score|Hermes usage metrics \[hermes\_usage\_metrics\] table|View the aggregated total of data consumed from Hermes in megabytes.|
|Usage trends|Trend|Hermes usage metrics \[hermes\_usage\_metrics\] table|Monitor data usage in terms of bytes in and bytes out for selected topics over time.|
|Topic Usage Data|Table|Hermes usage metrics \[hermes\_usage\_metrics\] table|Monitor data usage \(bytes in and bytes out\) for all topics or specific topics.|

## Topic usage data

View data usage \(bytes in and bytes out\) by source based on the combination of application ID, service ID, and topic that you select.

Topics with the prefix \[Internal\] are for applications used only by ServiceNow. Topics that don't have this prefix are considered external.

|Application ID|Hermes Topic Option|What You See|How You Might Use It|
|--------------|-------------------|------------|--------------------|
|All|All|Two roll-up rows: one for external topics \(\*All Topics\*\), one for internal topics \(“\[Internal\]\*All Topics\*”\).|Quickly compare total data usage for external integrations and internal ServiceNow workflows organization-wide.|
|All|INSTANCE\_ALL\_TOPICS|Roll-up plus individual topic rows for all topics \(external + internal\) across the organization.|Identify which specific topics are driving the most data usage while still seeing the aggregate totals.|
|All|\*All Topics\*|External topics roll-up per application \(topics without \[Internal\] prefix\), grouped by app.|Compare external integration usage across different applications \(for example, Stream Connect, Log Export Service\).|
|All|\[Internal\]All Topics|Internal topics roll-up per application \(topics with \[Internal\] prefix\), grouped by app.|Monitor internal ServiceNow data flows across applications \(for example, IDR internal topics\).|
|Specific App|Any topic option|Usage for topics related to that application, based on the topic filter selected.|Focus on data usage for a particular application \(for example, view Log Export Service topic usage\).|

**Note:** When **All** is selected for both the Application ID and Hermes Topic, the Topic Usage Data table displays two roll-up rows: one for external topics \(\*All Topics\*\) and one for internal topics \(\[Internal\]\*All Topics\*\).

**Parent Topic:**[Administering Hermes Messaging Service](hermes-messaging-service-administration.md)

**Related topics**  


[Check the status of and connection to the Hermes Kafka cluster](../task/run-hermes-messaging-service-diagnostics.md)

[Tracking message usage in Hermes](tracking-hermes-messaging-service-usage.md)

[Cloning with Hermes Messaging Service enabled](cloning-with-hermes-messaging-service.md)

[View Hermes Messaging Service log messages](../task/view-hermes-log-messages.md)

