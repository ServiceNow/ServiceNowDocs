---
title: Integrate your ServiceNow instance with a self-configured bot
description: Add the self-configured bot to your ServiceNow instance to complete the integration with Slack.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Self-configured bot, Slack, Virtual Agent, Channel, Integration]
breadcrumb: [Integrating a self-configured bot with Slack workspace, Integrate VA with Slack, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate your ServiceNow instance with a self-configured bot

Add the self-configured bot to your ServiceNow instance to complete the integration with Slack.

## Before you begin

Role required: virtual\_agent\_admin or admin and Slack workspace admin

This installation requires a ServiceNow instance other than the one integrated with the production bot to integrate one bot \(of the multiple bots\) with a single Slack workspace.

**Note:** The ServiceNow instance that you will use to integrate the self-configured bot with a single Slack workspace must not be an instance that you have used for integrating the ServiceNow Virtual Agent.

Ensure that you created a bot on the Slack workspace and fetched the bot details to complete the integration. For more information, see [Create a bot in Slack](create-self-config-bot-slack.md).

Fetch the Name of the bot, Team ID, Signing Secret, and Access Token details for your bot created in Slack. For more information, see [Retrieve bot details](setup-slack-bot-snow.md). Use this information when setting up the bot in your ServiceNow instance.

## Procedure

1.  As a ServiceNow admin, set up the bot on the ServiceNow instance in the global scope.

    **Note:** The virtual\_agent\_admin can install bots with multiple instances or bots apart from the production bot in the ServiceNow instance and avail all the features of Virtual Agent and also have the flexibility to integrate one of the multiple ServiceNow instances with a bot on a single Slack workspace.

    1.  Log in to your ServiceNow instance and navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

    2.  In **General Settings** under **Channels and integrations**, select **View All**.

        The Channels and integrations page opens.

    3.  Under the Available Channels section in the Slack tile, select **Add Integrations** and select **Integrate with Self-configured bot**.

        ![Slack Add integration dropdown. The Integrate with Self-configured bot option is highlighted.](../images/add-slack-self-integ.png)

        **Note:** The **Add Integrations** button is available only after installing the Conversational Integration with Slack plugin \(sn\_va\_slack\) on your ServiceNow instance. For more information about getting the plugin installed, see [Install the Conversational Integration with Slack](install-slack-from-store.md).

    4.  In the Integrate Slack with self-configured bot page, provide the following details that you made a note while creating the Slack bot and select **Submit**.

        -   **Name of the bot**
        -   **Team ID**
        -   **Signing Secret**
        -   **Access Token**
        For more information, see [Retrieve bot details](setup-slack-bot-snow.md).

        ![To integrate Slack, provide the bot name, Team ID, Signing Secret, and Access Token.](../images/slack-self-bot-integ.png "Integrate Slack with self-configured bot page")

        **Note:** For each additional ServiceNow instance to be integrated, repeat steps 1 and 2.

        If you would like to integrate your ServiceNow instance with another Slack bot, select the Plus icon against the Self-configured bot or select the **Add integration** button on the Manage Slack channel page and select **Integrate with Self-configured bot**.

        ![Manage Slack channel view in Conversational Interfaces general settings. The Add integration for self-configured bot button and Integrate with Self-configured bot option in the Add integration dropdown are highlighted.](../images/add-self-config-integ-slck.png)

        You will receive a message that the installation is successful.


**Parent Topic:**[Integrating a self-configured bot with Slack workspace](../concept/va-integ-single-slack.md)

