---
title: Application quota property
description: An administrator can add a system property to specify how often application quota rules are evaluated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/platform-performance/r\_AppQuotaProperty.html
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Platform performance reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Application quota property

An administrator can add a system property to specify how often application quota rules are evaluated.

<table id="table_awx_phf_z5"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.quota.manager.cluster.update.seconds

</td><td>

Indicates the application quota update period in seconds. If this value is less than the glide.quota.manager.heartbeat property, the glide.quota.manager.heartbeat value is used. Type: Number

 Default value: 300 \(5 minutes\)

 Location: [Add to the System Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md) `[sys_properties]` table

</td></tr></tbody>
</table>**Parent Topic:**[Platform performance reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/platform-performance/platform-performance-references.md)

