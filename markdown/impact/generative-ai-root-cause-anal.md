---
title: Generative AI powered Root cause analysis
description: Root cause analysis in Instance Observer provides automated detection and summarization of issues. It includes built-in root cause correlation and root cause summary using a large language model \(LLM\), which helps reduce troubleshooting time, improve incident transparency, and generative AI driven root cause recommendation by analyzing similar historical incidents.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Generative AI, root cause analysis, Telemetry signals]
breadcrumb: [Overview of Instance Observer, Platform Health, Using Impact, Impact]
---

# Generative AI powered Root cause analysis

Root cause analysis in Instance Observer provides automated detection and summarization of issues. It includes built-in root cause correlation and root cause summary using a large language model \(LLM\), which helps reduce troubleshooting time, improve incident transparency, and generative AI driven root cause recommendation by analyzing similar historical incidents.

**Important:** The Generative AI-powered summarization and recommendation components aren’t available to users in the regulated market. However, the core Root cause correlation \(RCC\) functionality is being offered under the revised name of Root Cause Analysis \(RCA\) to promote product consistency and alignment across all markets.

## Overview of Root Cause Analysis \(RCA\)

RCA automatically identifies and explains the origin of incidents by analyzing multiple telemetry signals. Signals included are related to Memory, Database, Transactions, Cache flush, and Sessions. This analysis enables teams to detect issues faster and resolve them more accurately by correlating relevant anomalies and generating human-readable summaries and recommended resolutions.

## Benefits of RCA

-   Reduced Mean Time To Detect \(MTTD\) or Mean Time To Repair \(MTTR\) through quick signal grouping and summarization.
-   Actionable summaries for faster remediation or automation.
-   Recommended resolutions by analyzing similar historical incidents.

For more information, see [Instance Observer performance insights](io-performance-insights.md).

## Root Cause Correlation \(RCC\)

RCC feature intelligently analyzes logs, metrics, and performance data to identify relationships and dependencies between anomalies automatically. By correlating signals across different performance metrics, it helps you to isolate quickly the origin of an issue with minimal manual effort. This correlation eliminates noise and narrows down the likely root cause from a sea of signals.

## LLM-based Root Cause Summary \(RCS\)

As soon as correlated data are identified, an LLM is invoked to generate a concise, human-readable summary. The LLM processes both structured and unstructured telemetry data to provide clear insights into the likely root cause and affected components.

The transaction with ID XXXXXX for URL/sys\_XXX.do has exceeded the maximum execution time, resulting in a cancellation. The total time taken for this transaction was 0:04:59.044, with processing time of 0:04:59.041 and CPU time of 0:00:07.775. The transaction was initiated by user XXXX. The SQL time was 0:00:50.154, with 4,836 queries executed.

Total processing time of 1095 secs for URL sys\_XXX.do. EXCESSIVE processing time of 0:02:37.194 for ListRecordDefaultTag. Slow silent evaluate for: \_\_ref\_\_.canRead\(\) took 0:00:02.475. A large amount of data has been streamed: 1,048,578 bytes by StreamingBytesSizeHandler. Total processing time of 1095 secs for URL sys\_XXX.do.

## LLM-based Root Cause Recommendation \(RCR\)

Instance Observer provides AI-powered recommended resolutions by analyzing similar historical incidents for the same instance. The system makes reference to case tasks that were successful in the past to resolve comparable issues and suggests them as the most likely remediation steps.

LLM-based RCR also provides:

-   **Personalized guidance**

    Recommendations are tailored to the instance and service based on past resolution history.

-   **Case task linking**

    Direct reference to earlier case tasks ensures that you can review proven fixes rather than starting from scratch.

-   **Human-in-loop validation**

    Recommendations are advisory in nature; operators must validate and apply them according to their standard operating procedures \(SOPs\).


This component reduces trial-and-error in incident response and ensures knowledge reuse across recurring patterns.

Review the query SELECT fcr.u\_XXXX\_approval\_status AS fcr\_u\_w7e\_XXX\_status, taskslatable.time\_left and optimize it by adding indexes or rewriting it for better performance, similar to the solution proposed in Incident ID CSXXXXXX, where indexes were suggested to be added to the tables to improve query performance.

**Note:** RCA is a deterministic model. Therefore, you may not see an RCA report for every alert, or Critical or Warning performance scenario. In cases where the model doesn’t have sufficient or relevant data to generate a result, you can continue to rely on traditional manual analysis.

