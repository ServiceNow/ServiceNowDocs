---
title: SolarWinds Observability tab for Service Observability
description: Dashboard and charts on the SolarWinds Observability tab of the Service Details page in the SOW.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SolarWinds templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# SolarWinds Observability tab for Service Observability

Dashboard and charts on the SolarWinds Observability tab of the Service Details page in the SOW.

**Note:** The X axis on SolarWinds charts use Universal Time Code \(UTC\) instead of the user's timezone.

## Application dashboard

This dashboard displays performance metrics for the selected service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart|Description|Data source|
|-----|-----------|-----------|
|Rate|Aggregate rate of transactions through the service, per minute.|SolarWinds|
|Latency|Aggregate duration of transactions through the service, in milliseconds.|SolarWinds|
|Time spent in database calls|Duration of requests to databases, in milliseconds.|SolarWinds|
|Time spent in database queries|Time spent querying the database, in milliseconds.|SolarWinds|
|Database throughput|Rate of database requests for this service per minute.|SolarWinds|

## Compute dashboard

This dashboard displays metrics for hosts related to the service.

|Chart|Description|Data source|
|-----|-----------|-----------|
|CPU utilization|Percent of the host processing power being consumed.|SolarWinds|
|Memory utilization|Percent of memory the host is using.|SolarWinds|
|Disk utilization|Percent of disk space being used.|SolarWinds|
|All Active Servers|Information for all hosts the service is actively using. Select a host link to view more detailed information.|CMDB|
|All Active VM Instances|Information for all virtual machine instances the service is actively using. Select a VM link to view more detailed information.|CMDB|

## Database dashboards

Database metrics are currently not supported for SolarWinds.

**Parent Topic:**[SolarWinds templates for Service Observability](solarwinds-templates.md)

