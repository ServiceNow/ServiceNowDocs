---
title: Limit metrics collection and evaluation
description: You can limit the metrics you send from the MID Server to the instance, either by de-activating a specific CI or an entire CI type.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enable metrics collection and evaluation, Configuring Agent Client Collector Monitoring, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Limit metrics collection and evaluation

You can limit the metrics you send from the MID Server to the instance, either by de-activating a specific CI or an entire CI type.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  To limit metrics collection and evaluation for specific CIs:

    1.  Navigate to **Event Management** &gt; **Anomaly Detection** &gt; **Metric to CI**.

        The **Metric to CI Mappings** page appears.

        ![Metric to CI Mappings page](../image/metric-to-ci-mappings.png "Metric to CI Mappings")

        **Note:** The Metric to CI Mapping is identified by both its metric identifier and its configuration item.

    2.  To prevent sending metrics for a specific metric and CI, set the value of the **Active** column to **false**.

2.  To limit metrics collection and evaluation for an entire CI type:

    1.  Navigate to **Event Management** &gt; **Anomaly Detection** &gt; **Metric Types**.

        The **Monitoring System Metric Types** page appears.

        ![Monitoring System Metric Types page](../image/monitoring-system-metric-types.png "Monitoring System Metric Types")

    2.  To prevent sending metrics for a metric type, set the value of the **Active** column to **false**.


