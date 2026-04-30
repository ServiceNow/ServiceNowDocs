---
title: View the relationships between source types and log sources
description: Explore the many-to-many relationships between source types and log sources in Health Log Analytics to help you optimize your data input mapping.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, relationship, source type, log source, data input, mapping, parsing, anomalies]
breadcrumb: [Log data auto-mapping and mapping, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# View the relationships between source types and log sources

Explore the many-to-many relationships between source types and log sources in Health Log Analytics to help you optimize your data input mapping.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Health Log Analytics uses source types to parse logs and utilizes log sources as the framework for detecting anomalies. Each source type provides logs that are analyzed by multiple log sources, and each log source receives logs that are parsed by multiple source types. Reviewing the associations between source types and log sources can help you improve your data input mapping for better performance and outcomes.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Mapping** &gt; **Data Input Mapping**.

2.  Ensure that log data is streaming into your instance, and then open a data input mapping record.

3.  View the associations between the log sources and the source types.

    -   View the log sources that are associated with a source type:
        1.  Open the **Source Types** tab to view the generated source type structures.
        2.  Open a source type structure record.
        3.  Select a source type.
        4.  Under **Sources**, view all the log sources that receive data from this source type.
    -   View the source types that are associated with a log source:
        1.  Open the **Sources** tab to view the generated log sources.
        2.  Select a log source record.
        3.  On the **Source Types** tab, view all the source types that feed data into this log source.
    **Note:** The displayed results are updated once a day. Results that are older than 24 hours are deleted automatically.


**Parent Topic:**[Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)

