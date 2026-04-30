---
title: Integrate your Self-configured bot with Microsoft Teams for GCC
description: You must install the bot that you created in your Microsoft Teams tenant on your ServiceNow instance to integrate it with the Virtual Agent. Use your ServiceNow Virtual Agent application to install and configure Conversational Integration with Microsoft Teams.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-06"
reading_time_minutes: 2
keywords: [Integrate, self-configured, bot, Microsoft, Teams, MSTeams, GCC, Conversational Integration]
breadcrumb: [Integrating Virtual Agent with Microsoft Teams using the self-configured bot, Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate your Self-configured bot with Microsoft Teams for GCC

You must install the bot that you created in your Microsoft Teams tenant on your ServiceNow instance to integrate it with the Virtual Agent. Use your ServiceNow Virtual Agent application to install and configure Conversational Integration with Microsoft Teams.

## Before you begin

Role required: virtual\_agent\_admin or admin and Microsoft Azure admin.

This installation requires a ServiceNow instance to integrate with a self-configured bot on the Microsoft Teams tenant.

Ensure that you created a bot on the Microsoft Teams tenant to integrate with the ServiceNow instance. For more information, see [Create a Bot in Microsoft Teams](create-bot-msteams.md).

## Procedure

1.  Fetch the Tenant ID, Client ID \(App ID\), Client Secret, and Bot Name details for your bot created in Microsoft Teams.

    For more information, see [Retrieve bot details](create-bot-msteams.md#bot-details).

    **Note:** Use this information when setting up the self-configured bot in your ServiceNow instance.

2.  As a ServiceNow admin, set up the self-configured bot on the ServiceNow instance in the global scope.

    1.  Log in to your ServiceNow instance and navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

    2.  In **General Settings** under **Channels and integrations**, select **View All**.

        The Channels and integrations page opens.

    3.  Under the Available Channels section in the Microsoft Teams tile, select **Add Integrations**.

        **Note:** The **Add Integrations** drop-down is available only after installing the Conversational Integration with Microsoft Teams plugin \(sn\_va\_teams\) on your ServiceNow instance.

        ![Microsoft Teams Add Integrations options. The Integrate with Self-configured bot option is selected.](../images/add-msteams-self-integ.png)

    4.  From the **Add Integrations** drop-down, select **Integrate with Self-configured bot**.

    5.  In the Integrate Microsoft Teams with self-configured bot page, provide the **Name of the bot**, **Tenant ID**, **Client ID \(App ID\)**, and **Client Secret** that you made a note while creating the Microsoft Teams bot and select **Submit**.

        ![Integrate Microsoft Teams with self-configured bot window in Conversational integrations Channels and integrations settings.](../images/msteams-multi-integ.png "Integrate Microsoft Teams with self-configured bot")

        **Note:** If you own multiple ServiceNow instances and would like to integrate additional bots for additional instances, repeat the preceding steps to add and integrate with bots.

        If you would like to integrate your ServiceNow instance with another Microsoft Teams bot, select the Add integration for self-configured bot icon against the Self-configured bot or select the **Add integration** drop-down on the Manage Microsoft Teams channel page and select **Integrate with your self-configured bot**. ![Manage Microsoft Teams channel in Conversational Interfaces general settings. The Add integration for Self-configured bot button and Integrate with Self-configured bot option in the Add integration dropdown are highlighted.](../images/add-self-config-integ.png).

        For more information, see [Manage the ServiceNow Virtual Agent integration with Microsoft Teams](configure-va-teams.md).

        User receives a message that the installation is successful.


## What to do next

[Auto-generate the manifest file for uploading on Microsoft Teams](generate-manifest-file-msteams.md).

