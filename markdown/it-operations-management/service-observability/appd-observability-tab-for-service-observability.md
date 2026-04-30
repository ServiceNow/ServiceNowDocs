---
title: AppDynamics Observability tab for Service Observability
description: Dashboard and charts on the AppDynamics Observability tab of the Service Details page in the SOW.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [AppDynamics templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# AppDynamics Observability tab for Service Observability

Dashboard and charts on the AppDynamics Observability tab of the Service Details page in the SOW.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart name|Description|Data source|
|----------|-----------|-----------|
|Average Response Time|Average rate of transactions through the service.|AppDynamics|
|Errors per Minute|Rate of errors per minute on transactions for the service.|AppDynamics|
|Calls per Minute|Number of calls to the server, per minute.|AppDynamics|
|Number of slow calls|Number of calls to the server that have a response time slower than the set slow threshold.|AppDynamics|
|Number of Very Slow Calls|Number of calls to the server that have a response time slower than the set very slow threshold.|AppDynamics|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU %Busy|Percent of the host processing power being consumed.|AppDynamics|
|Memory Used %|Percent of memory the host is using.|AppDynamics|
|Disk Reads/sec|Percent of disk space being used, per second.|AppDynamics|
|Disk Writes/sec|Percent of disk space being written to, per second.|AppDynamics|
|Network Incoming KB/sec|Number of kilobytes coming into the service, per second.|AppDynamics|
|Network Outgoing KB/sec|Number of kilobytes being sent by the service, per second.|AppDynamics|
|All Active Servers|Information for all servers the service is actively using. Select a host link to view more detailed information.|CMDB|

## Database dashboards

These dashboards display metrics for databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Calls Per Minute|Number of database calls made by the service, per minute|AppDynamics|
|Time Spent in Executions|Number of seconds spent executing database calls by the service.|AppDynamics|
|DB Inserts|Number of database inserts by the service.|AppDynamics|
|DB Reads|Number of database reads by the service.|AppDynamics|
|All MySQL Instances|Information for all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Calls Per Minute|Number of database calls made by the service, per minute|AppDynamics|
|Time Spent in Execution\(s\)|Time in seconds the database in execution mode for this service.|AppDynamics|
|All PostgreSQL Instances|Information of all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[AppDynamics templates for Service Observability](appd-templates.md)

