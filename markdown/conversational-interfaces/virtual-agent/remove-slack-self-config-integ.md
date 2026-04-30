---
title: Remove Self-configured bot integration with Slack
description: Remove the Self-configured bot integration from your ServiceNow instance to disassociate with the Slack app.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Remove, self-configured, bot, integration, Slack]
breadcrumb: [Integrating a Self-configured bot with Slack workspace, Integrating Virtual Agent with Slack, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Remove Self-configured bot integration with Slack

Remove the Self-configured bot integration from your ServiceNow instance to disassociate with the Slack app.

## Before you begin

Roles required:

-   Virtual\_agent\_admin and external\_app\_install\_admin or admin
-   Administrator for third-party applications

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, select **View All**.

3.  On the Channels and integration page, in the Slack tile, select **Manage**.

4.  In the Manage Slack Channel page, find the Self-configured bot integration to remove from your ServiceNow instance, select the manage bot icon ![Manage bot icon.](../images/manage-bot-icon.png), and select **Remove integration**.

    ![Remove integration option with Self-configured bot.](../images/remove-self-bot-integration.png "Remove integration with Self-configured bot")

5.  In the Remove integration confirmation message, select **Remove**.![Banner message confirming remove Self-configured bot integration with Slack.](../images/remove-slack-integ-success.png)

    The Self-configured bot integration with Slack has been removed successfully.


**Parent Topic:**[Integrating a Self-configured bot with Slack workspace](../concept/va-integ-single-slack.md)

