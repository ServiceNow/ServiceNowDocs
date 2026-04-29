---
title: Azure Monitor Observability tab for Service Observability
description: Dashboard and charts on the Azure Monitor Observability tab of the Service Details page in the SOW.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Azure Monitor templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Azure Monitor Observability tab for Service Observability

Dashboard and charts on the Azure Monitor Observability tab of the Service Details page in the SOW.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Requests|Aggregate rate of requests through the service.|Azure|
|Http 4xx|Number of transactions that have an HTTP 4xx response.|Azure|
|Response time|Aggregate duration of transactions through the service, in milliseconds.|Azure|
|Data Out|Volume in bytes of outgoing network traffic from this service.|Azure|
|Http 2xx|Number of transactions that have an HTTP 2xx response.|Azure|
|Data In|Volume in bytes of incoming network traffic to this service.|Azure|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Available Memory Percentage|Percent of the memory available to the service.|Azure|
|CPU %|Percent of the host processing power being consumed.|Azure|
|VM Cached Bandwidth Consumed Percentage|Percent of the virtual machine's cached bandwidth that the service is consuming.|Azure|
|All Active VM Instances|Information for all virtual machines \(VM\) the service is actively using. Select a VM link to view more information.|CMDB|
|All Active Servers|Information for all hosts the service is actively using. Select a host link to view more detailed information.|CMDB|

## Database dashboards

These dashboards display metrics for databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Storage %|Percentage of storage currently being consumed by the service.|Azure|
|CPU %|Percentage of CPU currently being consumed by the service.|Azure|
|Memory %|Percentage of memory currently being consumed by the service.|Azure|
|Active Connections|Number of connections currently used by the service.|Azure|
|Aborted Connections|Number of connections from the service terminated by the database|Azure|
|MySQL Uptime|Total time in seconds that this MySQL instance has been running since its last restart.|Azure|
|Slow Queries|Number of queries that take longer than the specified threshold to execute. This threshold is typically defined by the `long_query_time` parameter in MySQL.|Azure|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Storage %|Percentage of storage currently being consumed by the service.|Azure|
|CPU %|Percentage of CPU currently being consumed by the service.|Azure|
|Memory %|Percentage of memory currently being consumed by the service.|Azure|
|Active Connections|Number of connections currently used by the service.|Azure|
|Aborted Connections|Number of connections from the service terminated by the database|Azure|
|Succeeded Connections|Number of successful connections from the service to the database.|Azure|
|Deadlocks|Number of deadlocks encountered by the service.|Azure|
|Is Database Alive|`1` if database is up, `0` if it is down.|Azure|
|All PostgreSQL Instances|Information of all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[Azure Monitor templates for Service Observability](azure-templates.md)

