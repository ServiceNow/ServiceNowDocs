---
title: Create a scripted REST API
description: Create a scripted REST API to define web service endpoints.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Create a scripted REST API

Create a scripted REST API to define web service endpoints.

## Before you begin

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Click **New**.

3.  Enter a **Name** for the service.

    The **API ID** is set automatically based on the **Name**. You can modify the **API ID** if needed.

4.  In the Default ACLs field, select the default ACLs that apply to all resources in the API.

    If you configure security settings for resources in the API, including ACLs, the settings of the resource override the parent API settings.

5.  Click **Submit**.


## What to do next

After you create the API, configure the service as needed such as by creating resources, assigning ACLs, or specifying supported request and response formats.

-   **[Create a scripted REST API resource](t_CreateAScriptedRESTAPIResource.md)**  
Create a scripted REST API resource to define the HTTP method, the processing script, and to override settings from the parent service.
-   **[Define a REST API response header](define-scripted-api-response-header.md)**  
Define one or more REST API response headers in a REST API.
-   **[Define a scripted REST API request header](t_DefineRESTServiceHeaders.md)**  
Define scripted REST API requestheaders to control which headers the API accepts.
-   **[Associate a request header with a resource](associate-header-api-resource.md)**  
Define which request headers are expected for each resource within a scripted REST API.
-   **[Define a REST API schema](define-scripted-rest-api-schema.md)**  
Specify the expected data structure for requests or responses within a REST API by defining a schema.
-   **[Define an API resource request structure](add-schema-rest-api-request.md)**  
Add a schema to a REST request record to define the request's expected data structure.
-   **[Define an API resource response structure](add-schema-rest-api-response.md)**  
Add a schema and relevant response headers to a REST response to define the response's expected data structure.
-   **[Define available query parameters](t_DefineAvailableQueryParameters.md)**  
Define available query parameters to control what values a requesting user can pass in the request URI.
-   **[Associate query parameters with a resource](AssocQueryParmResource.md)**  
Associate scripted REST API query parameters with a resource.
-   **[Automatically generate API request definitions](autogenerate-api-request-definitions.md)**  
Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource.
-   **[Configure a scripted REST API to require an ACL](t_WbSvcRqACL.md)**  
Requests to scripted REST APIs respect platform ACLs, and the requesting user must meet any table ACL requirements to access instance data. Additionally, you can configure the scripted REST API to require a specific ACL.
-   **[Enable versioning for a scripted REST API](t_EnableVersioning.md)**  
Enable versioning for a scripted REST API to provide multiple versions of the API while maintaining compatibility with existing integrations.
-   **[Control request and response content type](../concept/c_SpecifyContentType.md)**  
Controls which content types are allowed in scripted REST API requests and responses.
-   **[Controlling maximum request size](../reference/r_ControllingMaxRequestSize.md)**  
You can specify the maximum file size allowed in a scripted REST API request payload.

**Parent Topic:**[Scripted REST APIs](../concept/c_CustomWebServices.md)

