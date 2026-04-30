---
title: Configure Lucidchart for external content indexing
description: Create and authorize an OAuth 2.0 application in the Lucid developer tools and enable the SCIM API in the Lucid admin tools to allow the Lucidchart external content connector to access your Lucidchart content.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-01"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Lucidchart external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Lucidchart for external content indexing

Create and authorize an OAuth 2.0 application in the Lucid developer tools and enable the SCIM API in the Lucid admin tools to allow the Lucidchart external content connector to access your Lucidchart content.

## Before you begin

You must have an Enterprise subscription for Lucidchart, with the System for Cross-domain Identity Management \(SCIM\) feature enabled for your account. To learn more about enabling SCIM for your account, see the Lucid SCIM API reference at [https://lucid.readme.io/reference/overview-scim](https://lucid.readme.io/reference/overview-scim).

You need admin privileges for the Lucid developer tools \([https://lucid.app/developer](https://lucid.app/developer)\) and the Lucid admin tools \([https://admin.lucid.app/](https://admin.lucid.app/)\).

The connector admin who will create your Lucidchart external content connectors needs an account in your organization's Lucidchart instance so that they can be assigned application collaborator roles for applications you create. Their account needs to have access to all of your Lucidchart content that you want the connector to be able to crawl or retrieve.

Role required: none

## About this task

The Lucidchart external content connector retrieves searchable content from documents in your Lucidchart source system using the Lucid SCIM API.

To allow the connector to access your Lucidchart source system via the SCIM API, you must configure and authorize an OAuth 2.0 application in the Lucid developer tools and generate a SCIM bearer token in the Lucid admin tools. Your connector admin needs the OAuth 2.0 application's client settings and the SCIM bearer token to configure the Lucidchart external connector for proper connection to your source system.

## Procedure

1.  Use the Lucid developer tools to create a new application for the Lucidchart external content connector.

    1.  Navigate to [https://lucid.app/developer](https://lucid.app/developer) and log in with admin credentials.

    2.  Select **Create Application**.

    3.  Enter a name for your new application.

        As an example, you might enter `Lucidchart external content connector`.

    4.  Select **Create**.

    The General settings tab for your new application appears.

2.  Invite your connector admin to be a collaborator on your new application.

    **Note:** You can skip this step if you're the connector admin who will create your Lucidchart external content connectors on your ServiceNow AI Platform instance. As the creator of the application, you're automatically added to it as an application collaborator with the **Owner** role.

    1.  In the Collaborators section, select **Invite**.

    2.  In the Invite application collaborator modal window, enter the email address for the connector admin who will create your Lucidchart external content connectors.

    3.  Select the **Tester** role for the invited application collaborator.

    4.  Select **Invite**.

    5.  Repeat these steps for each additional connector admin you need to invite to be an application collaborator.

3.  Create an OAuth 2.0 client in your new application.

    1.  Navigate to **OAuth 2.0**.

    2.  In the Create custom OAuth 2.0 client field, enter a name for your new OAuth 2.0 client.

        As an example, you might enter `Lucidchart external content connector OAuth 2.0 client`

    3.  Select **Create OAuth 2.0 client**.

        The details for your new OAuth 2.0 client appear.

    4.  Select the Copy icon ![](../image/lucid-copy-icon.png) to copy the **Client ID** value for your new OAuth 2.0 client, then record the value in a secure location.

        **Important:** Your external content connector admin needs this client ID value when configuring the Lucidchart external content connector.

    5.  Select the Copy icon ![](../image/lucid-copy-icon.png) to copy the **Client Secret** value for your new OAuth 2.0 client, then record the value in a secure location.

        **Important:** Your external content connector admin needs this client secret value when configuring the Lucidchart external content connector.

    6.  In the Authorized Redirect URIs section, select **Add Redirect URI**.

    7.  Enter `https://<instance-name>.service-now.com/oauth_redirect.do` as the callback URI, replacing `<instance-name>` with your ServiceNow AI Platform® instance name, then select **Add**.

4.  Generate a SCIM bearer token that you can use to authenticate requests to the Lucid SCIM API.

    1.  Navigate to [https://admin.lucid.app/](https://admin.lucid.app/) and log in with admin credentials.

    2.  Navigate to **App integration** &gt; **General**.

    3.  In the Enabled integrations section, find the SCIM integration and select its **Settings** link.

        **Note:** If the SCIM integration doesn't appear in the Enabled integrations section, contact Lucid support and ask them to enable SCIM for your account.

        The SCIM integration settings screen appears.

    4.  In the SCIM setup subsection's IdP configuration section, select **Generate token**.

        **Note:** If the link shows **Regenerate token** instead of **Generate token**, your account already has a SCIM bearer token generated. Skip to the next step.

    5.  Select the Copy icon ![](../image/lucid-copy-icon.png) to copy the **Bearer Token** value, then record the copied value in a secure location.

        **Important:** Your external content connector admin needs this SCIM bearer token value when configuring the Lucidchart external content connector.


## What to do next

Provide the following items to your connector admin:

-   The OAuth 2.0 client ID that you copied in step [3.d](configure-lucidchart-external-content-indexing.md#copy-client-id-step).
-   The OAuth 2.0 client secret that you copied in step [3.e](configure-lucidchart-external-content-indexing.md#copy-client-secret-step).
-   The SCIM bearer token that you copied in step [4.e](configure-lucidchart-external-content-indexing.md#copy-bearer-token-step).

Your connector admin needs these items to configure a Lucidchart external content connector to retrieve documents, folders, and security principals from your Lucidchart source system.

**Important:** If you invited any connector admins to be application collaborators in step [2](configure-lucidchart-external-content-indexing.md#invite-app-collaborators-step), make sure they've accepted their invitations. Without the application collaborator role, they won't be able to create a Lucidchart external content connector.

For details on creating and configuring a Lucidchart external content connector, see [Create a Lucidchart external content connector](create-ext-cont-connector-lucidchart.md).

**Parent Topic:**[Lucidchart external content connector](../concept/lucidchart-external-content-connector.md)

