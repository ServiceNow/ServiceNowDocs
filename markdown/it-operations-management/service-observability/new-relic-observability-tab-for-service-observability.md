---
title: New Relic Observability tab for Service Observability
description: Dashboard and charts on the New Relic Observability tab of the Service Details page in the SOW.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-03-19"
reading_time_minutes: 2
breadcrumb: [New Relic templates, Observability templates, Service Observability reference, Service Observability, ITOM Health, IT Operations Management]
---

# New Relic Observability tab for Service Observability

Dashboard and charts on the New Relic Observability tab of the Service Details page in the SOW.

## Application &gt; Service dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Rate|Aggregate rate of transactions through the service, per minute.|New Relic|
|Error %|Percent of transactions that have an error.|New Relic|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|New Relic|
|Time spent in database calls|Duration of requests to databases, in milliseconds.|New Relic|
|Database throughput|Rate of database requests for this service, per minute.|New Relic|
|Time spent in database queries|Time spent querying the database, in milliseconds.|New Relic|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Rate|Each line represents the throughput of a key transaction through the service. Hover over a point to view the different transaction names.|New Relic|
|Error %|Each line represents the percentage of errors on a key transaction in the service. Hover over a point to view the different transaction names.|New Relic|
|Latency|Each line represents the response time for a key transaction on the service. Hover over a point to view the different transaction names.|New Relic|

## Compute &gt; Host dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the host processing power being consumed.|New Relic|
|Memory utilization|Percent of memory the host is using.|New Relic|
|Disk utilization|Percent of disk space being used.|New Relic|
|Network traffic received per host| |New Relic|
|All Active Hosts|Information for all hosts the service is actively using. Select a host link to view more detailed information.|CMDB|

## Databases &gt; MySQL

This dashboard displays metrics for MySQL databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the database's processing power being consumed.|APM instance|
|Memory utilization|Percent of memory the database is using.|APM instance|
|Availability|Percent of time the database is available.|APM instance|
|Connections|Number of connections to the database.|APM instance|
|Slow queries|Number of database queries that have been categorized as slow by the APM.|APM instance|
|All MySQL Instances|Information for all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

## Databases &gt; PostgreSQL

This dashboard displays metrics for PostgreSQL databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Scheduled Checkpoints|Average number of scheduled checkpoints that were performed.|APM instance|
|Buffers Written for Checkpoint|Average number of buffers written during checkpoints.|APM instance|
|Buffers Written by Background Writer|Average number of buffers written by the background writer.|APM instance|
|Buffers Allocated|Average number of buffers allocated.|APM instance|
|Checkpoint Write Time|Time in milliseconds spent writing files to disk.|APM instance|
|All PostgreSQL Instances|Information of all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[New Relic templates](new-relic-templates.md)

