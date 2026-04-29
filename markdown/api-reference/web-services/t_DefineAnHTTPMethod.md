---
title: Define a REST message HTTP method
description: Define an HTTP method such as GET or POST to send a request to a web service provider.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a message, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Define a REST message HTTP method

Define an HTTP method such as GET or POST to send a request to a web service provider.

## Before you begin

Role required: web\_service\_admin

## About this task

When you create a REST message record, several default HTTP methods are automatically created using settings inherited from the REST message record, such as the **Endpoint**. Subsequent changes to the REST message record are not applied to the HTTP methods automatically. You can create additional HTTP methods or modify the default HTTP methods to implement new behavior.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Select a REST message you want to define an HTTP method for.

3.  In the **HTTP Methods** related list, click **New**.

4.  Select the **HTTP method** you want to use, such as GET or POST.

5.  Enter the **Endpoint** this HTTP method should access.

    The endpoint value may include variables using the format **$\{variable\}**.

6.  Right-click the form header and select **Save**.


## What to do next

After creating the HTTP method, you can override the security settings from the parent REST message, configure HTTP headers, add variables, or test the method. For PUT, POST, and PATCH methods you can define a message body.

-   **[Testing REST message HTTP methods](../concept/c_TestingMethods.md)**  
Test an HTTP method for an outbound REST message to ensure that the request is valid and the response returns as expected.

**Parent Topic:**[Create a REST message](t_ConfiguringARESTMessage.md)

