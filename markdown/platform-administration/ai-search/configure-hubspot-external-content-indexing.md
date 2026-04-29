---
title: Configure HubSpot for external content indexing
description: Create and authorize a legacy public app in HubSpot to allow the HubSpot external content connector to access your HubSpot source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [HubSpot external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure HubSpot for external content indexing

Create and authorize a legacy public app in HubSpot to allow the HubSpot external content connector to access your HubSpot source system.

## Before you begin

You need a HubSpot developer account. For details on developer accounts, see [https://developers.hubspot.com/docs/getting-started/account-types](https://developers.hubspot.com/docs/getting-started/account-types).

Role required: none

## About this task

The HubSpot external content connector retrieves tickets and notes from your HubSpot source system using the HubSpot API.

To allow the connector to access your HubSpot source system via the HubSpot API, you must configure and authorize a legacy public app in HubSpot. Your connector admin can use settings copied from the public app to configure the HubSpot external connector for proper connection to your source system.

## Procedure

1.  In HubSpot, begin creating a new legacy public app for the HubSpot external content connector.

    1.  Navigate to [https://app-na2.hubspot.com/](https://app-na2.hubspot.com/) \(or your HubSpot URL, if different\) and log in with your credentials.

    2.  In the menu, select **Development**.

    3.  In the Development menu, select **Legacy Apps**.

    4.  On the Legacy Apps screen, select **Create**.

    5.  In the Create Legacy App dialog box, select **Public**.

        You're taken to the Basic Info screen for your new draft legacy public app.

2.  Configure required settings for your new legacy public app.

    1.  In the Public app name field, enter a name for your new legacy public app.

        As an example, you might enter `HubSpot external content connector`.

    2.  Navigate to the **Auth** tab.

    3.  In the Redirect URLs section, enter `https://<instance-name>.service-now.com/oauth_redirect.do`, replacing `<instance-name>` with the name of your ServiceNow AI Platform® instance.

    4.  In the Scopes section, select **Add new scope**.

    5.  On the Add new scope form, select each of the following scopes as Required, then select **Update**.

        -   crm.objects.companies.read
        -   crm.objects.users.read
        -   files
        -   tickets
        **Note:** The oauth scope is automatically selected as Required.

    6.  Select **Create app**.

    The new legacy public app is created and you're taken to its Basic Info screen.

3.  Copy the client ID and client secret for your new legacy public app.

    1.  Navigate to the **Auth** tab.

    2.  Copy the client ID for your new legacy public app and store it in a secure location.

        **Important:** Your external content connector admin needs this client ID when configuring the HubSpot external content connector.

    3.  Reveal the client secret by selecting **Show**.

    4.  Copy the client secret for your new legacy public app and store it in a secure location.

        **Important:** Your external content connector admin needs this client secret when configuring the HubSpot external content connector.


## What to do next

Provide the following items to your connector admin:

-   The client ID that you copied in step [3.b](configure-hubspot-external-content-indexing.md#copy-client-id-step).
-   The client secret that you copied in step [3.d](configure-hubspot-external-content-indexing.md#copy-client-secret-step).

Your connector admin needs these items to configure a HubSpot external content connector to retrieve tickets, notes, and security principals from your HubSpot source system.

For details on creating and configuring a HubSpot external content connector, see [Create a HubSpot external content connector](create-ext-cont-connector-hubspot.md).

**Parent Topic:**[HubSpot external content connector](../concept/hubspot-external-content-connector.md)

