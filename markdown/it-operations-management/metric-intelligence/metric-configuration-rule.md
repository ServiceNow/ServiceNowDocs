---
title: Metric Configuration Rules
description: Metric configuration rules enable you to determine how incoming metrics from the Agent Client Collector are to be processed.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Metric Configuration Rules

Metric configuration rules enable you to determine how incoming metrics from the Agent Client Collector are to be processed.

When a new metric arrives from an Agent Client Collector, a new record is created in the Metric to CI Mappings table, with the value, **Anomaly Detection Action Level = Bounds**.

To trigger execution of a metric configuration rule, navigate to the Metric Configuration Rules table \(**Event Management** &gt; **Anomaly Detection** &gt; **Metric Config Rules**\) and select the **Sync to MID** button at the top of the page. This also synchronizes all MID Servers connected to the instance.

When executing the rule, the anomaly detection action level defined in the rule \(set by the **anomaly\_detection\_action\_level** parameter\) retroactively overrides the anomaly detection action level configured for the metric in the Metric to CI Mappings table.

If you do not trigger the rule execution, retroactive overriding of the **Anomaly detection action level** parameter is performed during execution of the hourly scheduled **Metric Intelligence - Metric configuration** job.

When configuring a metric configuration rule, rules with a filter run before rules with no filter. When multiple rules have the same priority, the most recently configured rule runs first.

For details on creating configuration settings rules, see [Create a configuration settings rule](../../event-management/task/create-config-overriding-rule.md).

For details on the available anomaly detection action levels, see [Configure the action level for anomaly detection](../../event-management/concept/configure-level-anomaly-detection.md).

