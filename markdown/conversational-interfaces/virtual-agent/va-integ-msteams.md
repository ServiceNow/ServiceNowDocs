---
title: Integrating Virtual Agent with Microsoft Teams
description: Enables ServiceNow Virtual Agent to integrate with Microsoft Teams application.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-04-02"
reading_time_minutes: 1
keywords: [ServiceNow, Virtual Agent, integration, MS Teams, Microsoft, Teams]
breadcrumb: [Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Microsoft Teams

Enables ServiceNow Virtual Agent to integrate with Microsoft Teams application.

**Note:** The Premium Chat experience is available for Virtual Agent in Microsoft Teams. You must have the virtual\_agent\_admin or admin role to activate Premium Chat. To display your assistant, do the following:

-   Navigate to **ALL** &gt; **sys\_now\_assist\_deployment\_channel.list**.
-   Find the **Document Id** `Provider Channel Identity: MSD Teams Bot`, and set the value of **Experience** to `AI Native`.

![Now Assist Deployment Channels table, with Microsoft Teams record Experience field highlighted. The Experience value is set to AI native chat.](../images/na-deployment-channel-ai-native-exp.png)

-   **[Integrate ServiceNow Virtual Agent with Microsoft Teams](../task/add-msteams-snow-va-bot.md)**  
Add the Now Virtual Agent bot to your ServiceNow instance to integrate with Microsoft Teams.
-   **[Override Microsoft Teams integration](../task/override-msteams-install.md)**  
Override Virtual Agent integration with Microsoft Teams.
-   **[Manage the ServiceNow Virtual Agent integration with Microsoft Teams](../task/configure-va-teams.md)**  
Manage your ServiceNow® Virtual Agent bot branding and customize the bot messages in your ServiceNow instance after integration with Microsoft Teams.
-   **[Specialized Virtual Agent integrations for Microsoft Teams](specialized-va-integs-msteams.md)**  
The specialized Virtual Agent integrations for Microsoft Teams support different users as per their need.

**Parent Topic:**[Conversational Integration with Microsoft Teams](teams-conv-integration.md)

