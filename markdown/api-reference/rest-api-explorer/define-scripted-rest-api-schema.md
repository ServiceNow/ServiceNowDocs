---
title: Define a REST API schema
description: Specify the expected data structure for requests or responses within a REST API by defining a schema.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Define a REST API schema

Specify the expected data structure for requests or responses within a REST API by defining a schema.

## Before you begin

Role required: web\_service\_admin

## About this task

Schemas are records that define the structure and format of request and response bodies and headers for a REST API in the OpenAPI 3.0.1 format. When you define a schema in the ServiceNow AI Platform, the schema is used to define the structure of requests and responses within the associated REST API. The schema data for the requests and responses is then available in the exportable OpenAPI specification for the API. For more information about exporting OpenAPI specifications, see [Export to OpenAPI specification](../../inbound-rest/task/export-openapi-specification.md).

The following procedure describes the process for manual schema definition. For details about automatically generating request schema definitions in non-production instances, see [Automatically generate API request definitions](autogenerate-api-request-definitions.md).

## Procedure

1.  Create a REST Schema in one of the following ways.

<table id="choicetable_kbq_szc_j3c"><thead><tr><th align="left" id="d352061e89">

Option

</th><th align="left" id="d352061e92">

Procedure

</th></tr></thead><tbody><tr><td id="d352061e98">

**Navigate through a scripted REST API record**

</td><td>

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.
2.  Select a scripted REST API record.
3.  In the **Schemas** related list, select **New**.


</td></tr><tr><td id="d352061e137">

**Navigate directly to a new REST Schema record**

</td><td>

1.  Navigate to **All** &gt; **Filter** and enter `sys_ws_schema.form`.
2.  In the **API** field, select or enter the API to associate with the schema.


</td></tr></tbody>
</table>2.  In the **Name** field, enter a name for the schema.

3.  In the **Schema** field, define the data type and structure of the new schema using the [OpenAPI version 3.0.1 format](https://spec.openapis.org/oas/v3.0.1.html).

    For example, the following entry specifies that the schema is an object that contains a first name. The first name is a string data type.

    ```
    { "type": "object", "properties": { "firstName": { "type": "string" } } }
    ```

4.  Select an **OpenAPI version**.

5.  In the **Description** field, summarize the expected structure of the new schema.

6.  Select **Submit**.


## What to do next

Define additional schemas as needed. Use the schemas to specify the expected structure and format in a REST request or response. For more information, see [Define an API resource request structure](add-schema-rest-api-request.md) or [Define an API resource response structure](add-schema-rest-api-response.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

