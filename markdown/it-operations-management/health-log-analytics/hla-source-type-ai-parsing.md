---
title: Parse log data automatically and review parsing suggestions
description: Parse log data automatically in Health Log Analytics using AI-assisted log parsing. ServiceNow Otto for ITOM generates a parser for each detected log format and displays suggested classifications and labels for the parsed properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/health-log-analytics/hla-source-type-ai-parsing.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-10-04"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, AI parser, AI-assisted log parsing, source type structure, classification, labels, streaming]
breadcrumb: [Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Parse log data automatically and review parsing suggestions

Parse log data automatically in Health Log Analytics using AI-assisted log parsing. ServiceNow Otto for ITOM generates a parser for each detected log format and displays suggested classifications and labels for the parsed properties.

## Before you begin

**Important:** To enable AI-powered automatic parsing and mapping of log data, the integration must be activated with AI.

Role required: evt\_mgmt\_admin

## About this task

AI-assisted log parsing parses incoming logs in real time, including high-volume streaming log data. ServiceNow Otto for ITOM detects each new log format and generates a parser for that format automatically. Verify that the log properties are classified and labeled correctly. You can override an AI-generated suggestion by selecting a different value from the list.

## Procedure

1.  If your integration is inactive, activate it with AI-powered capabilities by selecting **Activate with AI**.

    This option turns on AI-powered automatic parsing and mapping of log data. When the integration is activated, ServiceNow Otto for ITOM collects and analyzes your log data. The AI icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: indicates that AI is active.

    **Note:** Mapping starts only after the AI parser has generated a parser for your log format. After the first logs stream in, the system waits for the parser for up to 7 minutes by default. If the parser isn't ready by then, the system stops waiting.

2.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Inputs** &gt; **Source Type Structure**.

3.  Open the record for your source type.

4.  Review the extracted key/value mapping in the **Automated Parser Outcome** related list on the **Data Input Mapping** page.

    This related list shows the key/value mapping that the AI parser extracted from your log data.

5.  On the **Key/Value Mapping** tab of the **Source Type Structure** page, verify that the **Extraction type** column shows AI Parser.

6.  Verify that the log properties are classified and labeled correctly.

7.  Override an AI-generated suggestion by selecting a different value from the list in the **Classification** or **Labels to assign** column.


**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/health-log-analytics/hla-implement.md)

**Related topics**  


[Refine the source type structure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/health-log-analytics/hla-source-type-structure-refine.md)

