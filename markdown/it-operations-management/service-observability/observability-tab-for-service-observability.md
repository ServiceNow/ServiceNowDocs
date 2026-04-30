---
title: Dynatrace Observability tab for Service Observability
description: Dashboard and charts on the Dynatrace Observability tab of the Service Details page in the SOW.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Dynatrace templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Dynatrace Observability tab for Service Observability

Dashboard and charts on the Dynatrace Observability tab of the Service Details page in the SOW.

Dynatrace dashboards are the same for both managed and SaaS environments.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

<table id="table_avw_x53_zdc"><thead><tr><th>

Chart

</th><th>

Description

</th><th>

Data source

</th></tr></thead><tbody><tr><td>

Rate

</td><td>

Aggregate rate of transactions through the service.

</td><td>

Dynatrace

</td></tr><tr><td>

Error %

</td><td>

Percent of transactions that have an error.

</td><td>

Dynatrace

</td></tr><tr><td>

Latency

</td><td>

Aggregate duration of transactions through the service, in milliseconds.

</td><td>

Dynatrace

</td></tr><tr><td>

Client error rate

</td><td>

Rate of errors the service clients experienced.

</td><td>

Dynatrace

</td></tr><tr><td>

Client throughput

</td><td>

Rate of client requests for this service.

</td><td>

Dynatrace

</td></tr><tr><td>

Client response time

</td><td>

Response time for client requests on this service, in milliseconds.

</td><td>

Dynatrace

</td></tr><tr><td>

Total DB connections

</td><td>

Number of databases that this client has connections to.**Note:** Not available with Grail \(DQL\) queries.

</td><td>

Dynatrace

</td></tr><tr><td>

DB connection errors

</td><td>

Number of errors received by the client when trying to access databases.**Note:** Not available with Grail \(DQL\) queries.

</td><td>

Dynatrace

</td></tr><tr><td>

Time spent in database calls

</td><td>

Duration of requests to databases, in milliseconds.**Note:** Not available with Grail \(DQL\) queries.

</td><td>

Dynatrace

</td></tr></tbody>
</table>|Chart|Description|Data source|
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
|Network RX - bytes received|Count of bytes received.|Dynatrace|
|Network TX - bytes transferred|Count of bytes sent.|Dynatrace|
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
|Slow queries|Number of database queries that have been categorized as slow by Dynatrace.|Dynatrace|
|All MySQL Instances|Information for all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Deadlocks|Number of deadlocks detected in this database.|Dynatrace|
|Committed Transactions|Number of transactions in this database that have been committed.|Dynatrace|
|Active Backend Connections|Number of backends currently connected to this database.|Dynatrace|
|Query Conflicts|Number of queries cancelled due to conflicts with recovery in this database.|Dynatrace|
|Active Time|Time spent executing SQL statements in this database.|Dynatrace|
|Fatal Sessions|Number of database sessions to this database that were terminated by fatal errors|Dynatrace|
|All PostgreSQL Instances|Information of all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[Dynatrace templates for Service Observability](dynatrace-templates.md)

