---
title: Metric type IDs
description: Metric type IDs identify each time-series metric that a connector writes to the metrics database. Use these IDs to locate metrics in Insights Explorer or when you build custom dashboards and indicators.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/tsom-metric-type-ids.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-08-02"
reading_time_minutes: 1
keywords: [metric type ID, Insights Explorer]
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Metric type IDs

Metric type IDs identify each time-series metric that a connector writes to the metrics database. Use these IDs to locate metrics in Insights Explorer or when you build custom dashboards and indicators.

## Cisco Meraki metric type IDs

|Metric type ID|Unit|Description|
|--------------|----|-----------|
|`meraki.uplink.status`|Boolean|Uplink up or down.|
|`uplink.usage.sent`|Bytes|Bytes sent on the uplink.|
|`uplink.usage.received`|Bytes|Bytes received on the uplink.|
|`uplink.throughput.sent`|bps|Throughput sent on the uplink.|
|`uplink.throughput.received`|bps|Throughput received on the uplink.|
|`uplink.latency`|ms|Uplink latency.|
|`uplink.loss`|Percent|Uplink packet loss.|
|`uplink.bandwidth.limit.upload`|bps|Configured upload bandwidth limit for the uplink.|
|`uplink.bandwidth.limit.download`|bps|Configured download bandwidth limit for the uplink.|
|`vpn.usage.sent`|KB|Data sent over the VPN tunnel.|
|`vpn.usage.received`|KB|Data received over the VPN tunnel.|
|`vpn.minJitter`, `vpn.maxJitter`, `vpn.avgJitter`|ms|Minimum, maximum, and average VPN jitter.|
|`vpn.minLatency`, `vpn.maxLatency`, `vpn.avgLatency`|ms|Minimum, maximum, and average VPN latency.|
|`vpn.minPercentageLoss`, `vpn.maxPercentageLoss`, `vpn.avgPercentageLoss`|Percent|Minimum, maximum, and average VPN packet loss.|
|`vpn.minMOS`, `vpn.maxMOS`, `vpn.avgMOS`|String|Minimum, maximum, and average VPN Mean Opinion Score.|
|`device.performance.score`|String|Device performance score.|
|`switch.port.status`|Boolean|Switch port status.|

## Fortinet metric type IDs

|Metric type ID|Unit|Description|
|--------------|----|-----------|
|`fortinet.sdwan.sla.latency`|ms|SD-WAN SLA latency.|
|`fortinet.sdwan.sla.jitter`|ms|SD-WAN SLA jitter.|
|`fortinet.sdwan.sla.packetloss`|Percent|SD-WAN SLA packet loss.|
|`fortinet.sdwan.sla.link_up`|Boolean|SD-WAN link up or down status.|
|`fortinet.sdwan.sla_log.count`|String|SLA log entry count.|
|`fortinet.performance.cpu.usage`|Percent|FortiGate CPU usage.|
|`fortinet.performance.memory.usage`|Percent|FortiGate memory usage.|

VERIFY: Confirm the metric type IDs written by the Fortinet SD-WAN Interface Log integration. This integration is listed in the installed integrations reference but its metric type IDs are not yet documented here.

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

