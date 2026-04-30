---
title: Self-health monitoring for Metric Intelligence
description: Use Event Management self-health monitors to monitor the health of Metric Intelligence infrastructure components and processes, and to alert about potential issues. Self-health monitoring allows you to proactively remediate issues and minimize data loss.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Self-health monitoring for Metric Intelligence

Use Event Management self-health monitors to monitor the health of Metric Intelligence infrastructure components and processes, and to alert about potential issues. Self-health monitoring allows you to proactively remediate issues and minimize data loss.

Metric Intelligence is pre-configured to use Event Management self-health monitors to ensure that essential components and processes are functioning properly. If a monitor detects a failure, then the Event Management self-health monitoring system creates an event for the issue. These events are then converted into an Event Management alert or get appended to a previous alert. Metric Intelligence self-health monitors run every 60 seconds.

For example, if an Metric Intelligence MID Server distributed cluster experiences an issue, an event is generated with the status of **Major**. Then, this event is converted into an alert. Later, when the issue is resolved, a new event is generated with the status of **Info** and the original alert is closed.

## Monitored components and processes

<table id="table_vhc_ltm_kfb"><thead><tr><th>

Component/Process Check

</th><th>

Error Condition

</th></tr></thead><tbody><tr><td>

Metric Intelligence extension is running properly

</td><td>

Monitor checks the **status** field of the **ecc\_agent\_ext\_context\_metric** table to detect a state of **Error** or **Warning**.

</td></tr><tr><td>

Metric Intelligence MID Server distributed cluster is running properly

</td><td>

Monitor checks the **status** field of the **ecc\_agent\_cluster** table to detect a state of **Error**, **Segmented**, or**Stopped**. **Note:** For a state of **Stopped**, an event is created only if the **error\_message** field is not empty.

</td></tr><tr><td>

Metrics are collected by active connectors that are configured for metrics collection

</td><td>

For each connector with the **Metrics collection** flag set to **true**: Monitor checks the status of the **last\_kpi\_status** field in the **em\_connector\_instance** table to detect a status of **Error**.

</td></tr><tr><td>

Essential Metric Intelligence scheduled jobs are active

</td><td>

Monitor checks the following essential scheduled jobs, to detect if any is inactive:-   Metric Intelligence — Metric configuration job
-   Metric Intelligence — Sync tables with mid
-   Metric Intelligence — Validate MID Distributed cluster

</td></tr></tbody>
</table>For more information about enabling or disabling an Metric Intelligence self-health monitor, see [Configure a self-health monitor](../task/configure-threshold-monitoring.md).

**Parent Topic:**[Metric Intelligence](operational-metrics.md)

**Related topics**  


[Self-health monitors for Event Management](self-monitoring.md)

[Scheduled jobs installed with Metric Intelligence](../reference/installed-with-metrics.md)

