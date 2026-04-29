---
title: Multi-consumer support using unique mid servers
description: You can now precisely manage log consumption with a new multi-consumer system, enabling dedicated consumers and MID servers for each specific log stream.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MID server consumer, Configure, Log Export Service \(LES\), Platform Security]
---

# Multi-consumer support using unique mid servers

You can now precisely manage log consumption with a new multi-consumer system, enabling dedicated consumers and MID servers for each specific log stream.

The system now supports multi-consumer log consumption which means each log source can be consumed separately have its own dedicated topic.

Previously, all logs were consumed from the same topic. However, with the new multi-topic concept, you can create multiple consumers for different topics. To create a consumer, you can select the following:

-   A specific topic from the dropdown menu
-   Respective destination configuration
-   Respective consumer context

    **Note:** Starting Zurich release, the **Consumer context** is a new field added in the Consumer form. Each consumer context is associated with one unique mid server.


To create multiple consumers, you are required to select distinct topics for each consumer, which in turn would require to create separate consumer context records and its corresponding unique mid servers.

## Parallel processing with multiple MID servers

A major benefit of this multi-consumer architecture is the ability to run multiple consumers in parallel. This parallel processing significantly enhances the overall throughput and efficiency of log consumption, allowing the system to handle larger volumes of diverse log data more effectively than before.

**Note:** For a mid server consumer, the maximum production level throughput is 31500 msg/sec. You can use 27,000 msg/sec as the reliable sustained throughput.

**Parent Topic:**[MID server consumer](les-mid-server-consumer.md)

