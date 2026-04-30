---
title: Agent Client Collector Monitoring Footprint
description: The following table describes Agent Client Collector resource consumption. We supply performance testing values to specific customers upon request.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Monitoring Footprint

The following table describes Agent Client Collector resource consumption. We supply performance testing values to specific customers upon request.

|Parameters|Linux|Windows|
|----------|-----|-------|
|Machine spec|Cent OS 8, 4 CPU Core, 8GB Memory|Windows Server 2019, 2 CPU, 4GB Memory|
|Network - \(Agent &gt; MID\)|10.64 KB/s|350-400 byte/s|
|Network - \(MID &gt; Agent\)|48 byte/s|5-15 byte/s|
|Average CPU Utilization|~1%|~3.89%|
|Max CPU per check|10 to 15%|15 to 20%|
|Memory overhead \(avg\)|~13.88 MB|~31.15 MB|

**Parent Topic:**[Agent Client Collector Monitoring reference](acc-monitoring-reference.md)

