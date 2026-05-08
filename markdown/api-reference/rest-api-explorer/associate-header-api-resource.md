---
title: Associate a request header with a resource
description: Define which request headers are expected for each resource within a scripted REST API.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Associate a request header with a resource

Define which request headers are expected for each resource within a scripted REST API.

## Before you begin

A REST API resource and a request header must already be defined within the scripted REST API.

Role required: web\_service\_admin

## About this task

The following procedure describes the process for manually associating a REST API request header with a resource. For details about automatically generating request header definitions in non-production instances, see [Automatically generate API request definitions](autogenerate-api-request-definitions.md).

## Procedure

1.  Create a Scripted REST Header Association record in one of the following ways

<table id="choicetable_fv4_myc_j3c"><thead><tr><th align="left" id="d311168e67">

Option

</th><th align="left" id="d311168e70">

Procedure

</th></tr></thead><tbody><tr><td id="d311168e76">

**Navigate through a scripted REST API record**

</td><td>

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.
2.  Select a scripted REST API record.
3.  In the **Resources** related list, select a resource.
4.  In the **Request Header Associations** tab, select **New**.


</td></tr><tr><td id="d311168e121">

**Navigate directly to a new Scripted REST Header Association record**

</td><td>

Navigate to **All** &gt; **Filter** and enter `sys_ws_header_map.form`.

</td></tr></tbody>
</table>2.  In the **API request header** field, select or enter the request header to associate with the resource.

3.  In the **API resource** field, select or enter the API resource the request header should be associated with.

    If you navigated to a new Scripted REST Header Association record through a scripted REST API record, **API resource** is pre-populated.

4.  Select **Submit**.


## Result

The request headers that you added are included in the exportable OpenAPI specification in the REST API Explorer with a "type: string" schema definition. For more information about exporting OpenAPI specifications, see [Export to OpenAPI specification](../../inbound-rest/task/export-openapi-specification.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

