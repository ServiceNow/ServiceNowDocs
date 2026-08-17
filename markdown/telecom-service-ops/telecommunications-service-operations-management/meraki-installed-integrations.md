---
title: Cisco Meraki installed integrations
description: Predefined system integrations use Meraki REST APIs to pull metric data into your ServiceNow instance to monitor your Cisco Meraki devices. Each integration is driven by a connector instance whose metric parameter determines the data that the instance collects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/meraki-installed-integrations.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Cisco Meraki installed integrations

Predefined system integrations use Meraki REST APIs to pull metric data into your ServiceNow instance to monitor your Cisco Meraki devices. Each integration is driven by a connector instance whose metric parameter determines the data that the instance collects.

|Cisco Meraki integration|Description|Metric parameter value|
|------------------------|-----------|----------------------|
|Device Performance|Collects performance metrics from devices, including utilization, throughput, and availability data.|`getDevicePerformance`|
|Uplink Statuses|Monitors the connectivity status of WAN uplinks on MX and Z series devices.|`getUplinkStatuses`|
|Configuration Changes|Tracks configuration changes made to devices and networks in the dashboard.|`getConfigurationChanges`|
|Network Shaping Uplink Bandwidth|Collects configured bandwidth limits for WAN uplinks used in traffic shaping.|`getNetworkShapingUplinkBandwidth`|
|Switch Port Statuses by Switch|Monitors port status and connectivity for MS switches.|`getSwitchPortsStatusesBySwitch`|
|Uplink Usage by Network|Collects uplink bandwidth usage data aggregated by network for MX and Z series devices.|`getUplinksUsageByNetwork`|
|Uplinks Loss and Latency|Monitors packet loss and latency for WAN uplinks on MX appliances.|`getUplinksLossAndLatency`|
|VPN Stats|Monitors site-to-site VPN tunnel status for MX appliances.|`getVpnStats`|

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

**Related topics**  


[Metric type IDs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/tsom-metric-type-ids.md)

