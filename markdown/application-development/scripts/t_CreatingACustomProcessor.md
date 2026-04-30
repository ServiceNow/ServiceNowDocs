---
title: Create a custom processor
description: Create a custom processor to execute a script from a URL query. This feature is deprecated.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Processors, Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Create a custom processor

Create a custom processor to execute a script from a URL query. This feature is deprecated.

## Before you begin

Role required: admin

## About this task

**Note:** This feature is deprecated. While legacy, existing custom processors continue to be supported, creating new custom processors has been deprecated. Instead, use the [Scripted REST APIs](https://www.servicenow.com/docs/access?context=c_CustomWebServices&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

When complete, you can do the following tasks:

-   Create a new processor
-   Run a script from a URL query

The following example steps assume you have your own demonstration instance.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Processors**.

2.  Select **New**.

3.  In the **Name** field, enter `Hello`.

4.  In the **Type** field, select script.

5.  In the **Path** field, enter `Hello`.

6.  In the **Script** field, enter the following code.

    ```
    var name = g_request.getParameter("name");
    g_processor.writeOutput("text/plain", "Hello " + name);
    ```

7.  Select **Submit**.

8.  Log out of the instance and open a new browser window.

9.  Enter a URL query to the instance with the following format: `https://instance.service-now.com/processor_name.do?parameter=value`.

    For example: `https://<instance name>.service-now.com/Hello.do?name=world`.

10. When prompted, enter the credentials for a valid user.


**Parent Topic:**[Processors](../../processors/concept/c_Processors.md)

