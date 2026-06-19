---
title: MS Exchange default checks and policies
description: Agent Client Collector provides the following default checks and policies for MS Exchange monitoring.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/msexchange-checks-policies.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# MS Exchange default checks and policies

Agent Client Collector provides the following default checks and policies for MS Exchange monitoring.

<table id="table_gcb_fw2_v5b"><thead><tr><th>

Type

</th><th>

Check

</th><th>

Description

</th><th>

Usage and usage example

</th><th>

Output

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

app.msexchange.metrics-msexchange

</td><td>

Returns Microsoft Exchange metrics.

</td><td>

```
winchecks metric-msexchange (options)
-s scheme Replaces the host name with this parameter
```

 Usage example: `winchecks metric-msexchange {{if .labels.params_scheme}} -s {{if .labels.params_scheme}} {{end}}`

</td><td>

Metrics from MS Exchange server

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/agent-policies-checks.md)

