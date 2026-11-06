---
title: Agent Client Collector Monitoring system properties
description: Lists the Agent Client Collector Monitoring system properties that control monitoring behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/acc-monitoring-system-properties.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-10-12"
reading_time_minutes: 1
keywords: [system properties, sn\_itmon, proxy agent]
breadcrumb: [ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Monitoring system properties

Lists the Agent Client Collector Monitoring system properties that control monitoring behavior.

<table id="table_ep5_fwk_wkc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`sn_itmon.enable_auto_alert_closing`

</td><td>

Enables auto-closing of alerts when they are no longer monitored by a policy or check.Type: String

Default: true

</td></tr><tr><td>

`sn_itmon.increased_threshold_for_proxy_agent`

</td><td>

Specifies how many additional checks a proxy agent can run beyond the limit for a non-proxy agent.Type: Integer

Default: 30

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-monitoring-reference.md)

