---
title: CIs in maintenance mode
description: Configure anomaly detection to exclude metrics for CIs that are in maintenance mode from model learning.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# CIs in maintenance mode

Configure anomaly detection to exclude metrics for CIs that are in maintenance mode from model learning.

You can change the settings of system properties to include or exclude metric data for CIs while they are in maintenance mode.

When the system property [sa.model\_learner.maint\_event\_record\_history\_enabled](../reference/installed-with-metrics.md) is set to true \(default\), Metric Intelligence stores historical information about the times CIs enter and exit maintenance mode. When the system property [sa\_metric.maint\_exclusion](../reference/installed-with-metrics.md) is set to true \(default\), metrics from CIs that are in maintenance mode are excluded from model learning.

**Parent Topic:**[Metric Intelligence](operational-metrics.md)

