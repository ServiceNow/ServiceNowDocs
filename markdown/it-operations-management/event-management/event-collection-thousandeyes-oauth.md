---
title: Integrate ThousandEyes with OAuth authentication
description: Create credentials in the instance and configure the ThousandEyes webhook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/event-collection-thousandeyes-oauth.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Integrate ThousandEyes platform events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configure, Event Management, ITOM AIOps, IT Operations Management]
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

6.  In ThousandEyes, navigate to **Manage** &gt; **Alert Rules**.

7.  Open an alert rule and select the **Notifications** tab.

8.  Under **Webhooks**, select **Configure Webhooks** or **Edit webhooks**, and then select **Add New Webhook**.

9.  Complete the following fields:

    -   **Name**

        Enter a name for the webhook.

    -   **URL**

        `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=thousandeyes`

    -   **Auth Type**

        Select **OAuth**.

    -   **Auth URL**

        `https://<instance-name>.service-now.com/oauth_auth.do`

    -   **Client ID**

        Paste the Client ID generated in the ServiceNow instance.

10. Select **Get Token**.

11. When the ServiceNow authorization page opens, sign in and select **Allow**.

12. Test and save the webhook.


