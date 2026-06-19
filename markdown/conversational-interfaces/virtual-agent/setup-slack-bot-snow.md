---
title: Retrieve self-configured bot details
description: Retrieve the details of the bot that you created in the Slack workspace to integrate with the ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/setup-slack-bot-snow.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating a self-configured bot with Slack workspace, Integrate VA with Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Retrieve self-configured bot details

Retrieve the details of the bot that you created in the Slack workspace to integrate with the ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  Log in to [Slack API](https://api.slack.com/apps).

2.  Click **Your Apps**, select a bot and navigate to **Settings** &gt; **Basic Information** &gt; **Display Information** to copy the **App name** \(Bot name\).

3.  Enter your **Bot User OAuth Access Token** in the token argument, click **Test Method**, and copy the **Team ID**.

    **Note:** You can find the Access token in **OAuth &amp; Permissions** in your Slack app.

    \[Omitted image "slack-team-id.png"\] Alt text: The Slack Team ID is shown in the code window as "id":"T01GDN5CCUE."

4.  Navigate to Basic Information in your Slack workspace \(in api.slack.com\) and copy the **Signing Secret** under **App Credentials**.\[Omitted image "slack-signing-secret.png"\] Alt text: The Signing Secret field is highlighted in the App Credentials page in your workspace. If it is hidden, select Show.

5.  Navigate to OAuth &amp; Permissions in your Slack workspace and copy the **Bot User OAuth Access Token**.

    \[Omitted image "slack-access-token.png"\] Alt text: The Bot User OAuth Access Token field is highlighted in the Slack instance. Select "Copy" to copy it to the clipboard.


## Result

You should now be able to interact with your Self-configured bot.

If you do not see your bot under the Apps section, then click **Add Apps** and search for your bot and select it. You can type **hi** to receive a response.

**Parent Topic:**[Integrating a self-configured bot with Slack workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-integ-single-slack.md)

