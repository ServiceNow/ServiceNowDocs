---
title: LogicMonitor Overview tab for Service Observability
description: Information that is displayed on the LogicMonitor Overview tab of the Service Details page in the SOW.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [LogicMonitor templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# LogicMonitor Overview tab for Service Observability

Information that is displayed on the LogicMonitor **Overview** tab of the Service Details page in the SOW.

## KPIs section

The KPIs section displays basic performance metrics for the service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart name|Description|Data source|
|----------|-----------|-----------|
|Response Time|Response time metrics for the service, displayed in milliseconds over time.|LogicMonitor|
|Status|Status metrics for the service. A value of `1` means the service is up. A value of `2` means it's down.|LogicMonitor|

## Contextual information section

The Recent changes table shows changes made to the system that might have an impact on the service. This data comes from the related configuration items in the CMDB.

## Status indicators section

The Status indicators section displays charts for related CIs that might be affecting the service.

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

Current open alerts

</td><td>

Listing of active alerts that affect this service.

</td><td>

CMDB

</td></tr></tbody>
</table>**Parent Topic:**[LogicMonitor templates for Service Observability](logic-monitor-templates.md)

