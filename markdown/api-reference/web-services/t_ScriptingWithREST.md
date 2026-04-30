---
title: Generate a REST message script preview
description: You can generate an example script to send a REST message based on content and parameters you provide in the method record.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scripting outbound REST, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Generate a REST message script preview

You can generate an example script to send a REST message based on content and parameters you provide in the method record.

## Before you begin

Role required: web\_service\_admin or admin

## About this task

Generate an example script and use it as a starting point when scripting outbound REST messages.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST Message**.

2.  Select a REST message record.

3.  In the **HTTP Methods** related list, select an HTTP method record.

4.  Ensure the HTTP method is configured as needed, including any variables.

5.  Save the record.

6.  In the Variable Substitutions related list, assign a value to each variable.

7.  Under Related Links, click **Preview script usage**.

    The instance displays the script that the REST message generated for this method.

    ![REST Message Script Preview](../image/RESTMessageScriptPreview.png)

8.  Copy this script and modify it as needed to use elsewhere in the instance.


## What to do next

Refer to the RESTMessageV2 and RESTResponseV2 APIs for more information on available scripting methods. Outbound REST scripting examples are also available.

**Parent Topic:**[Scripting outbound REST](../concept/c_ScriptingOutboundREST.md)

