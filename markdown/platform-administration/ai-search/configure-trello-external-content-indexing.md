---
title: Configure Trello for external content indexing
description: Create and authorize a Power-Up in the Trello Power-Up Admin Portal to allow the Trello external content connector to access your Trello source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Trello external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Trello for external content indexing

Create and authorize a Power-Up in the Trello Power-Up Admin Portal to allow the Trello external content connector to access your Trello source system.

## Before you begin

Your organization must be on the Trello Enterprise plan. For details on this plan, see [https://trello.com/enterprise](https://trello.com/enterprise).

Make sure that you have the Trello Enterprise Name for your organization.

**Note:** You can find your Enterprise Name in the URL for your organization's Trello Enterprise Admin Dashboard, which has the format `https://trello.com/e/EnterpriseName/admin`. For more information on the Trello Enterprise Admin Dashboard, see [https://trello.com/guide/enterprise/admins-dashboard](https://trello.com/guide/enterprise/admins-dashboard).

You need developer privileges for the Trello Power-Up Admin Portal.

Role required: none

## About this task

The Trello external content connector retrieves content from publicly accessible boards in your Trello source system using the Trello REST API.

To allow the connector to access your Trello source system via the Trello REST API, you must configure and authorize a Power-Up in the Trello Power-Up Admin Portal. Your connector admin can use settings copied from the Power-Up to configure the Trello external connector for proper connection to your source system.

## Procedure

1.  In the Trello Power-Up Admin Portal, create a new Power-Up for the Trello external content connector.

    1.  Navigate to [https://trello.com/power-ups/admin](https://trello.com/power-ups/admin) and log in with developer credentials.

    2.  Select **New**.

    3.  Enter a name for your new Power-Up.

        As an example, you might enter `Trello external content connector`.

    4.  Select the Trello workspace that will own your new Power-Up.

        This should be the workspace that includes the content you want the external content connector to retrieve and make searchable.

    5.  Enter your email address, a support contact email address or URL, and an author name for your new Power-Up.

    6.  Select **Create**.

    You're taken to the Basic Information page for your new Power-Up.

2.  Generate an API key and a token for your new Power-Up.

    1.  Navigate to the **API Key** page for your new Power-Up.

    2.  Select **Generate a new API key**.

    3.  In the Generate API key modal window, select **Generate API key**.

    4.  Copy your new API key and store it in a secure location.

        **Important:** Your external content connector admin needs this API key when configuring the Trello external content connector.

    5.  Select **Token**.

    6.  On the authorization screen, select **Allow**.

    7.  Copy your new token and store it in a secure location.

        **Important:** Your external content connector admin needs this API token when configuring the Trello external content connector.

3.  Get the ID for your enterprise \(organization\) from Trello.

    1.  Run this curl command, replacing `<enterprise-name>` with your organization's Trello Enterprise Name, `<api-key>` with your copied API key, and `<api-token>` with your copied API token:

        ```rest_api_curl_example
        curl --request GET \
          --url 'https://api.trello.com/1/enterprises/<enterprise-name>?key=<api-key>&token=<api-token>' \
          --header 'Accept: application/json'
        ```

    2.  Copy the `idEnterprise` value from the curl response and store it in a secure location.

        **Important:** Your external content connector admin needs this enterprise ID when configuring the Trello external content connector.


## What to do next

Provide the following items to your connector admin:

-   The API key that you copied in step [2.d](configure-trello-external-content-indexing.md#copy-api-key-step).
-   The API token that you copied in step [2.g](configure-trello-external-content-indexing.md#copy-api-token-step).
-   The enterprise ID that you copied in step [3.b](configure-trello-external-content-indexing.md#copy-enterpriseid-step).
-   The base URL for the Trello REST API. This is usually `https://api.trello.com`.

Your connector admin needs these items to configure a Trello external content connector to retrieve boards from your Trello source system.

For details on creating and configuring a Trello external content connector, see [Create a Trello external content connector](create-ext-cont-connector-trello.md).

**Parent Topic:**[Trello external content connector](../concept/trello-external-content-connector.md)

