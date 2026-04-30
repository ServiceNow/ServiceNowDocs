---
title: Create a bot in Slack
description: You must create a self-configured bot in the targeted workspace in Slack to be able to integrate with the Virtual Agent.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating a self-configured bot with Slack workspace, Integrate VA with Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a bot in Slack

You must create a self-configured bot in the targeted workspace in Slack to be able to integrate with the Virtual Agent.

## Before you begin

Role required: none

**Note:** Users must have permissions to create a bot in the targeted workspace.

## Procedure

1.  Log in to [Slack API](https://api.slack.com/apps).

2.  Navigate to **Your Apps** and click **Create New App**.

3.  Enter an **App Name**, select your **Slack Workspace** and click **Create App**.

4.  Configure Interactive Components.

    1.  Navigate to **Interactivity** &gt; **Shortcuts** in the left menu and turn on **Interactivity**.

    2.  Update the **Request URL**.

        If you are setting up your self-configured bot on an ServiceNow instance, then the request URL must be `https://<instance-name>/api/now/v1/cs/adapter/slack/actions`.

    3.  Click **Save**.

5.  Configure Event Subscriptions.

    1.  Click **Event Subscriptions** in the left menu and turn on **Enable Events**.

    2.  Update the **Request URL**.

        If you are setting up your self-configured bot on a ServiceNow instance, then the request URL must be `https://<instance-name>.service-now.com/api/now/v1/cs/adapter/slack/events`.

    3.  Wait for the Request URL to get verified.![The Request URL field displays green "Verified" text with a check mark.](../images/slack-event-subscriptions.png)

    4.  Under Subscribe to bot events, click **Add Bot User Event** and add `message.im`.

    5.  Click **Save**.

6.  Navigate to the **Incoming Webhook** tab and slide the **Activate Incoming Webhooks** toggle switch to enable it.

7.  Configure OAuth &amp; Permissions.

    1.  Click OAuth &amp; Permissions from the left menu and navigate to **Scopes** &gt; **Bot Scopes**.

    2.  Select **Add an OAuth Scope** and add the following scopes:

        -   chat:write
        -   files:read
        -   files:write
        -   im.history
        -   incoming-webhook
        -   team:read
        -   users:read
        -   users:read.email
8.  Navigate to **OAuth &amp; Permissions**, click **Install to Workspace**, and click **Allow**.

    ![Dialog box window for allowing or canceling installation of a Test Bot in a Slack workspace.](../images/allow-bot-install.png)


**Parent Topic:**[Integrating a self-configured bot with Slack workspace](../concept/va-integ-single-slack.md)

