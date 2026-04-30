---
title: Retrieve Self-configured bot details
description: Retrieve the details of the bot that you created in the Slack workspace to integrate with the ServiceNow instance.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating a Self-configured bot with Slack workspace, Conversational Integration with Slack, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Retrieve Self-configured bot details

Retrieve the details of the bot that you created in the Slack workspace to integrate with the ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  Log in to [Slack API](https://api.slack.com/apps).

2.  Click **Your Apps**, select a bot and navigate to **Settings** &gt; **Basic Information** &gt; **Display Information** to copy the **App name** \(Bot name\).

3.  Enter your **Bot User OAuth Access Token** in the token argument, click **Test Method**, and copy the **Team ID**.

    **Note:** You can find the Access token in **OAuth &amp; Permissions** in your Slack app.

    ![The Slack Team ID is shown in the code window as "id":"T01GDN5CCUE."](../images/slack-team-id.png)

4.  Navigate to Basic Information in your Slack workspace \(in api.slack.com\) and copy the **Signing Secret** under **App Credentials**.![The Signing Secret field is highlighted in the App Credentials page in your workspace. If it is hidden, select Show.](../images/slack-signing-secret.png)

5.  Navigate to OAuth &amp; Permissions in your Slack workspace and copy the **Bot User OAuth Access Token**.

    ![The Bot User OAuth Access Token field is highlighted in the Slack instance. Select "Copy" to copy it to the clipboard.](../images/slack-access-token.png)


## Result

You should now be able to interact with your Self-configured bot.

If you do not see your bot under the Apps section, then click **Add Apps** and search for your bot and select it. You can type **hi** to receive a response.

