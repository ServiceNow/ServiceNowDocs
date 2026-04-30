---
title: Configure the action level for anomaly detection
description: Create a configuration setting rule that refines the level of anomaly detection processing and analysis that is applied to specific CIs and metrics. Set a processing level that reflects the importance of metrics at different stages of implementation, to reduce data load if needed.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Monitoring, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Configure the action level for anomaly detection

Create a configuration setting rule that refines the level of anomaly detection processing and analysis that is applied to specific CIs and metrics. Set a processing level that reflects the importance of metrics at different stages of implementation, to reduce data load if needed.

Anomaly detection consists of multiple levels of processing. At the lowest level, metric data is gathered from data sources. At the highest level, statistical models are created, anomaly scores are calculated, and anomaly alerts and IT alerts are created. You can apply the full anomaly detection process or a reduced level of processing, for specific data series.

Use the **anomaly\_detection\_action\_level** configuration setting in a [configuration setting rule](../task/create-config-overriding-rule.md) to set the level of processing for specific CIs and metrics. For example, you can initially set only a small percentage of CIs and metrics to generate anomaly alerts, and later increase that percentage.

## Action levels

The **anomaly\_detection\_action\_level** configuration setting provides action levels starting at 'Metrics only' for basic anomaly processing, and ending at 'IT Alerts' for full processing and analysis.

Action levels from lowest to highest:

-   **Metrics Only**

    Only gather metrics from the data source without any further processing.

-   **Bounds**

    'Metrics Only' processing level and in addition creates statistical model and show bounds in Insights Explorer.

-   **Anomaly Scores**

    'Bounds' processing level and in addition calculates and display anomaly scores.

-   **Anomaly Alerts**

    'Anomaly Scores' processing level and in addition creates anomaly alerts as applicable.

-   **IT Alerts**

    'Anomaly Alerts' processing level and in addition creates IT alerts which are based on anomaly alerts, as applicable.


**Related topics**  


[Create a configuration settings rule](../task/create-config-overriding-rule.md)

