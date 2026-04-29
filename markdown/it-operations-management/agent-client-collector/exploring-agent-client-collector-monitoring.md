---
title: Exploring Agent Client Collector Monitoring
description: Agent Client Collector Monitoring is built on a Sensu framework which enables you to adopt and extend monitoring checks from the community. Agent Client Collector Monitoring collects data on your company’s infrastructure and installed applications.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Exploring Agent Client Collector Monitoring

Agent Client Collector Monitoring is built on a Sensu framework which enables you to adopt and extend monitoring checks from the community. Agent Client Collector Monitoring collects data on your company’s infrastructure and installed applications.

## Agent Client Collector Monitoring overview

Checks and policies run on the agent’s client to retrieve the relevant data, which is transformed into events or metrics, as appropriate. Events and metrics are sent from the agent to your ServiceNow instance through a Metric Intelligence MID Server and are stored in the relevant database. A single MID Server can support multiple agents \(such as ACC-M and ACC-L\). For details on configuring the MID Server for Metric Intelligence, see [MID Server and MID Server distributed cluster for Metric Intelligence](../../event-management/concept/ops-intelligence-mid-server.md).

Agent Client Collector Monitoring comes with the Event Management plugin and also requires installing the request Metricbase \(Clotho DB\), as described in [How to request Metricbase \(Clotho DB\) configuration \(KB0816088\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0816088).

For details on the plugins installed with Agent Client Collector Monitoring, see [Plugins or applications installed with ITOM AIOps](../../it-operations-management/reference/plugin-app-itom-health.md).

## Agent Client Collector Monitoring workflow

The following illustration describes the layout and data flow within the Agent Client Collector Monitoring application.

![ACC-M Infographic](../image/acc-m-infographic.png "Monitoring service health and availability with ACC-M")

## Agent Client Collector Monitoring benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Monitor logs which track events occurring in a Windows environment|[Windows event log monitoring](windows-event-log-monitoring.md)|Agent Client Collector administrator|
|Monitor operating systems and applications|[Operating system and application monitoring using Agent Client Collector](itom-monitoring-for-acc.md)|Agent Client Collector administrator|
|Gather metrics on host data|[Metric Intelligence](operational-metrics.md)|Agent Client Collector administrator|

