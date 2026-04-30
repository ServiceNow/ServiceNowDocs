---
title: Configure bot ID and AI assistant
description: Specify the bot ID to configure Moveworks AI assistant on Employee Center portal.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-01-06"
reading_time_minutes: 1
breadcrumb: [Moveworks for Employee Center, Configure, Employee Center, Employee Service Management]
---

# Configure bot ID and AI assistant

Specify the bot ID to configure Moveworks AI assistant on Employee Center portal.

## Before you begin

Ensure you have the appropriate entitlements for the application.

Role required: admin

## About this task

Ensure you copy the bot ID from **Moveworks** &gt; **Chat Platform** &gt; **Manage Chatbots**. For more information, see [Embedded AI Assistant Installation-ServiceNow](https://help.moveworks.com/docs/moveworks-for-web-installation-servicenow).

**Note:** You don't need to perform other steps or provide any REST API details.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Moveworks Assistant Setup**.

2.  Add **Bot ID** which can be found from the **Manage Chatbots** record from Moveworks.

    For detailed Bot ID instructions, see [Embedded AI Assistant Installation-ServiceNow](https://help.moveworks.com/docs/moveworks-for-web-installation-servicenow).

3.  Specify the initialization options in JSON format for Moveworks integration.

    ![Example for illustration purpose only, Embedded AI Assistant setup for Moveworks](../images/mw-embed-ai-botid.png "Example: Embedded AI Assistant setup for Moveworks")

4.  Click **Save configuration**.


## Result

The Moveworks application is ready for use. You can access the features and functionality per your role permissions.

## What to do next

You can perform the following actions:

-   Verify the Moveworks chatbot visibility from **All** &gt; **Self-Service** &gt; **Employee Center** portal. For more information, see [Use Moveworks on employee portal](../concept/mw-employee-chat-ui.md).
-   Test basic functionality by invoking the assistant and asking a sample question.
-   Check system properties and verify that all Moveworks-specific properties are configured properly.

**Parent Topic:**[Moveworks for Employee Center](../concept/moveworks-for-employeecenter.md)

**Related topics**  


[Getting started with Moveworks for Employee Center](../concept/moveworks-ec-getting-started.md)

[Install Moveworks for Employee Center app from store](mw-install-app.md)

[Upload Java KeyStore certificate](mw-upload-jks-cert.md)

[Use Moveworks on employee portal](../concept/mw-employee-chat-ui.md)

[Moveworks for Employee Center reference](../reference/mw-ec-integration-reference.md)

[Moveworks for Employee Center reference](../reference/mw-ec-integration-reference.md)

