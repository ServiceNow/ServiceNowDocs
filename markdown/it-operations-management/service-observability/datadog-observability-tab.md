---
title: Datadog Observability tab for Service Observability
description: Dashboard and charts on the Datadog Observability tab of the Service Details page in the SOW.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Datadog templates, Observability templates, Service Observability reference, Service Observability, ITOM Health, IT Operations Management]
---

# Datadog Observability tab for Service Observability

Dashboard and charts on the Datadog Observability tab of the Service Details page in the SOW.

## Application &gt; Service dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Requests|Aggregate rate of requests through the service.|Datadog|
|Errors|Number of transactions that have an error.|Datadog|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|Datadog|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Requests|Each line represents the throughput of a key transaction through the service. Hover over a point to view the different transaction names.|Datadog|
|Errors|Each line represents the number of errors on a key transaction in the service. Hover over a point to view the different transaction names.|Datadog|
|Latency|Each line represents the response time for a key transaction on the service. Hover over a point to view the different transaction names.|Datadog|

## Compute &gt; Host dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU Utilization|Percent of the host processing power being consumed.|Datadog|
|Memory Utilization|Percent of memory the host is using.|Datadog|
|Disk Utilization|Percent of disk space being used.|Datadog|
|All Active Servers|Information for all hosts the service is actively using. Select a host link to view more detailed information.|CMDB|
|All Active VM Instances|Information for all virtual machines \(VM\) the service is actively using. Select a VM link to view more information.|CMDB|

## Databases &gt; MySQL

This dashboard displays metrics for MySQL databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Max Connections|Maximum number of concurrent connections that can be established with the MySQL database server.|Datadog|
|Failed Connections|Number of failed attempts to connect to the MySQL server.|Datadog|
|Slow Queries Rate|Number of database queries that have been categorized as slow by the APM.|Datadog|
|Data Reads|Number of read operations performed on the MySQL database.|Datadog|
|Data Writes|Number of write operations performed on the MySQL database.|Datadog|
|Cache Utilization|Percentage of the cache memory being used by the MySQL database.|Datadog|
|All MySQL Instances|Information for all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

## Databases &gt; PostgreSQL

This dashboard displays metrics for PostgreSQL databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Connections|Total number of connections to the database server, including all connection states such as active, idle, and others.|Datadog|
|Connections Used|Number of connections to the database used by this service.|Datadog|
|Active Waiting Queries|Number of queries in the queue waiting to be executed.|Datadog|
|Deadlocks|Number of deadlocks encountered by the service.|Datadog|
|Rollbacks|Number of transactions rolled back by the service.|Datadog|
|Buffer Hits|Number of times disk blocks were found in the buffer cache, so that a read was not necessary.|Datadog|
|All PostgreSQL Instances|Information of all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[Datadog templates](datadog-templates.md)

