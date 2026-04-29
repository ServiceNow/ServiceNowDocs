---
title: Zabbix Observability template for Service Observability
description: Dashboard and charts on the Zabbix Observability tab of the Service Details page in the SOW.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Zabbix templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Zabbix Observability template for Service Observability

Dashboard and charts on the Zabbix Observability tab of the Service Details page in the SOW.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU Usage \(System\)|CPU usage percentage over time.|Zabbix|
|CPU Load|CPU load for the system: rolling one minute average.|Zabbix|
|Running Processes|Number of processes currently running on the system.|Zabbix|
|Available Memory \(%\)|Percentage of memory currently available on the system.|Zabbix|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU Load|CPU load average for the host on a rolling one minute average.|Zabbix|
|CPU Idle Time|Percentage of time the CPU is idle.|Zabbix|
|Memory Available|Percentage of available memory on the host.|Zabbix|
|Running Processes|Number of processes currently running on the host.|Zabbix|
|Network RX|Network data received in bytes per second.|Zabbix|
|Network TX|Network data transmitted in bytes per second.|Zabbix|
|All Active Servers|Information for all active server instances with their operating system, CPU count, RAM, disk space, and support group information.|CMDB|
|All Active VM Instances|Information for all virtual machine instances the service is actively using. Select a VM link to view more detailed information.|CMDB|

## Database dashboards

These dashboards display metrics for databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Active Connections|Number of active database connections.|Zabbix|
|Queries Per Second|Rate of database queries executed per second.|Zabbix|
|Rows Deleted By Queries Per Second|Number of rows deleted by queries per second.|Zabbix|
|Rows Returned By Queries Per Second|Number of rows returned by queries per second.|Zabbix|
|Rows Inserted By Queries Per Second|Number of rows inserted by queries per second.|Zabbix|
|Rows Updated By Queries Per Second|Number of rows updated by queries per second.|Zabbix|
|All MySQL Instances|Table listing all MySQL database instances with their operational status, class, and support group information.|CMDB|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Number of Connections|Total number of active database connections.|Zabbix|
|Number of Waiting Connections|Number of database connections currently waiting.|Zabbix|
|Connected Backends|Number of connected backend processes.|Zabbix|
|Rows Returned By Queries Per Second|Number of rows returned by queries per second.|Zabbix|
|Rows Inserted By Queries Per Second|Number of rows inserted by queries per second.|Zabbix|
|Rows Deleted By Queries Per Second|Number of rows deleted by queries per second.|Zabbix|
|All Postgresql Instances|Table listing all PostgreSQL database instances with their operational status, discovery source, category, subcategory, and support group information.|CMDB|

## Networking dashboards

These dashboards display metrics for network devices related to the service.

By default, the Firewall dashboard displays Palo Alto metrics and the Load Balancer dashboard displays F5 Big-IP metrics.

<table id="table_u5n_czg_d3c"><thead><tr><th>

Chart

</th><th>

Description

</th><th>

Data source

</th></tr></thead><tbody><tr><td>

CPU Utilization

</td><td>

Percentage of CPU utilization on the firewall device.

</td><td>

Zabbix

</td></tr><tr><td>

Session Utilization

</td><td>

Percentage of session capacity currently in use.

</td><td>

Zabbix

</td></tr><tr><td>

Memory Utilization

</td><td>

Percentage of memory utilization on the firewall device.

</td><td>

Zabbix

</td></tr><tr><td>

Availability

</td><td>

Uptime and availability status of the firewall device:-   `0`: Unavailable
-   `1`: Available

</td><td>

Zabbix

</td></tr><tr><td>

Recent Changes

</td><td>

Table displaying recent configuration changes made to the firewall device.

</td><td>

CMDB

</td></tr><tr><td>

Current Open Incidents

</td><td>

Table listing active incidents affecting the firewall device.

</td><td>

CMDB

</td></tr><tr><td>

All Active Alerts

</td><td>

Table listing all active alerts related to the firewall device.

</td><td>

CMDB

</td></tr></tbody>
</table><table id="table_v5n_czg_d3c"><thead><tr><th>

Chart

</th><th>

Description

</th><th>

Data source

</th></tr></thead><tbody><tr><td>

Current Connections \(To Node\)

</td><td>

Number of current connections from server-side to the configured nodes.

</td><td>

Zabbix

</td></tr><tr><td>

Requests TX

</td><td>

Rate of bytes per second sent to server-side from the configured nodes.

</td><td>

Zabbix

</td></tr><tr><td>

Requests RX

</td><td>

Rate of bytes per second received server-side from the configured nodes.

</td><td>

Zabbix

</td></tr><tr><td>

Pool Availability State

</td><td>

Pool Availability Status:-   `0`: None \(no status available\)
-   `1`: Available, all members healthy
-   `2`: Degraded, some members down
-   `3`: Unavailable, all members down
-   `4`: Unknown, status cannot be determined

</td><td>

Zabbix

</td></tr><tr><td>

Packets TX

</td><td>

Number of packets transmitted per second from the server-side to the configured nodes.

</td><td>

Zabbix

</td></tr><tr><td>

Packets RX

</td><td>

Number of packets received per second by the server-side from the configured nodes.

</td><td>

Zabbix

</td></tr><tr><td>

Inbound Error %

</td><td>

Percentage of inbound errors on the load balancer.

</td><td>

Zabbix

</td></tr><tr><td>

Outbound Error %

</td><td>

Percentage of outbound errors on the load balancer.

</td><td>

Zabbix

</td></tr></tbody>
</table><table id="table_ydz_fzg_d3c"><thead><tr><th>

Chart

</th><th>

Description

</th><th>

Data source

</th></tr></thead><tbody><tr><td>

CPU Utilization

</td><td>

Percentage of CPU utilization on the networking device.

</td><td>

Zabbix

</td></tr><tr><td>

Availability

</td><td>

Uptime and availability status of the networking device:-   `0`: Unavailable
-   `1`: Available

</td><td>

Zabbix

</td></tr><tr><td>

Inbound Error %

</td><td>

Percentage of inbound errors on the networking device.

</td><td>

Zabbix

</td></tr><tr><td>

Outbound Error %

</td><td>

Percentage of outbound errors on the networking device.

</td><td>

Zabbix

</td></tr><tr><td>

Inbound Traffic

</td><td>

Amount of inbound network traffic in bytes per second.

</td><td>

Zabbix

</td></tr><tr><td>

Outbound Traffic

</td><td>

Amount of outbound network traffic in bytes per second.

</td><td>

Zabbix

</td></tr></tbody>
</table>**Parent Topic:**[Zabbix templates](zabbix-templates.md)

