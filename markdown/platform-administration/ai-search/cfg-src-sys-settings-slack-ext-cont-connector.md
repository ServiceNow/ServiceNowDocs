---
title: Configure Slack for external content indexing
description: Create a Slack API application to allow the Slack external content connector to crawl public channels in your Slack source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-30"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Slack external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Slack for external content indexing

Create a Slack API application to allow the Slack external content connector to crawl public channels in your Slack source system.

## Before you begin

You need permission to create Slack API applications in your organization's Slack workspace.

Role required: none

## About this task

The Slack external content connector retrieves content from public channels in your Slack source system using a Slack API application. You need to create this application and configure its OAuth settings to allow the external content connector access to your Slack workspace.

Your connector admin needs the Slack API application's client ID and secret to configure the Slack external content connector for proper connection to your Slack source system.

## Procedure

1.  Navigate to the Slack API: Applications page at [https://api.slack.com/apps](https://api.slack.com/apps).

2.  If prompted, sign in to your Slack account and select the workspace that you want the external content connector to crawl.

3.  Select **Create an App**.

    ![Your Apps page with Create an App button highlighted.](../image/slack-api-your-apps.png)

    If you already have existing applications on this page, select **Create New App** instead.

4.  In the Create an app dialog box, select **From scratch**.

    ![Create an app dialog box with From scratch option highlighted.](../image/slack-api-create-app.png)

5.  In the Name app &amp; choose workspace dialog box, specify a name and workspace for your application.

    1.  In the **App Name** field, enter a name for your application.

    2.  In the **Pick a workspace to develop your app in** field, select the workspace that you want the external content connector to crawl.

    3.  Select **Create App**.

    ![Name app & choose workspace dialog box with application name and workspace highlighted.](../image/slack-api-name-app-choose-workspace.png)

    The application's Settings page appears, open to the Basic Information page.

6.  In the App Credentials section, select **Show** to display the **Client Secret** field value, then record the application's **Client ID** and **Client Secret** values in a secure location.

    ![App Credentials section of Basic Information settings page with application client ID and client secret values highlighted.](../image/slack-api-app-credentials.png)

    **Important:** Your connector admin needs these values to configure the Slack external content connector.

7.  Navigate to **Features** &gt; **OAuth &amp; Permissions**.

8.  On the OAuth &amp; Permissions page, configure a redirect URL for the application.

    1.  In the Redirect URLs section, select **Add New Redirect URL**.

        ![Redirect URLs section of OAuth & Permissions features page with Add New Redirect URL button highlighted.](../image/slack-api-add-new-redirect-url.png)

    2.  Enter the URL for your ServiceNow AI Platform® instance, `https://<instance-name>.service-now.com`, replacing `<instance-name>` with the name of your instance.

    3.  Select **Add**.

    4.  Select **Save URLs**.

        ![Redirect URLs section of OAuth & Permissions features page with Save URLs button highlighted.](../image/slack-api-save-redirect-urls.png)

9.  On the OAuth &amp; Permissions page, in the Scopes section's Bot Token Scopes subsection, configure each of these bot token scopes for the application.

    -   channels:history
    -   channels:join
    -   channels:read
    -   files:read
    -   remote\_files:read
    -   team:read
    -   users:read
    1.  Select **Add an OAuth Scope**.

        ![Scopes section of OAuth & Permissions features page with Add an OAuth Scope button in Bot Token Scopes subsection highlighted.](../image/slack-api-add-oauth-bot-scope.png)

    2.  Enter the OAuth scope's name to filter the list of scopes, then select the scope's entry.

        The selected scope appears in the list of Bot Token Scopes for your application.

10. On the OAuth &amp; Permissions page, install the application into your Slack workspace.

    1.  In the OAuth Tokens section, select the link to install the application to your Slack workspace.

        The installation link's text will include the name of your Slack workspace. ![OAuth Tokens section of OAuth & Permissions features page with installation button highlighted.](../image/slack-api-install-workspace.png)

    2.  On the confirmation page, select **Allow**.

        ![Confirmation page for installation of application with Allow button highlighted.](../image/slack-api-install-allow.png)

11. On the OAuth &amp; Permissions page, opt into token rotation for the application.

    1.  In the Advanced token security via token rotation section, select **Opt In**.

        ![Advanced token security via token rotation section of OAuth & Permissions features page with Opt In button highlighted.](../image/slack-api-opt-in-token-rotation.png)

    2.  On the confirmation page, select **Opt in**.

        ![Confirmation page for token rotation opt-in with Opt in button highlighted.](../image/slack-api-opt-in-confirmation.png)


## What to do next

Provide the following items to your connector admin:

-   The Slack API application client ID and client secret that you recorded in step [6](cfg-src-sys-settings-slack-ext-cont-connector.md#record-client-id-and-secret-step).
-   The URL where your Slack workspace is accessible. This is usually `https://slack.com`.

Your connector admin needs these items to configure a Slack external content connector to retrieve searchable content and security principals from your Slack instance.

For details on creating and configuring a Slack external content connector, see [Create a Slack external content connector](create-ext-cont-connector-slack.md).

**Parent Topic:**[Slack external content connector](../concept/slack-external-content-connector.md)

