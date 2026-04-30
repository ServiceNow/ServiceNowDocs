---
title: Dynatrace Observability tab for Service Observability
description: Dashboard and charts on the Dynatrace Observability tab of the Service Details page in the SOW.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Dynatrace templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Dynatrace Observability tab for Service Observability

Dashboard and charts on the Dynatrace Observability tab of the Service Details page in the SOW.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Rate|Aggregate rate of transactions through the service.|Dynatrace|
|Error %|Percent of transactions that have an error.|Dynatrace|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|Dynatrace|
|Client error rate|Rate of errors the service clients experienced.|Dynatrace|
|Client throughput|Rate of client requests for this service.|Dynatrace|
|Client response time|Response time for client requests on this service, in milliseconds.|Dynatrace|
|Total DB connections|Number of databases that this client has connections to.|Dynatrace|
|DB connection errors|Number of errors received by the client when trying to access databases.|Dynatrace|
|Time spent in database calls|Duration of requests to databases, in milliseconds.|Dynatrace|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Key Request Count|Each line represents the throughput of a key transaction through the service. Hover over a point to view the different transaction names.|Dynatrace|
|Key Request Error %|Each line represents the percentage of errors on a key transaction in the service. Hover over a point to view the different transaction names.|Dynatrace|
|Key Request Response Time|Each line represents the response time for a key transaction on the service. Hover over a point to view the different transaction names.|Dynatrace|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the host processing power being consumed.|Dynatrace|
|Memory utilization|Percent of memory the host is using.|Dynatrace|
|Disk utilization|Percent of disk space being used.|Dynatrace|
|All Active Servers|Information for all hosts the service is actively using. Select a host link to view more detailed information.|CMDB|
|All Active VM Instances|Information for all virtual machines \(VM\) the service is actively using. Select a VM link to view more information.|CMDB|

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU Usage|Percent of the host processing power being consumed.|Dynatrace|
|Memory Usage|Percent of memory the host is using.|Dynatrace|
|Requests|Rate of requests per second|Dynatrace|
|Throughput|Size of requests, in megabytes per second.|Dynatrace|
|Latency|Aggregate duration of transactions, in milliseconds.|Dynatrace|

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU Usage|Percent of the host processing power being consumed.|Dynatrace|
|Memory Usage|Percent of memory the host is using.|Dynatrace|
|Requests|Rate of requests per second|Dynatrace|
|Throughput|Size of requests, in megabytes per second|Dynatrace|
|Latency|Aggregate duration of transactions, in milliseconds.|Dynatrace|
|All Active Servers|Information for all hosts the service is actively using. Select a host link to view more detailed information.|CMDB|

## Database dashboards

These dashboards display metrics for databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the database's processing power being consumed.|Dynatrace|
|Memory utilization|Percent of memory the database is using.|Dynatrace|
|Availability|Percent of time the database is available.|Dynatrace|
|Connections|Number of connections to the database.|Dynatrace|
|Slow queries|Number of database queries that have been categorized as slow by the APM.|Dynatrace|
|All MySQL Instances|Information for all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Scheduled Checkpoints|Average number of scheduled checkpoints that were performed.|Dynatrace|
|Buffers Written for Checkpoint|Average number of buffers written during checkpoints.|Dynatrace|
|Buffers Written by Background Writer|Average number of buffers written by the background writer.|Dynatrace|
|Buffers Allocated|Average number of buffers allocated.|Dynatrace|
|Checkpoint Write Time|Time in milliseconds spent writing files to disk.|Dynatrace|
|All PostgreSQL Instances|Information of all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[Dynatrace templates for Service Observability](dynatrace-templates.md)

