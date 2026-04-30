---
title: Define an API resource request structure
description: Add a schema to a REST request record to define the request's expected data structure.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-02-20"
reading_time_minutes: 1
breadcrumb: [Create, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Define an API resource request structure

Add a schema to a REST request record to define the request's expected data structure.

## Before you begin

You must define at least one REST API resource and at least one schema in the REST API before defining the request structure.

Role required: web\_service\_admin

## About this task

The following procedure describes the process for manually adding a request schema to a resource. For details about automatically generating request schema definitions in non-production instances, see [Automatically generate API request definitions](autogenerate-api-request-definitions.md).

## Procedure

1.  Navigate to a new REST Request record in one of the following ways.

    If you navigate through a scripted REST API record, most fields in the REST Request record are pre-populated.

<table id="choicetable_ehs_g3d_j3c"><thead><tr><th align="left" id="d450878e70">

Option

</th><th align="left" id="d450878e73">

Procedure

</th></tr></thead><tbody><tr><td id="d450878e79">

**Navigate through a scripted REST API record**

</td><td>

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST Services** &gt; **Scripted REST APIs**.
2.  Select a scripted REST API record.
3.  In the **Resources** related list, select a resource.
4.  In the **Request Schema** tab, select **New**.


</td></tr><tr><td id="d450878e127">

**Navigate directly to a new REST Request record**

</td><td>

1.  Navigate to **All** &gt; **Filter** and enter `sys_ws_request_spec.form`.
2.  In the **API** field, select an API.
3.  In the **API resource** field, select the API resource whose request schema you want to specify.
4.  In the **Version** field, select the API resource version.
5.  In the **Http method** field, select the method whose request schema you want to specify \(for example, PUT\).


</td></tr></tbody>
</table>2.  In the **Schema** field, find or enter the schema you want to define the structure and format of the resource's request body.

3.  In the **Description** field, summarize the expected format of the REST request.

4.  Select **Submit**.


## Result

The schema you used to define the request body structure is included in the exportable OpenAPI specification in the REST API Explorer. For more information about exporting OpenAPI specifications, see [Export to OpenAPI specification](../../inbound-rest/task/export-openapi-specification.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

