---
title: Remove ServiceNow Virtual Agent integration with Slack
description: Remove the ServiceNow Virtual Agent integration from your ServiceNow instance to disassociate the Slack app.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Virtual Agent, integration, Slack]
breadcrumb: [Integrating ServiceNow Virtual Agent with Slack, Integrating Virtual Agent with Slack, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Remove ServiceNow Virtual Agent integration with Slack

Remove the ServiceNow Virtual Agent integration from your ServiceNow instance to disassociate the Slack app.

## Before you begin

Roles required:

-   Virtual\_agent\_admin and external\_app\_install\_admin or admin
-   Administrator for third-party applications

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, select **View All**.

3.  On the Channels and integration page, in the Slack tile, select **Manage**.

4.  In the Manage Slack channel page, find the ServiceNow Virtual Agent integration to remove from your ServiceNow instance, select the manage bot icon ![Manage bot icon.](../images/manage-bot-icon.png), and select **Remove integration**.

    ![Remove integration option with Now Virtual Agent.](../images/remove-snva-integration.png "Remove integration with ServiceNow Virtual Agent")

5.  In the Remove integration confirmation message, select **Remove**.

    You are redirected to the Slack App Directory.

6.  On the Slack app directory, navigate to the Configuration tab, and select **See All** against **1 authorized member**.

7.  Select **Revoke** in the 1 Authorized member pop-up.

8.  Select **Revoke** in the confirmation message.![Revoke ServiceNow Virtual Agent integration with Slack.](../images/revoke-slack-snow-integ.png)

    A message appears saying that **You have successfully removed an authorization for Now Virtual Agent**.

    ServiceNow Virtual Agent integration with Slack is removed from your ServiceNow instance.


**Parent Topic:**[Integrating ServiceNow Virtual Agent with Slack](../concept/va-integ-slack.md)

