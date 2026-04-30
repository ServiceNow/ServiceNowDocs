---
title: Metric bounds sensitivity
description: When measuring metrics in Insights Explorer, metric bounds may be overly sensitive, creating an abnormally large number of anomalies. When this happens, the system adjusts itself to ensure that fewer anomalies are created.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Metric bounds sensitivity

When measuring metrics in Insights Explorer, metric bounds may be overly sensitive, creating an abnormally large number of anomalies. When this happens, the system adjusts itself to ensure that fewer anomalies are created.

For example, if 95% of a CI’s metric values fall within 2 standard deviations \(STDs\) of the mean metric values, those are considered **sensitive bounds**. Sensitive bounds generate a large number of anomalies, some of which may be irrelevant. When sensitive bounds are detected, the system adjusts to measure metric values within 5 STDs, to generate fewer anomalies.

If sensitive bounds are not detected, \(that is, 95% of metrics do not fall within 2 STDs of the mean metric value\), the system measures metric values within 3 STDs. Any metric values falling outside the configured bounds become anomalies.

The previous values are set by default. For details on customizing these values, see [Sensitivity bounds properties for Insights Explorer metrics](../reference/metric-bounds-properties.md).

