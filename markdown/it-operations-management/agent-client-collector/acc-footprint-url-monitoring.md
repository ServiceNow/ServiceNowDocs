---
title: Agent Client Collector performance and footprint for URL monitoring
description: The following tables display the agent performance KPIs and its footprint on the host during URL monitoring data collection execution on different operation systems.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector performance and footprint for URL monitoring

The following tables display the agent performance KPIs and its footprint on the host during URL monitoring data collection execution on different operation systems.

|Linux Cent OS 8, 2 CPUs, 4GB RAM|
|--------------------------------|
|Checks per minute|100|250|500|1000|1500|
|Metrics \(expected/actual\)|700/700|1750/1750|3500/3500|7000/7000|10500/10500|
|Network utilization - Tx \(MID &gt; Agent\)|35 KB/s|78 KB/s|146 KB/s|286 KB/s|430 KB/s|
|Network utilization - Rx \(MID &lt; Agent\)|15 KB/s|27 KB/s|51 KB/s|107 KB/s|116 KB/s|
|Network utilization - Tx \(Agent &gt; MID\)|8 KB/s|23 KB/s|37 KB/s|89 KB/s|113 KB/s|
|Network utilization - Rx \(Agent &lt; MID\)|28 KB/s|72 KB/s|142 KB/s|285 KB/s|426 KB/s|
|Memory consumption|22 MB|25 MB|26 MB|34 MB|39 MB|
|CPU of all checks|~3%|~7%|~11%|~21%|~24%|
|Process CPU utilization|1% - 1.5%|1.5% - 2.5%|5% - 6%|6% - 7%|12% - 13%|
|Host CPU utilization|~10%|~19%|~23%|~45%|~53%|

**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

