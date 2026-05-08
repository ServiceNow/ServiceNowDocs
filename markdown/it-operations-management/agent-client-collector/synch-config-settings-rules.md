---
title: Synchronize configuration settings rules
description: Metric Intelligence configuration settings rules contain user specified values that override default values that currently exist on Metric Intelligence MID Servers. To take effect, the Metric Intelligence MID Servers must be synchronized with the updated set of configuration settings rules.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Create a configuration settings rule, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Synchronize configuration settings rules

Metric Intelligence configuration settings rules contain user specified values that override default values that currently exist on Metric Intelligence MID Servers. To take effect, the Metric Intelligence MID Servers must be synchronized with the updated set of configuration settings rules.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can manually initiate a synchronization to immediately apply the updates on all Metric Intelligence MID Servers. Or, you can rely on a system job, that runs on an hourly recurring schedule, checking for updates to the metric configuration rules. If it is determined that there are updates, the system job sends these updates to the Metric Intelligence MID Servers.

## Procedure

1.  Navigate to **All** &gt; **Event Management Rules** &gt; **Anomaly Detection** &gt; **Metric Config Rules**.

2.  On the Metric Configuration Rules pane, click **Sync to MID**.


## What to do next

Verify that all Metric Intelligence MID Servers have been synchronized with the updated set of configuration settings rules:

1.  Navigate to **Output and Artifacts** &gt; **ECC Queue**.
2.  In the **Queues** pane, search the **Topics** column for `MetricConfigProbe`.
3.  Check the **Agent** column and verify that all MID Servers are updated.

**Parent Topic:**[Create a configuration settings rule](create-config-overriding-rule.md)

