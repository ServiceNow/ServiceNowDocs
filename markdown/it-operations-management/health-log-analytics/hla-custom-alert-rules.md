---
title: Alert rules in Health Log Analytics
description: Health Log Analytics \(HLA\) detects anomalies automatically by learning from your log data. However, some log types require a custom alert rule to generate alerts reliably.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-custom-alert-rules.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-15"
reading_time_minutes: 2
keywords: [Health Log Analytics, HLA, alert rule, custom alert rules, log analytics alerts, anomaly detection, automatic detection, log patterns, lively logs, sparse logs, stopped logs, probability-based method, high-frequency logs, low-frequency logs, periodic logs, critical conditions, machine learning, not enough data, too little data, pattern]
breadcrumb: [Use custom alert rules, Controlling alert generation, prioritization, and anomaly detection, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Alert rules in Health Log Analytics

Health Log Analytics \(HLA\) detects anomalies automatically by learning from your log data. However, some log types require a custom alert rule to generate alerts reliably.

You can use custom alert rules to specify the metric, threshold, and alert properties for generating alerts that HLA might not detect automatically.

## Anomaly detection logic by log pattern

HLA classifies incoming logs into three patterns before applying anomaly detection. This classification determines which detection logic is used.

<table id="table_nbj_4vy_djc"><thead><tr><th>

Pattern

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lively

</td><td>

Logs arrive frequently and consistently: at least once in 20 seconds. For example, an application writes hundreds of log entries per hour. The ML Engine has enough volume to build a reliable baseline, so it applies standard anomaly scoring to detect deviations.

</td></tr><tr><td>

Sparse

</td><td>

Logs arrive infrequently or irregularly: less than once in 1 minute \(60 seconds\). For example, a batch job runs every night and writes a small number of log entries. Standard anomaly scoring would produce unreliable results here, so the ML Engine applies probability distribution analysis instead. Sparse logs might not generate alerts if the volume is too low to establish a baseline.

</td></tr><tr><td>

Stopped

</td><td>

Logs have not arrived for more than the configured period. Default is 5 minutes \(300 seconds\). To modify the default value, update the HLA system property `detective.resolution.signal_dead`.For a log stream to be alerted as stopped or dead it must first be considered alive by running continuously for a minimum period of time. You can set this time in the HLA system property `detective.alive_period_seconds_for_signal_dead`.

For information about setting and changing HLA system properties, see [Configure global Health Log Analytics system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-system-properties-configure.md).

</td></tr></tbody>
</table>## When to create custom alert rules

-   For high-frequency logs with a lively log pattern, there is no need for a custom rule. However, you can add a rule to generate alerts under specific conditions.
-   For low-frequency logs with a sparse log pattern, the system might not generate alerts automatically. If these logs should still generate alerts, define a custom alert rule.
-   For known critical conditions that HLA might not flag automatically, define a custom rule. For example, if a specific log message indicates that a critical service has failed, define a rule that generates an alert every time that message appears.

|Scenario|ML detection|Custom rule|
|--------|------------|-----------|
|High-frequency logs with a lively log pattern|Likely sufficient|Optional|
|Low-frequency or periodic logs|Unreliable|Suggested|
|Known critical conditions|Insufficient|Required|

**Related topics**  


[Define a custom Log Analytics alert rule in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-alert-rule-add-sow.md)

[Change a custom Log Analytics alert rule in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-defined-alert-modify-sow.md)

[Delete a custom Log Analytics alert rule in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-defined-alert-delete-sow.md)

