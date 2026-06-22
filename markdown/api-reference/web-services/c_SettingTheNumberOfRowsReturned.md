---
title: Setting the number of rows returned
description: The following system property controls how many rows JSON returns with each query.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/api-reference/web-services/c\_SettingTheNumberOfRowsReturned.html
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [JSONv2 web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Setting the number of rows returned

The following system property controls how many rows JSON returns with each query.

<table id="table_ez1_q1j_bp"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.processor.json.row\_limit

</td><td>

Specify the maximum number of rows a JSON query returns.-   Type: Integer
-   Default value: 10,000
-   Location: [Add glide.processor.json.row\_limit to the system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md) `[sys_properties]` table

</td></tr></tbody>
</table>**Parent Topic:**[JSONv2 web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/api-reference/web-services/c_JSONv2WebService.md)

