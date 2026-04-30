---
title: Integrate ThousandEyes with OAuth authentication
description: Create credentials in the instance and configure the ThousandEyes webhook.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate ThousandEyes platform events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate ThousandEyes with OAuth authentication

Create credentials in the instance and configure the ThousandEyes webhook.

## Before you begin

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and then select **New**.

2.  Select **Create an OAuth API endpoint for external clients**.

3.  Copy the automatically generated field **Client ID**.

    The **Client ID** is used when configuring the ThousandEyes SeviceNow integration.

4.  Unlock the **Redirect URL** field and assign the value: **https://app.thousandeyes.com/webhooks-oauth-callback/**

5.  Configure the Access and Refresh token lifespans by providing a value in seconds.

6.  Open the ThousandEyes webhook configuration and complete the following fields:

    -   **Name**

        Any name

    -   **URL**

        ServiceNow ThousandEyes Push connector end point

    -   **Select Auth Type**

        OAuth

    -   **Grant Type**

        Implicit

    -   **Auth URL**

        https://servicenow\_insatnce&gt;.service-now.com/oauth\_auth.do

    -   **Client ID**

        Paste the Client ID automaticcally generated in Step 3.

7.  Select **Get Token**.

8.  Once the ThousandEyes connector navigates to a webpage requesting to connect to your ServiceNow account, select **Allow**.

9.  Provide account credentials which have the **web\_service\_admin** role.


