---
title: Generative AI powered root cause analysis
description: Root cause analysis in Instance Observer provides automated detection and summarization of issues. It includes built-in root cause correlation and root cause summary using a large language model \(LLM\), which helps reduce troubleshooting time and improve incident transparency.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Generative AI, root cause analysis, Telemetry signals]
breadcrumb: [Root Cause Correlation, Alerts in Instance Observer, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Generative AI powered root cause analysis

Root cause analysis in Instance Observer provides automated detection and summarization of issues. It includes built-in root cause correlation and root cause summary using a large language model \(LLM\), which helps reduce troubleshooting time and improve incident transparency.

## Overview of root cause analysis

Root cause analysis \(RCA\) automatically identifies and explains the origin of incidents by analyzing multiple telemetry signals. Signals included are related to Memory, Database, Transactions, Cache flush, and Sessions. This analysis enables teams to detect issues faster and resolve them more accurately by correlating relevant anomalies and generating human-readable summaries.

## Benefits of root cause analysis

-   Reduced Mean Time To Detect \(MTTD\) or Mean Time To Repair \(MTTR\) through quick signal grouping and summarization.
-   Actionable summaries for faster remediation or automation.

## Root cause correlation

Root cause correlation feature intelligently analyzes logs, metrics, and performance data to identify automatically relationships and dependencies between anomalies. By correlating signals across different performance metrics, it helps you to quickly isolate the origin of an issue with minimal manual effort. This correlation eliminates noise and narrows down the likely root cause from a sea of signals.

## LLM-based root cause summary

As soon as correlated data are identified, an LLM is invoked to generate a concise, human-readable summary. The LLM processes both structured and unstructured telemetry data to provide clear insights into the likely root cause and affected components.

The transaction with ID XXXXXX for URL/sys\_XXX.do has exceeded the maximum execution time, resulting in a cancellation. The total time taken for this transaction was 0:04:59.044, with processing time of 0:04:59.041 and CPU time of 0:00:07.775. The transaction was initiated by user XXXX. The SQL time was 0:00:50.154, with 4,836 queries executed.

Total processing time of 1095 secs for URL sys\_XXX.do. EXCESSIVE processing time of 0:02:37.194 for ListRecordDefaultTag. Slow silent evaluate for: \_\_ref\_\_.canRead\(\) took 0:00:02.475. A large amount of data has been streamed: 1,048,578 bytes by StreamingBytesSizeHandler. Total processing time of 1095 secs for URL sys\_XXX.do.

