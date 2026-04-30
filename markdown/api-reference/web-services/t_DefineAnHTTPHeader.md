---
title: Define a REST message HTTP header
description: Define an HTTP header for a REST message or HTTP method to send that header with REST requests.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a message, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Define a REST message HTTP header

Define an HTTP header for a REST message or HTTP method to send that header with REST requests.

## Before you begin

Role required: web\_service\_admin

## About this task

You can specify an HTTP header for a REST message, or for an HTTP method. Headers defined for a REST message apply to all HTTP methods for that REST message. If you specify the same header for both a REST message and a child HTTP method, the value defined for the HTTP method overrides the value from the parent REST message.

**Note:** Multipart Content-Type is not supported in RESTMessageV2. You can use REST Step on IntegrationHub instead.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST Message**.

2.  Select a REST message.

3.  To specify a header for an HTTP method instead of the REST message, in the **HTTP Method** related list, select an HTTP method.

4.  Select the **HTTP Request** tab.

5.  In the **HTTP Headers** embedded list, click **Insert a new row**.

6.  Enter the name of the header, such as Content-Type or Accept.

    **Note:**

    -   Multipart Content-Type is not supported in RESTMessageV2. You can use REST Step on IntegrationHub instead.
    -   For other supported headers, it depends on the REST web service provider that you're connecting. Refer to the documentation of your web service provider to identify which headers are valid or required.
7.  Click on the **Value** field for the new row and enter the value you want to assign this header.

    You can use a variable in the format $\{variable\} instead of a static value. You can assign a value to the variable when sending a REST request.

8.  Click **Update**.


**Parent Topic:**[Create a REST message](t_ConfiguringARESTMessage.md)

