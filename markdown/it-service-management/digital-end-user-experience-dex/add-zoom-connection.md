---
title: Add Zoom connection
description: Use the information generated during Zoom account configuration to register DEX for Zoom as an OAuth provider and enable the instance to request OAuth 2.0 tokens. Add the Zoom connection in Workflow Studio to perform actions in Zoom.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-09-15"
reading_time_minutes: 1
breadcrumb: [Configuring DEX for Zoom, Configure, Digital End-User Experience, IT Service Management]
---

# Add Zoom connection

Use the information generated during Zoom account configuration to register DEX for Zoom as an OAuth provider and enable the instance to request OAuth 2.0 tokens. Add the Zoom connection in Workflow Studio to perform actions in Zoom.

## Before you begin

Role required: admin

## Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  In the **Search all connections** field, enter `DEX for Zoom`.

    ![image.zoom_search_for_Dex]

    **Note:** The **Outbound** tab is selected by default. Confirm that the **Outbound** tab is already selected.

4.  In the **Zoom** card, select **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the DEX for Zoom spoke, select **View Details**.
    -   To manage more than one DEX for Zoom connection records, create a child alias record by selecting **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://www.servicenow.com/docs/access?context=support-multiple-connections&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
    If you’re configuring the spoke for the first time, select **Configure**. Otherwise, select **Edit**.

5.  On the form, fill the following values.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Base URL to connect to your Zoom instance. Enter `https://api.zoom.us`.|
    |OAuth Entity Name|Name to identify the application registry record.|
    |OAuth Client ID|Client ID created during application registration.|
    |OAuth Client Secret|Client secret created during application registration.|
    |OAuth Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`.|

    ![image.zoom_edit_connection_details]

6.  Select **Configure and Get OAuth Token**.

    A confirmation message is displayed that the token is available.![image.zoom_dex_confirmation_message]


