---
title: Azure Monitor Overview tab for Service Observability
description: Information that is displayed on the Azure Monitor Overview tab of the Service Details page in the SOW.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Azure Monitor templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Azure Monitor Overview tab for Service Observability

Information that is displayed on the Azure Monitor **Overview** tab of the Service Details page in the SOW.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart name|Description|Data source|
|----------|-----------|-----------|
|Requests|Aggregate rate of transactions through the service.|Azure|
|Response Time|Aggregate duration of transactions through the service, in milliseconds.|Azure|
|Http 5xx|Number of errors returned with a status of 5xx.|Azure|

## Contextual information section

The Recent changes table shows changes made to the system that might have an impact on the service. This data comes from the related configuration items in the CMDB.

## Status indicators section

The Status indicators section displays charts for related Configuration Items \(CIs\) that might be affecting the service.

<table id="table_bjg_j3b_zdc"><thead><tr><th>

Chart name

</th><th>

Description

</th><th>

Data source

</th></tr></thead><tbody><tr><td>

SLO Error Budget

</td><td>

Information about your current error budget for this service, as configured in Service Reliability Management \(SRM\).For more information on error budgets, see [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md).

</td><td>

CMDB

</td></tr><tr><td>

Systems impacted

</td><td>

Services or service offerings that have a relationship to the selected service.

</td><td>

CMDB

</td></tr><tr><td>

Open incidents last 30 days

</td><td>

Day-by-day occurrence of open incidents affecting this service over the last month.

</td><td>

CMDB

</td></tr><tr><td>

Open alerts last 30 days

</td><td>

Day-by-day occurrence of alerts affecting this service over the last month.

</td><td>

CMDB

</td></tr><tr><td>

Current open incidents

</td><td>

Listing of active incidents that affect this service.

</td><td>

CMDB

</td></tr><tr><td>

All Active alerts

</td><td>

Listing of active alerts that affect this service.

</td><td>

CMDB

</td></tr></tbody>
</table>**Parent Topic:**[Azure Monitor templates for Service Observability](azure-templates.md)

