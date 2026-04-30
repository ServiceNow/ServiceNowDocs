---
title: Create a bot in Microsoft Teams for GCC-H or DoD
description: Create a self-configured bot with Microsoft Teams for GCC-H or DoD customers to be able to integrate with the Virtual Agent.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Create, bot, Microsoft Teams, MSTeams, GCC-H, DoD]
breadcrumb: [Integrating Virtual Agent with Microsoft Teams for GCC-H or DoD, Specialized Virtual Agent integrations for Microsoft Teams, Integrating Virtual Agent with Microsoft Teams, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a bot in Microsoft Teams for GCC-Hor DoD

Create a self-configured bot with Microsoft Teams for GCC-H or DoD customersto be able to integrate with the Virtual Agent.

## Before you begin

Role required: none

## Procedure

1.  Log in to [Azure portal home page](http://portal.azure.us) and search for `Bot Services` on the top search bar.

    ![Microsoft Azure portal, with Bot Services feature highlighted.](../images/azure-bot-services.png)

2.  On the Bot services page, select **Create** and select **Azure Bot**.

    ![Microsoft Azure Applied AI Services portal with Create button highlighted, and Bot Service portal with Azure Bot service highlighted.](../images/select-azure-bot.png)

3.  On the Azure Bot page, select **Create** next to the Plan menu.

    ![Microsoft Azure Bot portal, showing Azure Bot plan selected from menu.](../images/create-azure-bot.png)

4.  On the form, fill in the **Bot Handle**, **Subscription**, **Resource group**, **New resource group location**, and **Pricing** details.

    ![Create an Azure bot form. Azure Government Enterprise subscription option, Multi Tenant type of app option, and Create new Microsoft App ID radio button are selected.](../images/create-bot.png)

5.  Under **Microsoft App ID**, select the type of application from the Type of App list.

    You can create a multi tenant app or a single tenant app.

6.  Select the **Creation type** radio button.

    **Note:** If an existing app is being used, make sure that the type of app is the same as the type of bot you’re creating. This verification is important because a multi tenant app will work with a multi tenant Microsoft Teams bot and vice versa.

7.  Select **Review + create**.

8.  Review the Basic bot details provided and select **Create**.

    When the bot is successfully created, you will receive the `Deployment succeeded` message.

9.  On the left navigation, select **Channels** and select the Microsoft Teams icon under **Add a featured channel**.

    ![MS Teams Channels tab view, with Channels tab and Configure Microsoft Teams channel highlighted.](../images/msteams-channel.png)

10. On the Terms of Service pop-up, select **Save** and select **Agree**.

    The channel gets saved.

11. On the left navigation, select **Configuration**, complete the configuration form, and select **Apply**.

    ![Microsoft Azure bot configuration form, with Configuration tab leading to form highlighted.](../images/bot-configuration.png)

    **Note:** In the **Messaging endpoint** field, provide the instance URL address.

    For example: `https://<instancename>.service-now.com/api/now/v1/cs/adapter/msft/events`.

    The domain might not be `service-now.com` and could be different. For example, the domain for GCC is `servicenowservices.com`.

    Replace the &lt;instancename&gt; with the name of your ServiceNow instance where you are integrating with Microsoft Teams.

12. On the left navigation, select **Overview**.

    You can also get to the Overview page by navigating to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App Registrations** and locate your application from the list to retrieve the following details.

13. Perform the following steps to retrieve the secret value code:

    1.  Copy the **Application \(client\) ID** and **Directory \(tenant\) ID** of your application and make a note of it.

    2.  On the left navigation bar under **Manage**, select **Certificates &amp; Secrets**.

    3.  Select **+ New client secret**, add your **Description** and **Expiration**, and select **Add**.

    4.  Copy the secret value code in the **Value** field and make a note of it.

        **Note:** The secret value code is visible only once.


**Parent Topic:**[Integrating Virtual Agent with Microsoft Teams for GCC-H or DoD](../concept/va-integ-msteams-gcch.md)

