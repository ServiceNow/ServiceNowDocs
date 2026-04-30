---
title: Exploring Health Log Analytics
description: ServiceNow Health Log Analytics predicts IT issues before they affect your users by collecting, analyzing, and correlating machine-generated log data in real time. It discovers anomalies and alerts you to potential issues.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Exploring Health Log Analytics

ServiceNow Health Log Analytics predicts IT issues before they affect your users by collecting, analyzing, and correlating machine-generated log data in real time. It discovers anomalies and alerts you to potential issues.

## Health Log Analytics overview

Health Log Analytics typically receives and processes log data and sends events to ServiceNow Event Management. The application discovers anomalies as they happen and helps you identify the root cause of an issue by enabling you to triage related logs and analyze the raw data.

Health Log Analytics can handle any kind of machine-generated textual log data. It can process application, infrastructure, and network logs, as well as other types of textual log data. Although a configuration management database \(CMDB\) can be helpful to generate high-quality events and alerts, it is not necessary.

**Note:**

-   Health Log Analytics supports only UTF-8 logs. It does not support binary logs.
-   If you are sending logs in a language other than English, additional configuration may be required.

## Health Log Analytics users

<table id="table_km4_gdw_c2c"><thead><tr><th>

User

</th><th>

Description

</th><th>

Role

</th></tr></thead><tbody><tr><td>

Administrator

</td><td>

Configures the Health Log Analytics application to make it ready for use by Operators.Performs administration tasks to keep the system running efficiently.

</td><td>

evt\_mgmt\_admin, admin

</td></tr><tr><td>

Operator

</td><td>

Analyzes Log Analytics alerts and takes action to help resolve the underlying issue.

</td><td>

evt\_mgmt\_operator

</td></tr></tbody>
</table>## Health Log Analytics workflow

Health Log Analytics collects and processes log data automatically. It structures the data logically for operators to analyze, and generates meaningful alerts and suggestions that display in Event Management.

The diagram shows the Health Log Analytics workflow from collecting the data through sending an event or alert to Event Management.

![Health Log Analytics workflow: Ingestion - Structuring - Enrichment - Analysis - ML & AI - Alert in Event Management](../image/hla-workflow-img.png "Health Log Analytics workflow")

-   **Ingestion**

    This layer connects your environment to Health Log Analytics. You can stream your logs directly from servers and endpoints or from log repositories. The optional guided setup helps you create data input connectors for common data sources, such as:

    -   Rsyslog
    -   Beats
    -   Splunk
    -   Elasticsearch
    -   MID Server
    -   TCP
-   **Structuring**

    This layer deals with structuring log data and auto-mapping it to logical silos, called Components. Data structuring can be done automatically or manually.

    The system auto-structures log data by extracting the following properties from incoming log messages: Message, Timestamp, Host, Severity, and External-IDs. It extracts explicit values, like "property-name" and "value is IP." and semantic ones such as length, number of English words, and variance.

    Auto-mapping assigns log samples and metadata to the appropriate tags automatically. The system tries to map log lines by analyzing the source that streams the data. The mapping is based on agent hints and common transport header fields.

-   **Enrichment**

    This layer handles identifying the variable parts of a log message.

    ![Health Log Analytics workflow - Enrichment.](../image/hla-enrichment-img.png "Health Log Analytics workflow - Enrichment")

    It also identifies keywords and contextual properties. In the image, "WARN" and "Failed" are the keywords to track. "User," "source IP," and "port" are the contextual properties.

-   **Analysis**

    In this layer, each log line is indexed. Health Log Analytics extracts properties from the inner log message that contribute to models of behavior that the system learns to expect. Anomalous behavior departs from this expected behavior. You can search for an event and its most significant properties for manual triaging.

-   **Machine Learning \(ML\) and Artificial Intelligence \(AI\)**

    Health Log Analytics uses advanced unsupervised machine-learning algorithms to discover patterns within logs and learn their unique data behavior. It then sets dynamic thresholds based on the data signature in real time to detect issues when they first occur. When the system detects a deviation from the typical pattern, it sends an event to Event Management.

-   **Alert in Event Management**

    Health Log Analytics sends events to Event Management. In Event Management, Health Log Analytics alerts appear in the **All alerts** list. This list enables operators to see alerts from the event and the Health Log Analytics alert type in a single location.


## Health Log Analytics benefits

|Benefit|Feature|User|
|-------|-------|----|
|Simplify data input setup using the guided setup.|[Guided setup](../task/hla-data-input-setup-guided.md)|Administrator|
|Set up log data connector integrations quickly and conveniently from the Integrations Launchpad.|[Log data connector integrations](hla-data-input-setup-integrations.md)|Administrator|
|Shorten onboarding time by installing content packs.|[Content packs](hla-content-packs.md)|Administrator|
|Save time and reduce errors by migrating data input configurations between instances.|[Data input migration](hla-data-input-migration.md)|Administrator|
|Identify the root cause of an alert by analyzing the logs that surround the anomaly.|[Surrounding logs](../../health-log-analytics-operator/concept/hla-op-surrounding-logs-view-concept.md)|Operator|
|Visualize anomalous log data on the Log viewer.|[Log viewer](../../health-log-analytics-operator/concept/hla-op-logs-log-viewer-concept.md)|Operator|
|Detect relationships in log data.|[Log correlators](../../health-log-analytics-operator/concept/hla-op-correlator-what-is-a.md)|Operator|
|Assign higher or lower significance to alerts.|[Mute alert metrics](../../health-log-analytics-operator/concept/hla-op-alert-significance.md)|Operator|
|Reduce noise by creating log filters.|[Log alert filters](../../health-log-analytics-operator/concept/hla-op-adv-alert-filtering.md)|Operator|
|Influence how Health Log Analytics finds anomalies by managing keywords it looks for in the log data.|[Lexical keywords](hla-log-anomaly-detection.md)|Operator|
|Create alerts for specified metrics by adding, changing, or deleting rules.|[Custom alert rules](hla-alert-rules-manage.md)|Operator|

## What to explore next

-   [Health Log Analytics architecture](hla-architecture.md)
-   [How Health Log Analytics generates alerts](../../health-log-analytics-operator/concept/hla-op-anomalies-detecting.md)

