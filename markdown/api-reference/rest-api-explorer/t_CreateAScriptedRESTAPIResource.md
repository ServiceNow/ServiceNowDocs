---
title: Create a scripted REST API resource
description: Create a scripted REST API resource to define the HTTP method, the processing script, and to override settings from the parent service.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Create a scripted REST API resource

Create a scripted REST API resource to define the HTTP method, the processing script, and to override settings from the parent service.

## Before you begin

Create a scripted REST API. For more information, see [Create a scripted REST API](t_CreateAScriptedRESTService.md).

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Select a scripted REST API record.

3.  In the **Resources** related list, click **New**.

4.  Enter a **Name**.

    The resource name affects the URI for sending requests to the API.

5.  Select the **HTTP method** this resource implements, such as **GET**.

6.  In the **Script** field, define how the operation parses and responds to requests.

7.  Override settings from the parent REST API as needed, such as by specifying different security settings or valid content types.

8.  On the **Documentation** tab, provide a **Short description** explaining how to access the resource.

    This information appears when exploring this resource using the REST API Explorer.

9.  Click **Submit**.


## What to do next

After creating the resource, you can associate headers and query parameters. For details, see [Define scripted REST API headers](t_DefineRESTServiceHeaders.md) and [Define available query parameters](t_DefineAvailableQueryParameters.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

