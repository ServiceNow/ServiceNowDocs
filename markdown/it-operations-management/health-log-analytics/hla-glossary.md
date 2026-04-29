---
title: Health Log Analytics terminology
description: Before getting started with Health Log Analytics, it's important to familiarize yourself with some key concepts used in the application.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [ServiceNow, Health Log Analytics, HLA, terminology, glossary, terms]
breadcrumb: [Exploring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics terminology

Before getting started with Health Log Analytics, it's important to familiarize yourself with some key concepts used in the application.

<table><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alert

</td><td>

A notification that HLA generates when it finds a statistically significant anomaly in metrics based on your system's log data, indicating a potential IT issue. HLA sends these alerts to Event Management, where you can see them in the **All Alerts** list.

</td></tr><tr><td>

Anomaly

</td><td>

Unusual or unexpected behavior in log data that differs from the baseline of normal behavior that HLA has learned from historical patterns.

</td></tr><tr><td>

Baseline

</td><td>

The statistical model of normal behavior of your system that HLA has learned from historical log data patterns. This baseline helps HLA identify anomalies.

</td></tr><tr><td>

Classification

</td><td>

A data type that determines how the HLA engine analyzes and processes a parsed log field. Available classifications are: Meter, Gauge, Histogram, Automatic Root Cause \(ARC Only\), Timeless Gauge, and Invalid.

</td></tr><tr><td id="hla-glossary-component">

Component

</td><td>

Representation of the smallest part of a [service instance](hla-glossary.md#hla-glossary-service-instance), typically a single micro service, module, or daemon. For example, a "checkout flow" service instance may include components such as cart-service, payment-service, and inventory-service. Every log or metric is assigned to a single component. This ensures that anomalies or incidents are attributed to that specific component.

</td></tr><tr><td>

Configuration Item \(CI\)

</td><td>

An individual item in your IT environment, such as a server, database, or application, that is tracked and managed in the Configuration Management Database \(CMDB\).

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

The central database in ServiceNow that stores and manages information about all CIs and their relationships. This database provides HLA with the necessary context to correlate logs, anomalies, and alerts to specific services.

</td></tr><tr><td>

Correlation

</td><td>

The process of connecting related log events, anomalies, and alerts. By using factors like patterns and relationships defined in the CMDB service relationships, HLA identifies a shared root cause and reduces "noise."

</td></tr><tr><td id="hla-glossary-data-input">

Data input

</td><td>

A configurable connector that enables HLA to collect, transform, and ingest log data from external sources. **Note:** The term data input is used in HLA's classic interface \(UI16\) and back-end records. See also: [Integration](hla-glossary.md#hla-glossary-integration).

</td></tr><tr><td id="hla-glossary-data-input-mapping">

Data input mapping

</td><td>

The process of mapping raw log data to its specific log source, enabling HLA to connect logs to the corresponding service instance and component for analysis with full context. It also involves mapping your raw log data to source types so HLA can understand the format and structure of your logs.**Note:** The term data input is used in HLA's classic interface \(UI16\) and back-end records. See also: [Integration](hla-glossary.md#hla-glossary-integration).

For a description of the simplified mapping interface in the new HLA UI, see: [Log context mapping](hla-glossary.md#hla-glossary-log-context-mapping).

</td></tr><tr><td>

Detection algorithm

</td><td>

The statistical or machine-learning logic that HLA uses to analyze metrics and patterns to identify anomalous behavior. Examples include sigma-based detection, trend analysis, and comparing against a baseline.

</td></tr><tr><td>

Enrichment

</td><td>

The process of adding extra, contextual information to raw log data to make it more meaningful and actionable for analysis. Enrichment helps HLA connect technical events to their potential impact on your business.

</td></tr><tr><td>

Grouped alerts

</td><td>

A collection of related alerts that are combined into a single group to reduce noise and simplify triage.

</td></tr><tr><td>

Incident

</td><td>

A record created in ServiceNow when correlated alerts point to a significant disruption in a service, requiring investigation and resolution.

</td></tr><tr><td id="hla-glossary-integration">

Integration

</td><td>

A configurable connector that establishes data pipelines so HLA can collect, transform, and ingest log data from external sources. Setup of integrations is done through the Integrations Launchpad, which significantly reduces implementation time compared to manual data input setup.**Note:** The term integration is used in HLA's new UI experience and front-end records. See also: [Data input](hla-glossary.md#hla-glossary-data-input).

</td></tr><tr><td>

Integrations Launchpad

</td><td>

A framework that provides integration setup workflows for connecting external log data sources to HLA.Setting up integrations through the Integrations Launchpad significantly reduces implementation time compared to manual data input setup.

</td></tr><tr><td>

Label

</td><td>

A semantic identifier assigned to common log properties, such as MESSAGE, HOST, TIMESTAMP, SEVERITY, and EVENT-ID. Labels tell HLA what role a parsed log field plays in the log structure.

</td></tr><tr><td>

Lexical keywords

</td><td>

Specific words found in log data, such as "crashed" or "failed," that can point to important issues. HLA tracks lexical keywords to detect widespread issues and long-forming trends. For more information, see: [Add, edit, or delete lexical keywords in Health Log Analytics](../task/hla-lexical-keywords-admin.md).

</td></tr><tr><td id="hla-glossary-log-context-mapping">

Log context mapping

</td><td>

The process of mapping your raw log data to the appropriate log source, enabling HLA to connect logs to their corresponding service instance and component for contextualized analysis.The user-friendly Log context mapping interface in the new HLA UI focuses only on the service context. It's simpler to use than Data input mapping in HLA's classic interface \(UI16\), which also includes source type configuration. See also: [Data input mapping](hla-glossary.md#hla-glossary-data-input-mapping).

</td></tr><tr><td>

Log ingestion

</td><td>

The process of streaming of logs from servers and endpoints or log repositories to HLA, using data input connectors or integrations.

</td></tr><tr><td>

Log property

</td><td>

A structured data element, such as timestamp, severity, or error code, that is extracted from a log entry.

</td></tr><tr><td>

Log source

</td><td>

A logical representation of the source of the log data that HLA ingests. Each log source is defined by a [service instance](hla-glossary.md#hla-glossary-service-instance)-[component](hla-glossary.md#hla-glossary-component) pair. HLA performs anomaly detection and generates alerts on issues within the scope of each individual log source.

</td></tr><tr><td>

Log Viewer

</td><td>

An interface within HLA that allows you to search, filter, and examine raw or parsed log data from multiple sources. The Log Viewer helps you investigate events and better understand your system's behavior.

</td></tr><tr><td>

Metric

</td><td>

A quantifiable measurement extracted from log data in HLA. HLA supports various generic metric types, such as METER \(event count\), GAUGE \(numeric value\), and HISTOGRAM \(distribution bucket\). It uses the extracted log data to automatically create message-pattern-based metrics \(METER\), severity metrics \(METER\), keyword metrics \(METER\), and raw log metrics \(METER, GAUGE, and HISTOGRAM\). Each metric is associated with a specific log source and monitored for anomalous behavior.

</td></tr><tr><td>

MID Server

</td><td>

An intermediary agent that facilitates secure communication between on-premise or private cloud log sources and the ServiceNow instance. It enables HLA to collect log data securely from environments that the instance can't access directly.

</td></tr><tr><td>

Parsing

</td><td>

The process of extracting meaningful, structured data fields from raw log entries. HLA uses its AutoParser and AutoExtraction capabilities to parse the logs, which then enables effective analysis, correlation, and visualization of the data.

</td></tr><tr><td>

Pattern

</td><td>

A recurring format found in log messages \(free text fields within log records\). HLA groups similar log messages that share this format into a pattern. It then monitors how often that pattern occurs to establish normal system behavior and detect anomalies.**Note:** HLA only performs pattern monitoring and anomaly detection on log properties labeled as MESSAGE.

</td></tr><tr><td>

Raw log data

</td><td>

The original, unprocessed log entries collected from external sources, which HLA ingests before parsing and analysis.

</td></tr><tr><td>

Root Cause Analysis \(RCA\)

</td><td>

An automated analysis that identifies meaningful factors, entities, and highlights that contributed to an alert or incident, helping to identify the underlying cause.

</td></tr><tr><td id="hla-glossary-service-instance">

Service instance \(formerly application service\)

</td><td>

A logical grouping of Configuration Items \(CIs\), such as servers, databases, and applications, that collectively deliver a complete business service. In HLA, log data is correlated to service instances to provide a comprehensive, real-time view of their operational health and performance. **Note:** A single service instance can consist of multiple CIs, whereas the same CIs might be part of multiple service instances.

</td></tr><tr><td>

Severity

</td><td>

A classification in HLA that indicates the level of impact or urgency of an alert. This helps operators prioritize which issues to investigate and resolve first.

</td></tr><tr><td>

Source type

</td><td>

A configuration profile for a log data type that determines how HLA interprets, parses, and extracts fields from logs of that format and prepares the data for processing. Think of it as telling HLA: "Here’s a specific type of log, and here’s how you should process it."

</td></tr><tr><td>

Source type structure

</td><td>

A template within a Source Type that defines the fields and their arrangement in logs of that specific type. The Source type structure ensures that HLA can consistently extract and understand the incoming data. Think of it as telling HLA: "This part of this log is the timestamp." "This part is the severity." "This part is the error code," and so on.

</td></tr><tr><td>

Tag

</td><td>

Metadata applied to logs, metrics, or alerts. Tags are used for categorization, filtering, and correlation.

</td></tr><tr><td>

Time series

</td><td>

A sequence of metric values recorded in chronological order over a period of time. This data is used to identify trends, seasonality, and anomalies.

</td></tr><tr><td>

Variable extraction

</td><td>

The process of identifying and extracting dynamic, user-defined fields from log messages to enable custom metrics and analytics in HLA.

</td></tr></tbody>
</table>