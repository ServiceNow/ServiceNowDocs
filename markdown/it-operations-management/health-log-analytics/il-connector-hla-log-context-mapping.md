---
title: Mapping logs for contextual alerts in Health Log Analytics
description: Map your logs to service instances, components, and source types so that Health Log Analytics can generate alerts in context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/il-connector-hla-log-context-mapping.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [integration, mapping, ServiceNow Otto, automatic, log context, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Mapping logs for contextual alerts in Health Log Analytics

Map your logs to service instances, components, and source types so that Health Log Analytics can generate alerts in context.

Mapping your log data to the correct context is especially important when the integration processes logs from multiple service instances and components. ServiceNow Otto suggests the best log field for mapping to service instances and components. When you use the AI-suggested field, or when that field is the default, an AI sparkle icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text:\) appears. You can select a different field if needed. If the AI agent can't find a suitable match, HLA uses the system default. The system default also applies if the selected field is not present in the sample log.

For a walkthrough of how to set up and review AI-suggested mappings, see [AI-assisted log mapping in Health Log Analytics](https://player.vimeo.com/video/1204161467?h=bf31a8c144&badge=0&autopause=0&player_id=0&app_id=58479).

## Example

A large financial institution might face performance issues with its e-banking application, which relies on various components like web, application, and database servers. Without log context mapping, logs from these components appear isolated, making it difficult to correlate issues. An anomaly in a Tomcat server log might be detected, but without proper context, the operator struggles to assess its impact. Log context mapping enables you to define rules to map logs to the e-banking application service instance and the Tomcat server component. This mapping provides a contextualized view for root cause analysis and resolution.

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-implement.md)

