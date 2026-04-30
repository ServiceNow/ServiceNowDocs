---
title: Exploring Metric Intelligence
description: Learn more about using Metric Intelligence to analyze metric data and identify anomalies.
locale: en-US
release: yokohama
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Metric Intelligence, IT Operations Management]
---

# Exploring Metric Intelligence

Learn more about using Metric Intelligence to analyze metric data and identify anomalies.

## Metric Intelligence overview

Metric Intelligence helps identify and avoid potential service outages. Based on historical metric data, Metric Intelligence indicates anomalous behavior of CIs which events might not capture.

## Metric Intelligence users

<table id="table_o3l_jxq_ydc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event Management user\[evt\_mgmt\_user\]

</td><td>

Can view alerts and their underlying metrics.

</td></tr><tr><td>

Event Management administrator\[evt\_mgmt\_admin\]

</td><td>

Can configure all metric definitions and connector settings.

</td></tr><tr><td>

Operator\[evt\_mgmt\_operator\]

</td><td>

Can view all metric definitions and connector settings.

</td></tr></tbody>
</table>## Metric Intelligence workflow

The following illustration describes the layout and data flow within the Metric Intelligence application.

![Infographic outlining Metric Intelligence workflow](../../agent-client-collector/image/mi-infographic.png "Metric Intelligence Pipeline")

1.  Data collection: Agents, third-party connectors, and custom connectors \(REST\) gather performance data from servers and infrastructure components. Data collected by agents is passed to the MID Server via the WebSocket, and data gathered by third-party and custom connectors is passed to the MID Server via the Connector.
2.  Data normalization: Raw data is formatted by the Normalizer to make it legible to the metric base.
3.  Data grouping: Data is grouped by the Batcher and sent to the REST API on the instance \(Glide\).
4.  Data transference to the Clotho TSDB: REST API processes data and sends it to the Clotho TSDB.
5.  Model creation: The Trainer/Learner job runs and creates a model based on the received data. For example, the job may learn that the threshold for normal CPU usage is 60%. A new model is created every day, based on that day's data together with past data \(most models collect data from the past 14 days\).
6.  Model data transference to the Time Series Model Cache DB: The data is sent to the Time Series Model Cache DB on the MID Server via the instance \(Glide\). The model cache stores the bounds of the 'normal' model.
7.  Anomaly detection: Data outside the bounds of normal is detected by the MID Server and is rendered an anomaly score. Anomalies are stored on the instance and are displayed in the Service Operations Workspace. Anomaly detection is performed in real-time, so customers are made aware of anomalies immediately.

## Metric Intelligence benefits

<table id="table_r3l_jxq_ydc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Monitor your system’s health, performance, and availability through automated collection of events and metrics, leveraging automated configurations.

</td><td>

[Agent Client Collector Monitoring](../../agent-client-collector/concept/acc-monitoring-landing-page.md)

</td><td>

NOC Operator, Event Management administrator

</td></tr><tr><td>

Reduce noise by promoting only the most meaningful anomalies.

</td><td>

[View anomaly alerts](../../event-management/task/view-metrics-anomaly-alerts.md)

 [Create metric rules](../../agent-client-collector/task/create-metric-rules.md)

</td><td>

Event Management administrator

</td></tr><tr><td>

Detect anomalies with AI-based anomaly detection, either with unsupervised machine-learning abnormal pattern detection \(no user intervention\), or by setting deterministic alert rules \(manually setting a static threshold\).

</td><td>

[How Health Log Analytics generates alerts](../../health-log-analytics-operator/concept/hla-op-anomalies-detecting.md)

</td><td>

Event Management administrator

</td></tr><tr><td>

Improve resolution time on open alerts and incidents with raw metric data visualization.

</td><td>

[Metric Explorer](../../event-management/concept/agent-workspace-ops-intelligence.md)

</td><td>

NOC Operator, Event Management administrator

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Metric Intelligence, see:

-   [Configuring Metric Intelligence](configuring-metric-intelligence.md)
-   [Optimizing Metric Intelligence](optimizing-metric-intelligence.md)
-   [Metric Intelligence reference](../reference/metric-intelligence-reference.md)

