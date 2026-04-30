---
title: CIs in maintenance mode
description: Configure anomaly detection to exclude metrics for CIs that are in maintenance mode from model learning.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# CIs in maintenance mode

Configure anomaly detection to exclude metrics for CIs that are in maintenance mode from model learning.

You can change the settings of system properties to include or exclude metric data for CIs while they are in maintenance mode.

When the system property [sa.model\_learner.maint\_event\_record\_history\_enabled](../reference/installed-with-metrics.md) is set to true \(default\), Metric Intelligence stores historical information about the times CIs enter and exit maintenance mode. When the system property [sa\_metric.maint\_exclusion](../reference/installed-with-metrics.md) is set to true \(default\), metrics from CIs that are in maintenance mode are excluded from model learning.

