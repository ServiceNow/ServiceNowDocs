---
title: Define a scripted REST API request header
description: Define scripted REST API request headers to control which headers the API accepts.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a scripted REST API, Scripted REST APIs, REST APIs, Web services, API implementation, API implementation and reference]
---

# Define a scripted REST API request header

Define scripted REST API requestheaders to control which headers the API accepts.

## Before you begin

There must be a scripted REST API defined before you can create requestheaders.

Role required: web\_service\_admin

## About this task

The following procedure describes the process for manual definition of a scripted REST API request header. For details about automatically generating request header definitions in non-production instances, see [Automatically generate API request definitions](autogenerate-api-request-definitions.md).

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Select a scripted REST API record.

3.  In the **Request Headers** related list, select **New**.

4.  Enter a **Header name**.

5.  Enter a **Short description** and **Example value** to explain how to use the header.

6.  Select **Submit**.

7.  From the Request Headers tab, locate the header name and set **Is required** to "true" to document this request header as required.

    **Note:** If you set **Is required** to "true", the scripted REST service doesn't enforce requiring the header. To enforce requiring a header, you must add logic to the scripted REST API resource that rejects requests that are missing the required headers.


## What to do next

After defining available headers, associate the headers with a scripted REST resource. For more information, see [Associate a request header with a resource](associate-header-api-resource.md).

**Parent Topic:**[Create a scripted REST API](t_CreateAScriptedRESTService.md)

