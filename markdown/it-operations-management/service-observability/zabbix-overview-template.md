---
title: Zabbix Overview tab for Service Observability
description: Information that is displayed on the Zabbix Overview tab of the Service Details page in the SOW.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2026-01-30"
reading_time_minutes: 1
breadcrumb: [Zabbix templates, Service Observability templates, Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Zabbix Overview tab for Service Observability

Information that is displayed on the Zabbix **Overview** tab of the Service Details page in the SOW.

## KPIs section

The KPIs section displays basic performance metrics for the service.

**Note:** If the dashboards have been customized, they might not reflect the information shown on this page.

|Chart name|Description|Data source|
|----------|-----------|-----------|
|CPU Usage \(System\)|Displays the system CPU usage percentage over time.|Zabbix|
|CPU Load|Shows the CPU load average for the system.|Zabbix|
|Running Processes|Number of processes currently running on the system.|Zabbix|
|Available Memory \(%\)|Percentage of memory currently available on the system.|Zabbix|

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
</table>**Parent Topic:**[Zabbix templates](zabbix-templates.md)

