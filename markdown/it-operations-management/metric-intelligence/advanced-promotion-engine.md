---
title: Advanced Promotion Engine
description: You can create a definition for the Advanced Promotion Engine so that you can define the conditions for promoting the anomaly alerts to the All Alerts table. By promoting the alerts that meet the conditions, only the most relevant anomaly alerts move to the table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/metric-intelligence/advanced-promotion-engine.html
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Advanced Promotion Engine

You can create a definition for the Advanced Promotion Engine so that you can define the conditions for promoting the anomaly alerts to the All Alerts table. By promoting the alerts that meet the conditions, only the most relevant anomaly alerts move to the table.

The Advanced Promotion Engine moves the most relevant anomaly alerts to the All Alerts table. When anomaly alerts on a CI meet the conditions in your definition, the promoted alerts are grouped in the All Alerts table. For example, you can promote only anomaly alerts that belong to a specific CI class with a minimum severity of Major.

The All Alerts table is the table that contains the issues that need your immediate attention. The anomaly alerts on the different metrics within a CI in a specific time period indicate an issue that needs to be promoted to the All Alerts table.

Anomaly alerts indicate a deviation from projected metric values for monitored CIs. For details, see [View anomaly alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/metric-intelligence/view-metrics-anomaly-alerts.md).

The Advanced Promotion Engine is activated automatically as part of the Metric Intelligence application.

You can use the Advanced Promotion Engine definitions that come with the base system \(for the Linux server and for the Windows server\). You can also create definitions on different CI classes. The base system definitions indicate that the CIs on the Linux and Windows servers are operational. CIs with a minimum severity of Major are promoted to the All Alerts table.

All Advanced Promotion Engine tasks require the evt\_mgmt\_admin role. The evt\_mgmt\_user role enables you to view definitions and properties only.

**Parent Topic:**[Exploring Metric Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/metric-intelligence/exploring-metric-intelligence.md)

