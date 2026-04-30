---
title: Collect analytics for an API
description: Select which APIs to collect analytics for and select if requestor information should be collected for each API.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Analyze REST and SOAP API usage, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Collect analytics for an API

Select which APIs to collect analytics for and select if requestor information should be collected for each API.

## Before you begin

**Note:** API analytics is not available for certain APIs used for internal platform functionality, such as the UI and Mobile app APIs.

Role required: api\_analytics\_read or admin

## About this task

When a new API is added, an inclusion list record is created automatically. You can modify or create new inclusion list records to manually configure which APIs and requestor information are logged.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Inclusion List** and create a new record.

<table id="table_zvk_rjz_qw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

API name

</td><td>

For REST APIs, enter the API name. This name should contain only the namespace and ID of the API. Do not include any request parameters in the API name.For example, for the Table API endpoints `api/now/table/incident`and `api/now/table/problem`, the namespace and ID are **now/table**.

 SOAP APIs do not support separate logging configurations for different APIs. You can configure logging for all SOAP APIs by modifying the SOAP APIs inclusion list record.

</td></tr><tr><td>

Collect API stats

</td><td>

Select this check box to track analytics for the specified API.

</td></tr><tr><td>

Collect API requestor stats

</td><td>

Select this check box to track which users make requests to this API. This option is available only if **Collect API stats** is selected.

</td></tr></tbody>
</table>
**Parent Topic:**[Analyze REST and SOAP API usage](../concept/c_APIAnalytics.md)

