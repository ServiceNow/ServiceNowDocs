---
title: Create a Bot in Microsoft Teams
description: You must create a bot in Microsoft Teams to be able to integrate with the Virtual Agent.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating multiple ServiceNow instances with a single Microsoft Teams tenant, Specialized Virtual Agent integrations for Microsoft Teams, Integrating Virtual Agent with Microsoft Teams, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a Bot in Microsoft Teams

You must create a bot in Microsoft Teams to be able to integrate with the Virtual Agent.

## Before you begin

Role required: Microsoft Teams admin, Global Administrator, or roles containing Application Administrator.

## Procedure

1.  Login into [Microsoft Teams](https://teams.microsoft.com/) and navigate to [Developer Portal](https://dev.teams.microsoft.com).

2.  On the Developer Portal page, navigate to the **Tools** &gt; **Bot Management**.

3.  Select **Create a New bot** and provide a bot name of your choice and select **Add**.

4.  Open the bot that you created and select the **Configure** tab.

5.  Under Endpoint address, specify the following URL:

    For example: `https://<instancename>.service-now.com/api/now/v1/cs/adapter/msft/events`

    **Note:** Replace the &lt;instancename&gt; with the name of your ServiceNow instance where you are integrating with Microsoft Teams. In case of multi-instance single tenant integration, use the secondary ServiceNow instance for integrating with a bot on Microsoft Teams tenant.

6.  Select **Save**.

7.  Navigate to **Client secrets** and select **Add a client secret for your bot**.

8.  Copy the value of the client secret from the **New client secret generated** pop-up for later use as it is displayed only during this step and select **OK**.

9.  Navigate to **Developer Portal** &gt; **Tools** &gt; **Bot management** and copy the Bot ID of the bot you created.

10. Retrieve the following details of your bot in Microsoft Teams to integrate with Virtual Agent.

    -   Tenant ID: Follow the instructions on [Microsoft Teams documentation](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-how-to-find-tenant), to fetch the Tenant ID.
    -   Client ID \(App ID\): Client ID is the Bot Id that you have copied as mentioned in Step 8.
    -   Client Secret: It is the secret that you have copied as mentioned in Step 7.
    -   Bot Name: The name of the bot that you entered in Step 3.
    -   Select the **Single tenant** check box.

        **Note:** If you created your bot before October 2025, you don't need to select the **Single tenant** check box.

11. Press **Enter** to save.


## What to do next

[Integrate your Self-configured bot with single Microsoft Teams tenant](teams-install-custom-app.md).

**Parent Topic:**[Integrating multiple ServiceNow instances with a single Microsoft Teams tenant](../concept/va-integ-single-teams.md)

