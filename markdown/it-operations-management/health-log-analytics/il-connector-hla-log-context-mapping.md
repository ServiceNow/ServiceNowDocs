---
title: Mapping logs for contextual alerts in Health Log Analytics
description: Map your logs to service instances, components, and source types so that Health Log Analytics \(HLA\) can generate alerts in context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-01-08"
reading_time_minutes: 1
keywords: [integration, mapping, automatic, log context, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Mapping logs for contextual alerts in Health Log Analytics

Map your logs to service instances, components, and source types so that Health Log Analytics \(HLA\) can generate alerts in context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.

The AI agent suggests the optimal log field for mapping to service instances and components. When you use the AI-suggested field, or when that field is the default, an AI sparkle icon \(![](../../../common/image/icon-ai-sparkle.png)\) appears. You can select a different field if needed. If the AI agent cannot find an optimal match, HLA uses the system default. The system default also applies if the selected field is not present in the sample log.

## Example

A large financial institution might face performance issues with its e-banking application, which relies on various components like web, application, and database servers. Without log context mapping, logs from these components appear isolated, complicating issue correlation. An anomaly in a Tomcat server log might be detected, but without proper context, the operator struggles to assess its impact. Log context mapping enables defining rules to map logs to the e-banking application service instance and the Tomcat server component. This mapping provides a contextualized view for root cause analysis and resolution.

**Parent Topic:**[Setting up Health Log Analytics on your ServiceNow instance](hla-implement.md)

