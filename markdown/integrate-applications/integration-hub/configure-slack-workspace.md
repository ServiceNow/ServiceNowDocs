---
title: Configure Slack app
description: Create a custom OAuth application on your Slack workspace to enable OAuth 2.0 authentication with the Slack spoke.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up Slack spoke, Slack Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Configure Slack app

Create a custom OAuth application on your Slack workspace to enable OAuth 2.0 authentication with the Slack spoke.

## Before you begin

Role required: admin

## About this task

Complete these steps from your Slack account. You can create an app or configure an existing app as per the configurations outlines here.

## Procedure

1.  Create a Slack workspace.

    To learn how to create a workspace, see [Create a Slack workspace](https://slack.com/intl/en-in/help/articles/206845317-Create-a-Slack-workspace).The following image shows a typical Slack workspace.

    ![Slack Workspace.](../../integrationhub-store-spokes/image/slack-workspace.png)

2.  Navigate to the [Slack API](https://api.slack.com/) console.

3.  Click **Create an app**.

4.  On the Create an app window, select the most appropriate method to create the app.

    ![Create an app on Slack.](../../integrationhub-store-spokes/image/slack-create-app.png)

5.  From the App Credentials page on the Basic Information page, copy and record the values of Client ID, Client Secret, and Signing Secret of your Slack app.

    ![Slack app credentials.](../../integrationhub-store-spokes/image/slack-app-credentials.png)

    For more information, see the [Obtain Client ID and Client Secret](https://api.slack.com/authentication/postman#get_client_secret) for later step.

6.  On the OAuth &amp; Permissions page:

    1.  Specify the ServiceNow instance URL in **Redirect URLs** in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.

    2.  Add these bot token scopes:

        -   channels:history
        -   channels:manage
        -   channels:read
        -   chat:write
        -   chat:write.customize
        -   groups:read
        -   im:read
        -   mpim:read
        -   groups:history
        -   groups:write
        -   im:history
        -   im:write
        -   mpim:history
        -   mpim:write
        -   users:read
        -   users:read.email
        -   files:read
        For more information, see [Scopes and permissions](https://api.slack.com/scopes).

        **Note:** The spoke set up procedure outlined here requires bot user tokens only. You can't use the Create User and Deactivate User actions while using the bot token scopes. To use these actions, you must obtain user token from your Slack account.

7.  On the Slash Commands page, create a command and specify these values:

    |Field|Value|
    |-----|-----|
    |Command|/now|
    |Request URL|https://&lt;instance-name&gt;.service-now.com/api/sn\_slack\_ah\_v2/command\_service/&lt;slack-app-name&gt;|
    |Short Description|Description about the command.|
    |Usage Hint|List of parameters than can be passed. For example, `[operation] [table]`.|

    For more information, see the [Creating a Slash command](https://api.slack.com/interactivity/slash-commands) step.

8.  On the Interactivity &amp; Shortcuts page:

    1.  Enable **Interactivity** and specify the ServiceNow instance URL in **Request URL** in this format: `https://<instance-name>.service-now.com/api/sn_slack_ah_v2/slack/<slack-app-name>/interactivepayload` .

        For more information, see the [Preparing your app for user interactions](https://api.slack.com/interactivity/handling) section.

    2.  Create a shortcut that appears on messages and enter the value, `post_message_now` for **Callback ID**.

        For more information, see the [Creating a shortcut](https://api.slack.com/interactivity/shortcuts/using#:~:text=To%20make%20shortcuts%20available%20in,the%20menu%20item%20OAuth%20%26%20Permissions.) section.

9.  Create a Slack bot and add the bot to your Slack app and required channels.

    For more information, see [Create a bot for your workspace](https://slack.com/intl/en-in/help/articles/115005265703-Create-a-bot-for-your-workspace).


