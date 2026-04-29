---
title: Chart error states
description: Understand the different error states that the charts in Service Observability might display and how to fix them.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Chart error states

Understand the different error states that the charts in Service Observability might display and how to fix them.

|Error message|Fix|
|-------------|---|
|Set up this service's observability data mapping|Observability mapping hasn't been configured for the service by an admin. See [Create and manage data mappings](../task/create-and-manage-observability-data-mappings.md).|
|Data mapping is not configured|Observability mapping hasn't been configured for the service by an admin. See [Create and manage data mappings](../task/create-and-manage-observability-data-mappings.md).|
|Authentication failed|Service Observability can't connect to the data source. See [Connect a Service Observability data source](../task/connect-an-observability-data-source.md).|
|No results found|No metrics were found for the chart.|
|Something went wrong|Connection to the data source was successful, but the observability instance didn't respond. This error might be due to a connection timeout on the observability vendor side.|
|No impacted systems found \(Impacted systems chart on the Overview page\)|Only services found on your service map can be displayed. Update your service map to include all services that should be included in the chart. See [Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md).|
|Set up objectives \(SLO Error Budget chart on the Overview page\)|SLOs haven't been configured for Service Reliability Management. See [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md).|

**Parent Topic:**[Service Observability reference](service-observability-reference.md)

