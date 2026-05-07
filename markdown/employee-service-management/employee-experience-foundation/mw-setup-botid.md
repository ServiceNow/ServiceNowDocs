---
title: Configure bot ID and AI assistant
description: Specify the bot ID to configure Moveworks AI assistant on Employee Center portal.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-01-06"
reading_time_minutes: 1
breadcrumb: [Moveworks for Employee Center, Unified Employee Experience, Employee Service Management]
---

# Configure bot ID and AI assistant

Specify the bot ID to configure Moveworks AI assistant on Employee Center portal.

## Before you begin

Confirm that you have the appropriate entitlements for the application.

**Note:** To save the page with Bot ID, verify that the your application scope is selected to Moveworks for Employee Center.

Role required: admin

## About this task

Copy the bot ID from **Moveworks** &gt; **Chat Platform** &gt; **Manage Chatbots**. For more information, see [Embedded AI Assistant Installation-ServiceNow](https://help.moveworks.com/docs/moveworks-for-web-installation-servicenow).

**Note:** You need not perform other steps or provide any REST API details.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Moveworks Assistant Setup**.

2.  Add **Bot ID** which can be found from the **Manage Chatbots** record from Moveworks.

    For detailed Bot ID instructions, see [Embedded AI Assistant Installation-ServiceNow](https://help.moveworks.com/docs/moveworks-for-web-installation-servicenow).

3.  Specify the initialization options in JSON format for Moveworks integration.

    ![Example for illustration purpose only, Embedded AI Assistant setup for Moveworks](../images/mw-embed-ai-botid.png "Example: Embedded AI Assistant setup for Moveworks")

    You can configure initialization options according to your requirement. For example, for custom width and height,

    ```
    
    "styles": {
       "bottom": "20px",
       "right": "20px",
       "width": "400px",
       "height": "600px"
    }
    
    ```

    For complete configuration with branding,

    ```
    
    {
    "styles": {
       "bottom": "30px",
       "right": "30px",
       "z_index": "9999"
    },
    "theme": {
       "primary_color": "#5550DD",
       "font_family": "Arial, sans-serif"
    }
    }
    ```

4.  Select **Save configuration**.


## Result

The Moveworks application is ready for use. You can access the features and functionality per your role permissions.

## What to do next

You can perform the following actions:

-   Verify the Moveworks chatbot visibility from **All** &gt; **Self-Service** &gt; **Employee Center** portal. For more information, see [Use Moveworks on employee portal](../concept/mw-employee-chat-ui.md).
-   Test basic functionality by invoking the assistant and asking a sample question.
-   Check system properties and verify that all Moveworks specific properties are configured properly.

**Related topics**  


[Moveworks for Employee Center reference](../reference/mw-ec-integration-reference.md)

