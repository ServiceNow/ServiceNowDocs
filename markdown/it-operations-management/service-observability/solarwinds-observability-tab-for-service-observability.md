---
title: SolarWinds Observability tab for Service Observability
description: Dashboard and charts on the SolarWinds Observability tab of the Service Details page in the SOW.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [SolarWinds templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# SolarWinds Observability tab for Service Observability

Dashboard and charts on the SolarWinds Observability tab of the Service Details page in the SOW.

**Note:** The X axis on SolarWinds charts use Universal Time Code \(UTC\) instead of the user's timezone.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Rate|Aggregate rate of transactions through the service, per minute.|SolarWinds|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|SolarWinds|
|Time spent in database calls|Duration of requests to databases, in milliseconds.|SolarWinds|
|Time spent in database queries|Time spent querying the database, in milliseconds.|SolarWinds|
|Database throughput|Rate of database requests for this service per minute.|SolarWinds|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the host processing power being consumed.|SolarWinds|
|Memory utilization|Percent of memory the host is using.|SolarWinds|
|Disk utilization|Percent of disk space being used.|SolarWinds|
|All Active Servers|Information for all hosts the service is actively using. Select a host link to view more detailed information.|CMDB|
|All Active VM Instances|Information for all virtual machine instances the service is actively using. Select a VM link to view more detailed information.|CMDB|

## Database dashboards

Database metrics are currently not supported for SolarWinds.

## Networking dashboards

These dashboards display metrics for network devices related to the service.

By default, the Firewall dashboard displays Palo Alto metrics and the Load Balancer dashboard displays F5 Big-IP metrics.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU Utilization|Percentage of CPU utilization on the firewall device.|SolarWinds|
|Session Utilization|Percentage of session capacity currently in use.|SolarWinds|
|Drop Rate|Percentage of network packets/connections that the device has intentionally blocked or failed to process.|SolarWinds|
|Availability|Percentage of time the firewall is available.|SolarWinds|
|Recent Changes|Table displaying recent configuration changes made to the firewall device.|CMDB|
|Current Open Incidents|Table listing active incidents affecting the firewall device.|CMDB|
|All Active Alerts|Table listing all active alerts related to the firewall device.|CMDB|

<table id="table_v5n_czg_d3c"><thead><tr><th>

Chart

</th><th>

Description

</th><th>

Data source

</th></tr></thead><tbody><tr><td>

Connection Utilization

</td><td>

Percentage of available connections currently in use.

</td><td>

SolarWinds

</td></tr><tr><td>

Inbound Rate

</td><td>

Rate of bytes per second received from the configured nodes.

</td><td>

SolarWinds

</td></tr><tr><td>

Outbound Rate

</td><td>

Rate of bytes per second sent to the configured nodes.

</td><td>

SolarWinds

</td></tr><tr><td>

Pool Member Status

</td><td>

Pool Availability Status:-   `0`: None \(no status available\)
-   `1`: Available, all members healthy
-   `2`: Degraded, some members down
-   `3`: Unavailable, all members down
-   `4`: Unknown, status cannot be determined

</td><td>

SolarWinds

</td></tr><tr><td>

Error

</td><td>

Percentage of inbound errors on the load balancer.

</td><td>

SolarWinds

</td></tr><tr><td>

Latency

</td><td>

Aggregate duration of transactions through the load balancer, in milliseconds.

</td><td>

SolarWinds

</td></tr></tbody>
</table>|Chart|Description|Data source|
|-----|-----------|-----------|
|Error|Percentage of inbound errors on the interface.|SolarWinds|
|Traffic|Rate in bytes per second of traffic through the interface.|SolarWinds|
|Bandwidth Utilization|Percentage of available bandwidth.|SolarWinds|

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU Utilization|Percentage of CPU utilization on the networking device.|SolarWinds|
|Packet Loss|Percentage of packets dropped.|SolarWinds|
|Error|Percentage of errors on the networking device.|SolarWinds|

**Parent Topic:**[SolarWinds templates for Service Observability](solarwinds-templates.md)

