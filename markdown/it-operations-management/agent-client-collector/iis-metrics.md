---
title: Internet Information Services \(IIS\) metrics
description: The following table lists the metrics that are gathered as output from IIS checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC-M default checks and policies, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# Internet Information Services \(IIS\) metrics

The following table lists the metrics that are gathered as output from IIS checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Resource \(name of specific database, where relevant\)|Units|Metric type description|
|-----------|------------------------------------------------------|-----|-----------------------|
|iis.\_Total.Web\_Service\(\_Total\).Current\_Connections \(featured metric\)| |count|Total number of current connections to IIS.|
|iis.\_Total.Web\_Service\(\_Total\).Total\_Get\_Requests \(featured metric\)| |count|Total of HTTP GET requests received by the IIS server.|
|iis.\_Total.Web\_Service\(\_Total\).Total\_Post\_Requests \(featured metric\)| |count|Total of HTTP POST requests received by the IIS server.|
|iis.\_Total.Web\_Service\(\_Total\).Get\_Requests/sec \(featured metric\)| |count per second|Rate of all HTTP GET requests received by the IIS server.|
|iis.\_Total.Web\_Service\(\_Total\).Post\_Requests/sec \(featured metric\)| |count per second|Rate of all HTTP POST requests received by the IIS server.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

