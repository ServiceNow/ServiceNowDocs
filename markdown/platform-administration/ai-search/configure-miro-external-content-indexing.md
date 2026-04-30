---
title: Configure Miro for external content indexing
description: Create and authorize an application in the Miro Developer Hub to allow the Miro external content connector to access your Miro source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-14"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Miro external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Miro for external content indexing

Create and authorize an application in the Miro Developer Hub to allow the Miro external content connector to access your Miro source system.

## Before you begin

You must be on the Miro Enterprise plan. For details on the Enterprise plan, see [https://help.miro.com/hc/en-us/articles/360017730433-Enterprise-Plan](https://help.miro.com/hc/en-us/articles/360017730433-Enterprise-Plan).

You need the Company Admin role for your organization in Miro. To learn about admin roles in Miro, see [https://help.miro.com/hc/en-us/articles/14766440626834-Understand-admin-roles-and-their-privileges](https://help.miro.com/hc/en-us/articles/14766440626834-Understand-admin-roles-and-their-privileges).

You must have a Developer team set up for your organization in Miro. To learn about creating a Developer team for your organization, see [https://help.miro.com/hc/en-us/articles/4766759572114-Enterprise-Developer-teams](https://help.miro.com/hc/en-us/articles/4766759572114-Enterprise-Developer-teams).

Role required: none

## About this task

The Miro external content connector retrieves searchable text content and metadata from boards in your Miro source system using the Miro REST API.

To allow the connector to access your Miro source system via the Miro REST API, you must configure and authorize an OAuth 2.0 application in the Miro Developer Hub. Your connector admin can use settings copied from the OAuth 2.0 application to configure the Miro external connector for proper connection to your source system.

## Procedure

1.  In the Miro Developer Hub, create a new application for the Miro external content connector.

    1.  Navigate to [https://developers.miro.com/](https://developers.miro.com/) and log in with your Company Admin credentials.

    2.  Navigate to **Your apps**, then select **Create a new app**.

        If you haven't created an app before, the app creation link may show **Create your first app** instead of **Create a new app**.

        The Profile settings screen appears and displays a Create new app modal window.

    3.  In the Create new app modal window, enter a name for your new app.

        As an example, you might enter `Miro external content connector`.

    4.  Select the Developer team for your new app.

    5.  Select the **Expire user authentication token** option.

    6.  Select **Create app**.

    The Profile settings page displays settings for your new app.

2.  Record the client settings for your new app.

    1.  In the App Credentials section of the app's settings screen, copy the client ID for your new app and record it in a secure location.

        **Important:** Your external content connector admin needs this client ID when configuring the Miro external content connector.

    2.  Copy the client secret for your new app and record it in a secure location.

        **Important:** Your external content connector admin needs this client secret when configuring the Miro external content connector.

3.  Configure the OAuth 2.0 redirect URI for your new application.

    1.  In the Redirect URI for OAuth 2.0 section of the app's settings screen, enter `https://<instance-name>.service-now.com/oauth_redirect.do`, replacing `<instance-name>` with your ServiceNow AI Platform® instance hostname.

    2.  Select **Add**.

    The new redirect URI appears in the application's settings.

4.  Configure permissions for your new application.

    1.  In the Permissions section of the app's settings screen, select the options for the following permissions in the All plans listing:

        -   boards:read
        -   identity:read
        -   team:read
    2.  Select the options for the following permissions in the Enterprise plan only listing:

        -   organizations:read
        -   organizations:teams:read
        -   projects:read
    Your permissions changes are automatically saved as you make them.


## What to do next

Provide the following items to your connector admin:

-   The OAuth 2.0 application client ID that you copied in step [2.a](configure-miro-external-content-indexing.md#copy-client-id-step)
-   The OAuth 2.0 application client secret that you copied in step [2.b](configure-miro-external-content-indexing.md#copy-client-secret-step)

Your connector admin needs these items to configure a Miro external content connector to retrieve searchable text content and metadata and security principals from your Miro source system.

For details on creating and configuring a Miro external content connector, see [Create a Miro external content connector](create-ext-cont-connector-miro.md).

**Parent Topic:**[Miro external content connector](../concept/miro-external-content-connector.md)

