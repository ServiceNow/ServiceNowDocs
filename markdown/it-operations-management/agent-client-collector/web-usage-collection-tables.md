---
title: Web usage data collection tables and fields
description: Description of the tables and their fields used when gathering web usage data from your Windows and macOS machines.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-26"
reading_time_minutes: 2
breadcrumb: [ACC-VC reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Web usage data collection tables and fields

Description of the tables and their fields used when gathering web usage data from your Windows and macOS machines.

|Name|Description|
|----|-----------|
|User Web Usage \(sn\_acc\_vis\_content\_user\_web\_usage\)|Stores per-user, per-device, per-domain web usage records, including page visit counts and data measured by each day.|
|Application Domain \(sn\_acc\_vis\_content\_application\_domain\)|Stores domain-level information. Updated with aggregated totals \(total page views, total users, daily trends\) by the daily aggregation job. Domains not previously configured are automatically created here when collected via full monitoring.|
|Application \(sn\_acc\_vis\_content\_application\)|Stores service application records that group one or more domains. Each application is linked to a CMDB service and a source.|

|Name|Description|
|----|-----------|
|Domain \(domain\)|The application domain of the visited website.|
|Device \(device\_id\)|The computer \(cmdb\_ci\_computer\) from which the website was accessed.|
|User \(user\)|User that accessed the website.|
|Last Accessed \(last\_accessed\)|Date and time that the website was last accessed.|
|Page Visits \(page\_visits\)|Number of page visits for the current user-domain-device combination.|
|Page Visits Daywise \(page\_visits\_daywise\)|A JSON object storing page visit counts, broken down by day for the retention period \(for example, \{"2026-03-15": "12", "2026-03-16": "8"\}\)|

<table id="table_unn_bkp_s3c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application \(application\)

</td><td>

Application record that the domain belongs to.

</td></tr><tr><td>

Domain \(domain\)

</td><td>

Domain name that can be monitored \(such as `example.com`\). The display field. Must be unique.

</td></tr><tr><td>

Category \(category\)

</td><td>

The URL category \(sn\_acc\_vis\_content\_url\_category\) for the domain.

</td></tr><tr><td>

Domain Type \(domain\_type\)

</td><td>

Indicates whether the domain is internal or external.Default: external

</td></tr><tr><td>

CMDB endpoint http \(endpoint\_http\)

</td><td>

The CMDB HTTP endpoint \(cmdb\_ci\_endpoint\_http\) for SaaS applications.

</td></tr><tr><td>

Metric monitoring \(monitored\)

</td><td>

Indicates whether the domain is monitored for metrics.Default: false

</td></tr><tr><td>

Total accessed time \(total\_accessed\_time\)

</td><td>

Total accumulated access duration for the domain.

</td></tr><tr><td>

Total users \(total\_users\)

</td><td>

Total number of unique users who accessed the domain. Updated by the daily aggregation job.

</td></tr><tr><td>

Last accessed time \(last\_accessed\_time\)

</td><td>

Date and time that the domain was last accessed.

</td></tr><tr><td>

Total page views \(total\_page\_views\)

</td><td>

Total number of page views for the domain. Updated by the daily aggregation job.

</td></tr><tr><td>

Total page views daywise \(total\_page\_views\_day\_wise\)

</td><td>

A JSON object storing total page view counts broken down by day \(for example, \{"2026-03-15": "120", "2026-03-16": "85"\}\). Updated by the daily aggregation job.

</td></tr></tbody>
</table><table id="table_scm_4lp_s3c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service \(ci\_id\)

</td><td>

The CMDB service \(cmdb\_ci\_service\) associated with the application. The display field.

</td></tr><tr><td>

SAMP product \(samp\_sw\_product\)

</td><td>

The Software Asset Management product \(samp\_sw\_product\) for the application.

</td></tr><tr><td>

Source \(source\)

</td><td>

The source \(sn\_acc\_vis\_content\_source\) that discovered or created the application.

</td></tr><tr><td>

Type \(type\)

</td><td>

Type of application: web or installedDefault: web

</td></tr><tr><td>

Metric monitoring \(monitored\)

</td><td>

Indicates whether the application is monitored for metrics. Read-only.Default: false

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector for Visibility - Content reference](../concept/agent-client-collector-for-visibility-references.md)

