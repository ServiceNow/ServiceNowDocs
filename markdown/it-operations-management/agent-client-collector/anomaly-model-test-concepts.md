---
title: Anomaly model testing
description: Use anomaly model testing to apply and evaluate anomaly detection for a small set of CIs and metrics, using actual metric data. Compare test results to expected results, then fine-tune the anomaly detection model before enabling anomaly detection for the tested CIs and metrics in the production environment.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Anomaly model testing

Use anomaly model testing to apply and evaluate anomaly detection for a small set of CIs and metrics, using actual metric data. Compare test results to expected results, then fine-tune the anomaly detection model before enabling anomaly detection for the tested CIs and metrics in the production environment.

For example, before enabling anomaly detection for Linux Servers, you can use anomaly model testing with actual metric data collected for those Linux Servers. Existing alerts might indicate an anomaly for a specific metric and CI. You can create an anomaly test rule to test anomaly detection for those CIs and metrics, and then check if the expected anomaly is detected. You can also examine the bounds calculated by the anomaly model to see if they match expected bounds. After you fine-tune the test model, you can enable anomaly detection for Linux Servers.

Anomaly model testing supports up to 20 time series, which can include 20 metric types for the same CI, the same metric type for 20 different CIs, or any combination of those options.

## View test results in the Insights Explorer

Upon completion of a test run, a URL to an Insights Explorer becomes available. The anomaly model testing results appear in this trimmed-down version of the Insights Explorer. This Insights Explorer is pre-loaded with the charts and scores for the metric series specified in the anomaly test rule. You cannot add any CMDB groups or application services to this Insights Explorer.

Each chart in the Insights Explorer, contains the Anomaly Test Statistics section in its **Chart Settings**. This section is specific to anomaly model testing and provides the following options:

-   **Show Bounds**: Displays a computed upper and lower bound for the metric in an anomaly model testing, based on learning of past metric values. The upper and lower bounds always appear together.
-   **Show Anomaly Scores**: Displays anomaly scores on a virtual axis of 0-10, for an anomaly model test. Color code is based on the score thresholds that are defined in the Anomaly Score to Event Severity Map \[sa\_metric\_anomaly\_score\_to\_event\_severity\_map\] table.

## Use test results to fine-tune anomaly detection

Anomaly model testing uses the [upper and lower bounds](../task/override-metric-bounds.md) configured for selected series in the anomaly test rule. The anomaly model test results show how many anomaly alerts would have been generated based on the specified settings, if anomaly detection was enabled for the tested CIs and metrics. You can then decide if this result is acceptable. Fine-tune the bounds so that the number of anomaly alerts that are generated is not excessive, but sufficient to accurately indicate an out of bounds score.

**Parent Topic:**[Metric Intelligence](operational-metrics.md)

