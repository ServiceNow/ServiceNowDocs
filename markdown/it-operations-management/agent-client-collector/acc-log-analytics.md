---
title: Agent Client Collector Log Analytics
description: Agent Client Collector Log Analytics \(ACC-L\) enables you to stream log data from Linux and Windows hosts to a ServiceNow instance, using the Agent Client Collector.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Log Analytics

Agent Client Collector Log Analytics \(ACC-L\) enables you to stream log data from Linux and Windows hosts to a ServiceNow instance, using the Agent Client Collector.

As with Agent Client Collector Framework \(ACC-F\), the Agent Client Collector connects to a MID Server. A single MID Server may support multiple agents, while a single agent works with one MID Server at a time and switches to a different MID Server when necessary to provide failover protection.

Use the Agent Client Collector to stream log data to your ServiceNow® instance by means of a log shipper. The log data is mapped and structured in the ServiceNow® Health Log Analytics application. For more information, see the [Health Log Analytics](../../health-log-analytics-admin/reference/hla-landing-page.md) product documentation.

Agent Client Collector Log Analytics has a dependency on the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Streaming log data from Windows hosts is supported in Agent Client Collector Log Analytics Version 3.1.0 and later.

The Agent Client Collector Log Analytics \(ACC-L\) application, Version 3.2.0, August 2022, has a dependency on the Agent Client Collector Framework \(ACC-F\) application, Version 2.10.1, August 2022.

To enable Agent Client Collector Log Analytics, you enable log analytics on the Agent Client Collector, as described in [Set up Agent Client Collector Log Analytics without using guided setup](../task/acc-enable-hla.md).

## Dependencies

For a list of Agent Client Collector Log Analytics plugin dependencies, see [Plugins or applications installed with ITOM AIOps](../../it-operations-management/reference/plugin-app-itom-health.md).

