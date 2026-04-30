---
title: Create a scripted REST API
description: Create a scripted REST API to define web service endpoints.
locale: en-US
release: yokohama
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Create a scripted REST API

Create a scripted REST API to define web service endpoints.

## Before you begin

Role required: web\_service\_admin

## About this task

By default, scripted REST APIs contain an ACL that prohibits users with the snc\_external role from making requests to the API.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Click **New**.

3.  Enter a **Name** for the service.

    The **API ID** is set automatically based on the **Name**. You can modify the **API ID** if needed.

4.  Click **Submit**.


## What to do next

After you create the API, configure the service as needed such as by creating resources, assigning ACLs, or specifying supported request and response formats.

-   **[Create a scripted REST API resource](t_CreateAScriptedRESTAPIResource.md)**  
Create a scripted REST API resource to define the HTTP method, the processing script, and to override settings from the parent service.
-   **[Define scripted REST API headers](t_DefineRESTServiceHeaders.md)**  
Define scripted REST API headers to control which headers the API acceptsand can respond with.
-   **[Associate a request header with a resource](associate-header-api-resource.md)**  
Define which request headers are expected for each resource within a scripted REST API.
-   **[Define available query parameters](t_DefineAvailableQueryParameters.md)**  
Define available query parameters to control what values a requesting user can pass in the request URI.
-   **[Associate query parameters with a resource](AssocQueryParmResource.md)**  
Associate scripted REST API query parameters with a resource.
-   **[Configure a scripted REST API to require an ACL](t_WbSvcRqACL.md)**  
Requests to scripted REST APIs respect platform ACLs, and the requesting user must meet any table ACL requirements to access instance data. Additionally, you can configure the scripted REST API to require a specific ACL.
-   **[Enable versioning for a scripted REST API](t_EnableVersioning.md)**  
Enable versioning for a scripted REST API to provide multiple versions of the API while maintaining compatibility with existing integrations.
-   **[Control request and response content type](../concept/c_SpecifyContentType.md)**  
Controls which content types are allowed in scripted REST API requests and responses.
-   **[Controlling maximum request size](../reference/r_ControllingMaxRequestSize.md)**  
You can specify the maximum file size allowed in a scripted REST API request payload.

**Parent Topic:**[Scripted REST APIs](../concept/c_CustomWebServices.md)

