---
title: Automatically generate API request definitions
description: Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 2
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Automatically generate API request definitions

Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource.

## Before you begin

An instance admin must set the system property **glide.rest.sampling.enabled** to true. To limit the likelihood of performance problems, only enable automatic generation of API request definitions in non-production instances.

Role required: web\_service\_admin

## Procedure

1.  Create a scripted REST API request sampling configuration in one of the following ways.

<table id="choicetable_rjy_kf1_s3c"><thead><tr><th align="left" id="d963056e66">

Option

</th><th align="left" id="d963056e69">

Procedure

</th></tr></thead><tbody><tr><td id="d963056e75">

**Navigate through a scripted REST API record**

</td><td>

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST Services** &gt; **Scripted REST APIs**.
2.  Select a scripted REST API record.
3.  In the **Resources** related list, select a resource.
4.  In the **Request Sampling Configuration** tab, select **New**.


</td></tr><tr><td id="d963056e123">

**Navigate directly to a new scripted REST API request sampling configuration**

</td><td>

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST Sampling Configurations**.
2.  Select **New**.
3.  In the **Rest resource** field, select or enter the scripted REST resource to automatically generate request definitions for.


</td></tr></tbody>
</table>2.  In the **Max samples** field, enter the number of sample requests to analyze for automatic definition generation.

    You must enter a number from 1 through 1000.

3.  Select **Submit**.

    Requests made to the resource are sampled for analysis, up to the number of samples you set in step 5. After the maximum number of samples is reached, the request sampling configuration state is set to **analyzed** and REST request staging schemas are available for review.

    You can select **Complete Sampling** from the request sampling configuration record to end sampling before the maximum number of samples has been reached.

4.  After sampling ends, return to the request sampling configuration you created by selecting its number from the **Request Sampling Configuration** tab of the scripted REST resource.

5.  Select a record from the **REST Request Staging Schemas** list to review and edit the automatically generated request definitions in the **Headers**, **Body**, and **Query parameters** fields.

    **Body** structure is only generated for **PUT** and **POST** HTTP methods.

6.  Select **Commit** to add the definitions to the scripted REST API resource and its associated scripted REST API service.


## Result

-   The committed REST request staging schema and the samples requests are deleted.
-   **Headers** field content is used to create the resource's request header associations. The associated request headers are added to the relevant REST service's **Request Headers** tab.
-   **Body** field content is used to create the resource's request schema. The resource's request schema is added to the relevant REST service's **Schemas** tab.
-   **Query parameters** field content is used to create the resource's query parameter associations. The associated query parameters are added to the relevant REST service's **Query Parameters** tab.
-   All committed request definitions that you added are included in the exportable OpenAPI specification in the REST API Explorer. For more information about exporting OpenAPI specifications, see [Export to OpenAPI specification](../../inbound-rest/task/export-openapi-specification.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

