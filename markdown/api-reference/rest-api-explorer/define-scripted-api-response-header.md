---
title: Define a REST API response header
description: Define one or more REST API response headers in a REST API.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Define a REST API response header

Define one or more REST API response headers in a REST API.

## Before you begin

Role required: web\_service\_admin

## Procedure

1.  Create a REST response header in one of the following ways.

<table id="choicetable_rv3_mwc_j3c"><thead><tr><th align="left" id="d234118e60">

Option

</th><th align="left" id="d234118e63">

Procedure

</th></tr></thead><tbody><tr><td id="d234118e69">

**Create a response header from a REST API**

</td><td>

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.
2.  Select a scripted REST API record.
3.  In the **Response Headers** related list, select **New**.


</td></tr><tr><td id="d234118e108">

**Create a response header and associate it with a REST API**

</td><td>

Navigate to **All** &gt; **Filter** and enter `sys_ws_response_header.form`.1.  Enter `sys_ws_response_header.form` in the filter navigator.
2.  In the **API** field, select or enter the API to associate with the response header.


</td></tr></tbody>
</table>2.  In the **Header Name** field, add the name of the new header.

3.  In the **Example value** field, enter an example of a valid header value.

4.  Select **Submit**.

5.  Repeat these steps for each response header that you want to define.


## Result

The response headers that you added are included in the exportable OpenAPI specification in the REST API Explorer with a `type: string` schema definition. For more information about exporting OpenAPI specifications, see [Export to OpenAPI specification](../../inbound-rest/task/export-openapi-specification.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

