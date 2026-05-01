---
title: Define an API resource response structure
description: Add a schema and relevant response headers to a REST response to define the response's expected data structure.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-02-20"
reading_time_minutes: 1
breadcrumb: [Create, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Define an API resource response structure

Add a schema and relevant response headers to a REST response to define the response's expected data structure.

## Before you begin

At least one REST API resource and at least one schema must already be defined for use in the relevant REST API. You must also define any response headers you want to use. For more information, see [Define a REST API response header](define-scripted-api-response-header.md).

Role required: web\_service\_admin

## Procedure

1.  Navigate to a new REST Response record in one of the following ways.

    If you navigate through the scripted REST API record, most fields in the REST Response record are pre-populated.

<table id="choicetable_mvh_34d_j3c"><thead><tr><th align="left" id="d702230e64">

Option

</th><th align="left" id="d702230e67">

Procedure

</th></tr></thead><tbody><tr><td id="d702230e73">

**Navigate through a scripted REST API record**

</td><td>

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST Services** &gt; **Scripted REST APIs**.
2.  Select a scripted REST API record.
3.  In the **Resources** related list, select a resource.
4.  In the **Response Schema** tab, select **New**.


</td></tr><tr><td id="d702230e121">

**Navigate directly to the REST Response record**

</td><td>

1.  Navigate to **All** &gt; **Filter** and enter `sys_ws_response_spec.form`.
2.  In the **API** field, select an API.
3.  In the **API resource** field, select the API resource whose response format you want to specify.
4.  In the **Http method** field, select the method whose response format you want to specify \(for example, GET\).
5.  **Version** field, select the API resource version.


</td></tr></tbody>
</table>2.  In the **Http status** field, enter the HTTP status that the REST response specifications apply to \(for example, 200\).

    For example, return ABC status by entering 200.

3.  In the **Schema** field, find or enter the schema that defines the structure and format for the resource's selected HTTP status, version, and method.

4.  Add relevant response headers associated with the API.

    1.  Select the Unlock Response Headers icon ![](../../../reuse/icons/product-icons/lock-outline-24.svg).

    2.  Find or enter relevant response headers associated with the API.

5.  In the **Description** field, summarize the expected format of the REST response.

6.  Select **Submit**.


## Result

The schema you used to define the response body structure is included in the exportable OpenAPI specification in the REST API Explorer. For more information about exporting OpenAPI specifications, see [Export to OpenAPI specification](../../inbound-rest/task/export-openapi-specification.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

