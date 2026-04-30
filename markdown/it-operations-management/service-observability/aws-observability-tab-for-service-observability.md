---
title: Amazon CloudWatch Observability tab for Service Observability
description: Dashboard and charts on the Amazon CloudWatch tab of the Service Details page in the SOW.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Amazon CloudWatch templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Amazon CloudWatch Observability tab for Service Observability

Dashboard and charts on the Amazon CloudWatch tab of the Service Details page in the SOW.

## Application dashboards

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Request Count|Aggregate rate of transactions through the service, per minute.|AWS|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|AWS|
|4xx Errors|Number of errors returned with a status of 4xx.|AWS|
|5xx Errors|Number of errors returned with a status of 5xx.|AWS|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Request Count|Aggregate rate of transactions through the service, per minute.|AWS|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|AWS|
|4xx Errors|Number of errors returned with a status of 4xx.|AWS|
|5xx Errors|Number of errors returned with a status of 5xx.|AWS|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Request Count|Aggregate rate of transactions through the service, per minute.|AWS|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|AWS|
|4xx Errors|Number of errors returned with a status of 4xx.|AWS|
|5xx Errors|Number of errors returned with a status of 5xx.|AWS|

|Chart|Description|Data source|
|-----|-----------|-----------|
|Errors|Number of errors reported by the Lambda function.|AWS|
|Duration|Aggregate duration of transactions through the service, in milliseconds.|AWS|
|Invocations|Number of Lambda invocations executed by this service.|AWS|

## Compute dashboards

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the host processing power being consumed by this service.|AWS|
|Disk Write Bytes|Number of bytes written to the database by this service.|AWS|
|Disk Read Bytes|Number of bytes read from the database by this service.|AWS|
|Network In Bytes|Amount of incoming network traffic in bytes for this service.|AWS|
|Network Out Bytes|Amount of outgoing network traffic in bytes for this service.|AWS|
|All EC2 VM Instances|Information for all EC2 VM instances the service is actively using. Select a link to view more detailed information.|CMDB|
|All Active Servers|Information for all servers the service is actively using. Select a Server link to view more detailed information.|CMDB|

## Database dashboards

This dashboard displays metrics for RDS databases related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the database's processing power being consumed by this service.|AWS|
|Free Memory|Amount of memory in bytes available on this database.|AWS|
|Free Storage|Amount of storage in bytes available on this database.|AWS|
|Current Connections|Number of connections from this service to the database.|AWS|
|Read Latency|Time taken in milliseconds for read operation from the database to complete.|AWS|
|Write Latency|Time taken in milliseconds for write operation from the database to complete.|AWS|
|All RDS Instances|Information for all databases the service is actively using. Select a database link to view more detailed information.|CMDB|

**Parent Topic:**[Amazon CloudWatch templates for Service Observability](aws-templates.md)

