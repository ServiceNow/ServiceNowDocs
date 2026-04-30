---
title: Splunk Observability tab for Service Observability
description: Dashboard and charts on the Splunk Observability tab of the Service Details page in the SOW.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Splunk templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Splunk Observability tab for Service Observability

Dashboard and charts on the Splunk Observability tab of the Service Details page in the SOW.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Rate|Aggregate rate of transactions through the service, per minute.|Splunk|
|Error %|Percent of transactions that have an error.|Splunk|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|Splunk|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Rate|Each line represents the throughput of a key transaction through the service. Hover over a point to view the different transaction names.|Splunk|
|Error %|Each line represents the percentage of errors on a key transaction in the service. Hover over a point to view the different transaction names.|Splunk|
|Latency|Each line represents the response time for a key transaction on the service. Hover over a point to view the different transaction names.|Splunk|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percentage of CPU currently being consumed by the service.|Splunk|
|Memory utilization|Percentage of memory currently being consumed by the service.|Splunk|
|Disk utilization|Percentage of disk space currently being consumed by the service.|Splunk|
|All Active Servers|Information for all hosts the service is actively using. Select a host link to view more detailed information.|CMDB|
|All Active VM Instances|Information for all VM instances the service is actively using. Select a host link to view more detailed information.|CMDB|

## Database Dashboards

These dashboards display metrics for databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Queries Per Second|Number of queries per second the service is sending to the database.|Splunk|
|Row Locks Rate|Frequency at which row locks are encountered by transactions from this service.|Splunk|
|Buffer Pool Usage|Usage of the buffer pool to access cached data by this service.|Splunk|
|Table I/O Wait Time|Time in milliseconds that the database is waiting on Input/Output operations on tables sent by this service to complete.|Splunk|
|Threads|Number of threads used by this service|Splunk|
|Uptime|Amount of time in \(?\) that the database has been running since its last restart.|CMDB|

**Parent Topic:**[Splunk templates for Service Observability](splunk-templates.md)

