---
title: Prometheus Observability tab for Service Observability
description: Dashboard and charts on the Prometheus Observability tab of the Service Details page in the SOW.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Prometheus templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Prometheus Observability tab for Service Observability

Dashboard and charts on the Prometheus Observability tab of the Service Details page in the SOW.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Request Rate|Aggregate rate of transactions through the service, per second.|Prometheus|
|Error %|Percent of transactions that have an error.|Prometheus|
|Average Response Time|Aggregate duration of transactions through the service, in seconds.|Prometheus|
|Throughput|Count of successful transactions, per second.|Prometheus|
|Active Requests|Count of current in-flight requests to the service.|Prometheus|
|Response Time \(95th Percentile\)|95th percentile response time for HTTP requests, in seconds.|Prometheus|
|Average Request Size|Average size of requests to the service, in bytes.|Prometheus|
|Average Response Size|Average size of responses from the service, in bytes.|Prometheus|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the host processing power being consumed.|Prometheus|
|Memory utilization|Percent of memory the host is using.|Prometheus|
|Disk utilization|Percent of the host disk being used.|Prometheus|
|All Active Servers|Information for all servers the service is actively using. Select a host link to view more detailed information.|CMDB|
|All Active VM Instances|Information for all virtual machines the service is actively using. Select a host link to view more detailed information.|CMDB|

## Database dashboards

These dashboards display metrics for databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Thread Utilization %|Percent of the database's threads being consumed.|Prometheus|
|Queries Per Second|Number of queries made to the database by the service, per second.|Prometheus|
|InnoDB Memory %|Percent of InnoDB buffer pool being consumed.|Prometheus|
|Active Connections|Number of connections to the database.|Prometheus|
|Aborted Connections|Rate of aborted connections.|Prometheus|
|Uptime|Average number of hours the database has been available.|Prometheus|
|Inbound Network Traffic|Number of bytes per second of inbound traffic to the database.|Prometheus|
|Outbound Network Traffic|Number of bytes per second of outbound traffic to the database.|Prometheus|
|Slow Queries|Rate of slow queries detected by MySQL, per second.|Prometheus|
|All MySQL Instances|Information for all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Active Sessions|Count of sessions currently active.|Prometheus|
|Idle Sessions|Count of idle sessions.|Prometheus|
|Committed Transactions|Total committed transactions since server start.|Prometheus|
|Failed Transactions|Total rolled back transactions since server start.|Prometheus|
|Deadlocks|Total deadlocks detected since server start.|Prometheus|
|Locks Count|Current count of locks given out by the database.|Prometheus|
|Cache Hit Ratio|Percentage of database requests that can be served by the cache.|Prometheus|
|All PostgreSQL Instances|Information of all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[Prometheus templates for Service Observability](prometheus-templates.md)

