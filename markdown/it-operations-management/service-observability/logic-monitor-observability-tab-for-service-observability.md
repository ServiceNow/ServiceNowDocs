---
title: LogicMonitor Observability tab for Service Observability
description: Dashboard and charts on the LogicMonitor Observability tab of the Service Details page in the SOW.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [LogicMonitor templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# LogicMonitor Observability tab for Service Observability

Dashboard and charts on the LogicMonitor Observability tab of the Service Details page in the SOW.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Response Time|Response time metrics for the service, displayed in milliseconds over time.|LogicMonitor|
|Status|Status metrics for the service. A value of `1` means the service is up. A value of `2` means it's down.|LogicMonitor|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU Busy %|Percentage of time the CPU is actively busy processing tasks, showing periods of high activity versus idle time.|LogicMonitor|
|Memory Usage|Percent of memory the host is using.|LogicMonitor|
|CPU Utilization|Overall CPU load and usage patterns across the host, showing continuous utilization levels over time.|LogicMonitor|
|Network RX - bytes transferred|Amount of data received by the host over the network, measured in bytes.|LogicMonitor|
|Network TX - bytes transferred|Amount of data transmitted by the host over the network, measured in bytes.|LogicMonitor|
|All Active Servers|Information for all servers the service is actively using. Select a host link to view more detailed information.|CMDB|

## Database dashboards

These dashboards display metrics for databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Response Time|Response time metrics for the database, displayed in milliseconds over time.|LogicMonitor|
|CPU Busy %|Percent of the database's processing power being consumed.|LogicMonitor|
|Memory Used %|Percent of memory the database is using.|LogicMonitor|
|Status|Status metrics for the service. A value of `1` means the database is up. A value of `2` means it's down.|LogicMonitor|
|All MySQL Instances|Information for all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Response time|Response time metrics for the database, displayed in milliseconds over time.|LogicMonitor|
|CPU Busy %|Percent of the database's processing power being consumed.|LogicMonitor|
|Memory Used %|Percent of memory the database is using.|LogicMonitor|
|Status|Status metrics for the service. A value of `1` means the database is up. A value of `2` means it's down.|LogicMonitor|
|Busy servers|Number of busy servers for the database over time.|LogicMonitor|
|Maximum servers|Maximum number of servers available for the database.|LogicMonitor|
|All PostgreSQL Instances|Information of all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[LogicMonitor templates for Service Observability](logic-monitor-templates.md)

