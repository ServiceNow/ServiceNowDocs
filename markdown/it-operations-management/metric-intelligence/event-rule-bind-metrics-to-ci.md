---
title: Creating an event rule to map metrics to specific CIs
description: Create event rules to map incoming raw metric data to specific CIs, to optionally modify metric names, and to populate the resource\_path attribute for resource binding.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Metric binding, Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Creating an event rule to map metrics to specific CIs

Create event rules to map incoming raw metric data to specific CIs, to optionally modify metric names, and to populate the **resource\_path** attribute for resource binding.

The system generates events for every new raw metric data for which there are no CI binding specifications. You can create event rules that filter those events to map the incoming metric data to specific CIs. In such event rules, you can for example define a filter that is based on the monitoring object \(such as SCOM\).

To use resource binding, the **resource\_path** attribute of events must be populated. You can configure an event rule to ensure that the **resource\_path** attribute is included in the **Additional information** field in events. For more information about configuring and using resource binding, see [resource binding](resource-binding.md).

For example, in the Event Rule designer you can update the event rule **SCOM IIS Web Server** as follows:

-   On the **Event Filter** tab, define filter to match only IIS Web Servers.
-   On the **Binding** tab, set **Class** to `Microsoft IIS Web Server`.

**Related topics**  


[Event rules](create-event-rules.md)

[View metric to CI and resource binding](../task/view-metric-to-CI-binding.md)

[Get started with Metric Intelligence](../task/get-started-metrics.md)

