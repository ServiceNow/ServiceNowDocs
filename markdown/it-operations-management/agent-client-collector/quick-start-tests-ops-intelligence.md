---
title: Quick start tests for Metric Intelligence
description: Validate that Metric Intelligence still works after you make any configuration change such as apply an upgrade or develop an application. Copy and configure these quick start tests to pass when using your instance-specific data.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring reference, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Quick start tests for Metric Intelligence

Validate that Metric Intelligence still works after you make any configuration change such as apply an upgrade or develop an application. Copy and configure these quick start tests to pass when using your instance-specific data.

Metric Intelligence quick start tests require activating the Metric Intelligence plugin \(com.snc.sa.metric\).

<table id="table_usl_4wy_vfb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

OI: Health Metrics Collection

</td><td>

An individual test that verifies the following:

-   There is at least one Metric Intelligence Metrics extension that is running.
-   There are entries for the ‘Health Metrics’ in the Metric to CI table.
-   For each of the Metric Intelligence Metrics extensions that are currently running, that there is data stored in MetricBase.

 If the test initially fails, wait until the Metric Intelligence Metrics extension runs for at least 10-15 minutes. Then try again.

</td><td>

Madrid

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Monitoring reference](../../../product/agent-client-collector/reference/acc-monitoring-reference.md)

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

