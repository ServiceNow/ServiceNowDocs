---
title: About Log Analytics alert rules
description: Health Log Analytics \(HLA\) detects anomalies automatically by learning from your log data. However, automatic detection doesn’t work equally well for all log types. Some logs need a custom alert rule to generate alerts reliably.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-15"
reading_time_minutes: 2
keywords: [Health Log Analytics, HLA, alert rule, custom alert rules, log analytics alerts, anomaly detection, automatic detection, log patterns, lively logs, sparse logs, stopped logs, probability-based method, high-frequency logs, low-frequency logs, periodic logs, critical conditions, machine learning, too little data, pattern]
breadcrumb: [Use alert rules to control when HLA generates alerts, Controlling alert generation, prioritization, and anomaly detection, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# About Log Analytics alert rules

Health Log Analytics \(HLA\) detects anomalies automatically by learning from your log data. However, automatic detection doesn’t work equally well for all log types. Some logs need a custom alert rule to generate alerts reliably.

HLA sorts incoming log patterns into three groups: Lively, sparse, and stopped. It uses different detection logic for each group. Infrequent logs are treated as sparse. For sparse logs, HLA uses a probability-based method instead of standard anomaly scoring. It does so by design: Using standard scoring on a log that shows up only now and then would give unreliable results. However, as a result, logs with too little data might not generate alerts, because the HLA engine doesn’t have enough to establish a normal pattern.

## When to use a custom alert rule

Use a custom alert rule when your log data isn’t generating alerts automatically.

|Scenario|ML detection|Custom rule|
|--------|------------|-----------|
|High-frequency logs with changing patterns|Sufficient|Optional|
|Low-frequency or periodic logs|Unreliable|Suggested|
|Known critical conditions|Not applicable|Required|

## Examples

The following examples show how the type of log data determines whether a custom alert rule is needed.

-   High-frequency logs: An application writes hundreds of log entries per hour. HLA builds a reliable pattern quickly and alerts when behavior changes. A custom rule isn’t required, but you may add one to alert on a specific condition.
-   Infrequent logs: A batch job runs every night and writes a small number of log entries. HLA can’t build a reliable pattern from so little data. Define a custom rule to verify alerts are generated when the job fails or behaves unexpectedly.
-   Known critical conditions: A specific error code must never appear in your logs. HLA might not flag it automatically. Define a custom rule that generates an alert every time that error code appears.

**Related topics**  


[Define a Log Analytics alert rule in Health Log Analytics](../../health-log-analytics-operator/task/hla-op-alert-rule-add-sow.md)

[Change a Log Analytics alert rule in Health Log Analytics](../../health-log-analytics-operator/task/hla-op-defined-alert-modify-sow.md)

[Delete a Log Analytics alert rule in Health Log Analytics](../../health-log-analytics-operator/task/hla-op-defined-alert-delete-sow.md)

