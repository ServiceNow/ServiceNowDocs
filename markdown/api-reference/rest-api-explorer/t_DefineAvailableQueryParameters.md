---
title: Define available query parameters
description: Define available query parameters to control what values a requesting user can pass in the request URI.
locale: en-US
release: yokohama
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Define available query parameters

Define available query parameters to control what values a requesting user can pass in the request URI.

## Before you begin

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Select a scripted REST API record.

3.  In the **Query Parameters** related list, select **New**.

4.  Specify the **Query parameter name**.

5.  Enter a **Short description** and **Example value** to explain how to use the parameter.

6.  Select **Submit**.

7.  From the Query Parameters tab, locate the query parameter and set **Is required** to "true" to document this query parameter as required.

    **Note:** If you set **Is required** to "true", the scripted REST service doesn't enforce requiring the parameter. To enforce requiring a query parameter, you must add logic to the scripted REST API resource that rejects requests that are missing the required parameters.


## What to do next

After defining available query parameters, associate the parameters to a scripted REST resource. For details, see [Associate query parameters with a resource](AssocQueryParmResource.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

