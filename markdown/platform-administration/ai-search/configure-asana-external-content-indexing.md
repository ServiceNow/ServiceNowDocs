---
title: Configure Asana for external content indexing
description: Create and authorize an OAuth 2.0 application in the Asana developer console to allow the Asana external content connector to access your Asana source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Asana external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Asana for external content indexing

Create and authorize an OAuth 2.0 application in the Asana developer console to allow the Asana external content connector to access your Asana source system.

## Before you begin

You need the super admin role for your organization's Asana instance. To learn about this role, see the [Admin and super admin roles in Asana](https://help.asana.com/s/article/admin-and-super-admin-roles-in-asana) Asana help resource.

Role required: none

## About this task

The Asana external content connector retrieves projects, tasks, and comments from your Asana source system using the Asana API.

To allow the connector to access your Asana source system via the Asana API, you must configure and authorize an OAuth 2.0 application in the Asana developer console. Your connector admin can use settings copied from the OAuth 2.0 application to configure the Asana external connector for proper connection to your source system.

## Procedure

1.  Log in to Asana and access the Asana developer console.

    1.  Navigate to [https://app.asana.com/](https://app.asana.com/) and log in with your super admin credentials.

    2.  Select your user avatar, then select **Settings** from the context menu.

    3.  In the Apps tab of the Settings modal window, find the Build new apps section and select **View developer console**.

    The Asana developer console opens.

2.  In the Asana developer console, create a new OAuth 2.0 application for the Asana external content connector.

    1.  Select **Create new app**.

    2.  In the Create new app modal window, enter a name for your app.

        As an example, you might enter `Asana external content connector`.

    3.  Select the **Integrate Asana and another tool** option.

    4.  Select the **I agree to the Asana API Terms** option.

    5.  Select **Create app**.

    The Basic information page for your new app appears.

3.  On the Basic information page, record the client ID and client secret for your new OAuth 2.0 application.

    1.  In the Client ID field, select **Copy** to copy your new app's client ID, then record its value in a secure location.

        **Important:** Your external content connector admin needs this client ID when configuring the Asana external content connector.

    2.  In the Client secret field, select **Copy** to copy your new app's client secret, then record its value in a secure location.

        **Important:** Your external content connector admin needs this client secret when configuring the Asana external content connector.

4.  Configure an OAuth redirect URL for your new app.

    1.  Navigate to **Configure** &gt; **OAuth**.

        The OAuth page for your new app appears.

    2.  In the Redirect URLs section, select **Add redirect URL**.

    3.  In the Add redirect URL modal window, enter `https://<instance-name>.service-now.com/oauth_redirect.do`, replacing `<instance-name>` with the name of your ServiceNow AI Platform® instance, then select **Add**.

    The new redirect URL appears on the OAuth page.

5.  Configure Asana API permission scopes for your new app.

    1.  On the OAuth page, in the Permission scopes section, select the options for all of the following permission scopes:

        -   Goals: Read \(`goals:read`\)
        -   Portfolios: Read \(`portfolios:read`\)
        -   Projects: Read \(`projects:read`\)
        -   Stories: Read \(`stories:read`\)
        -   Tasks: Read \(`tasks:read`\)
        -   Team memberships: Read \(`team_memberships:read`\)
        -   Teams: Read \(`teams:read`\)
        -   Users: Read \(`users:read`\)
        -   Workspaces: Read \(`workspaces:read`\)
    2.  Select **Save changes**.

6.  Share your new app with your Asana workspaces.

    1.  Navigate to **Test &amp; distribute** &gt; **Manage distribution**.

        The Manage distribution page for your new app appears.

    2.  Select **Specific workspaces**.

    3.  Select **Add workspace**, then choose the Asana workspace that you want to distribute the new app to and select **Add**.

    4.  Repeat the preceding step if you want to distribute your new app to multiple Asana workspaces.


## What to do next

Provide the following items to your connector admin:

-   The client ID for your new OAuth 2.0 application that you copied in step [3.a](configure-asana-external-content-indexing.md#copy-client-id-step).
-   The client secret for your new OAuth 2.0 application that you copied in step [3.b](configure-asana-external-content-indexing.md#copy-client-secret-step).

Your connector admin needs these items to configure an Asana external content connector to retrieve projects, tasks, comments, and security principals from your Asana source system.

For details on creating and configuring an Asana external content connector, see [Create an Asana external content connector](create-ext-cont-connector-asana.md).

**Parent Topic:**[Asana external content connector](../concept/asana-external-content-connector.md)

