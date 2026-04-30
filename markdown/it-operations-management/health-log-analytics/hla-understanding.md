---
title: Understanding ServiceNow Health Log Analytics \(HLA\)
description: Health Log Analytics predicts IT issues before they affect your users. The application helps you solve problems faster by collecting, understanding, and correlating machine-generated log data in real time. It discovers any deviation from normal behavior as it happens and alerts you of possible issues.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [Health Log Analytics, HLA, overview, introduction, architecture, workflow, log data, data input connectors, data sources, ingestion, anomalies]
breadcrumb: [Exploring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Understanding ServiceNow Health Log Analytics \(HLA\)

Health Log Analytics predicts IT issues before they affect your users. The application helps you solve problems faster by collecting, understanding, and correlating machine-generated log data in real time. It discovers any deviation from normal behavior as it happens and alerts you of possible issues.

Health Log Analytics receives and processes logs via the MID Server and sends events to the ServiceNow Event Management application.

## Data that Health Log Analytics can process

Health Log Analytics can handle any kind of machine-generated textual log data. It can process application, infrastructure, and network logs, as well as other types of textual log data. Although a configuration management database \(CMDB\) can be helpful to generate high-quality events and alerts, it is not necessary.

**Note:**

-   Health Log Analytics supports only UTF-8 logs. The application does not support binary logs.
-   If you are sending logs in a language other than English, additional configuration may be required..

## Architecture

Health Log Analytics collects logs streaming into your ServiceNow instance from endpoints or data lakes, such as Splunk and Elasticsearch. The instance receives the logs via the [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) connector instance. Health Log Analytics identifies and triages anomalies in your log data using unsupervised machine-learning \(ML\) models. It then groups the anomalies together and applies further algorithms to help identify the root cause of the issue.

The following figure shows a setup using Rsyslog, Splunk, Filebeat, and Elasticsearch.

![Health Log Analytics architecture.](../image/hla-architecture-img.png "Health Log Analytics architecture")

## Workflow

Health Log Analytics collects and processes log data automatically. It structures the data logically for operators to analyze, and generates meaningful alerts and suggestions that display in Event Management.

The diagram shows the Health Log Analytics workflow from collecting the data through sending an event or alert to Event Management.

![Health Log Analytics workflow: Ingestion - Structuring - Enrichment - Analysis - ML & AI - Alert in Event Management](../image/hla-workflow-img.png "Health Log Analytics workflow")

-   **Ingestion**

    This layer connects your environment to Health Log Analytics. You can stream your logs directly from servers and endpoints or from log repositories. The optional guided setup helps you create data input connectors for the following common data sources:

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


**Parent Topic:**[Exploring Health Log Analytics](hla-exploring.md)

