---
title: Integrate your self-configured bot with single Microsoft Teams tenant
description: Integrate multiple ServiceNow instances with a single Microsoft Teams tenant by creating multiple bots on the Microsoft Teams tenant. Use your ServiceNow Virtual Agent application, which supports multiple bots on a single Microsoft Teams tenant, to install Conversational Integration with Microsoft Teams application.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Microsoft Teams, MSTeams, tenant, Virtual Agent, Conversational Integration, bot]
breadcrumb: [Integrate multiple ServiceNow instances with a single MS Teams tenant, Specialized VA integrations for Teams, Integrate VA with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrate your self-configured bot with single Microsoft Teams tenant

Integrate multiple ServiceNow instances with a single Microsoft Teams tenant by creating multiple bots on the Microsoft Teams tenant. Use your ServiceNow Virtual Agent application, which supports multiple bots on a single Microsoft Teams tenant, to install Conversational Integration with Microsoft Teams application.

## Before you begin

Role required: virtual\_agent\_admin or admin and Microsoft Teams Tenant admin

This installation requires a ServiceNow instance other than the one integrated with the production bot to integrate with one bot \(of the multiple bots\) on a single Microsoft Teams tenant.

**Note:** The ServiceNow instance that you will use to integrate with a single Microsoft Teams tenant must not be an instance that you have used for installing Conversational Integration with Microsoft Teams in the primary method where you can integrate only one ServiceNow instance with one tenant.

Ensure that you created a bot on the Microsoft Teams tenant for each ServiceNow instance to be integrated. For more information, see [Create a bot in Microsoft Teams](create-bot-msteams.md).

## Procedure

1.  Fetch the Tenant ID, Client ID \(App ID\), Client Secret, and Bot Name details for your bot created in Microsoft Teams.

    For more information, see [Retrieve bot details](create-bot-msteams.md#bot-details).

    **Note:** Use this information when setting up the bot in your ServiceNow instance.

2.  As a ServiceNow admin, set up the bot on the ServiceNow instance in the global scope.

    **Note:** The virtual\_agent\_admin can install bots with multiple instances or bots apart from production in the ServiceNow instance and avail all the features of Virtual Agent and the flexibility to integrate one of the multiple ServiceNow instances with a bot on a single Microsoft Teams tenant.

    1.  Log in to your ServiceNow instance \(secondary instance for integrating with a bot on single Microsoft Teams tenant\) and navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

    2.  In **General Settings** under **Channels and integrations**, select **View All**.

        The Channels and integrations page opens.

    3.  Under the Available Channels section in the Microsoft Teams tile, select **Add Integrations**.

        **Note:** The **Add Integrations** drop-down is available only after installing the Conversational Integration with Microsoft Teams plugin \(sn\_va\_teams\) on your ServiceNow instance.

        ![Microsoft Teams Add Integrations options. The Integrate with Self-configured bot option is selected.](../images/add-msteams-self-integ.png)

    4.  From the **Add Integrations** drop-down, select **Integrate with Self-configured bot**.

    5.  In the Integrate Microsoft Teams with self-configured bot page, enter the **Name of the bot**, **Tenant ID**, **Client ID \(App ID\)**, and **Client Secret** from creating the Microsoft Teams bot, and select the **Single tenant bot** check box before selecting **Submit**.

        ![Integrate Microsoft Teams with self-configured bot window in Conversational integrations Channels and integrations settings.](../images/msteams-multi-integ.png "Integrate Microsoft Teams with self-configured bot")

        **Note:** For each additional bot to be integrated, repeat steps 1 and 2. If you created your bot before October 2025, you don't need to select the **Single tenant box** check box.

        If you would like to integrate your ServiceNow instance with another Microsoft Teams bot, select the Add integration for Self-configured bot icon against the Self-configured bot or select the **Add integration** drop-down on the Manage Microsoft Teams channel page and select **Integrate with Self-configured bot**.![Manage Microsoft Teams channel in Conversational Interfaces general settings. The Add integration for Self-configured bot button and Integrate with Self-configured bot option in the Add integration drop-down menu are highlighted.](../images/add-self-config-integ.png)

        User receives a message that the installation is successful.


## What to do next

-   [Auto-generate the manifest file for uploading on Microsoft Teams](generate-manifest-file-msteams.md).
-   [Upload the manifest package file to publish your bot](upload-package-file-msteams.md)

**Parent Topic:**[Integrating multiple ServiceNow instances with a single Microsoft Teams tenant](../concept/va-integ-single-teams.md)

