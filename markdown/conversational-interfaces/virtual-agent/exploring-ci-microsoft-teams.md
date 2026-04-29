---
title: Exploring Conversational Integration with Microsoft Teams
description: Use the Conversational Integration with Microsoft Teams application to connect your end users with Virtual Agent or live agents through your company’s Microsoft Teams account.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Exploring Conversational Integration with Microsoft Teams

Use the Conversational Integration with Microsoft Teams application to connect your end users with Virtual Agent or live agents through your company’s Microsoft Teams account.

## Conversational Integration with Microsoft Teams users

|User|Description|
|----|-----------|
|admin or virtual\_agent\_admin|Create and publish Virtual Agent conversations.|
|admin.microsoft.com|A Microsoft 365 account with admin privileges is required to integrate Virtual Agent in Microsoft Teams.|

## Conversational Integration with Microsoft Teams workflow

Ensure that you have a Microsoft 365 account with admin privileges \(admin.microsoft.com accessible\). To install Conversational Integration with Microsoft Teams, you need the admin or virtual\_agent\_admin role.

![Workflow describing the sequence of processes carried out in Conversational Integration with Microsoft Teams.](../images/workflow-ci-ms-teams.png "Workflow of Conversational Integration with Microsoft Teams")

1.  [Install Conversational Integration with Microsoft Teams](../task/teams-install.md).
2.  Add integrations.
    -   **[Integrate with Virtual Agent](va-integ-msteams.md).**

        Manage and configure Virtual Agent settings.

    -   **[Integrate with a self-configured bot](va-integ-teams-self-configured-bot.md).**

        Create a bot in Microsoft Teams. Manage and configure the self-configured bot, then generate the manifest file. Upload the manifest file to Microsoft Teams. Configure Virtual Agent settings.

        **Note:** Verify that you enabled Message Extensions when generating the manifest file, and verify your bot name is one word.


## What to explore next

To learn more about configuring and using Conversational Integration with Microsoft Teams, see:

-   [Configure Virtual Agent for Microsoft Teams](../task/configure-va-msteams-settings.md).
-   [Enable Now Assist in Virtual Agent for Microsoft Teams](../task/enable-na-llm-teams.md).
-   [Integrate Now Assist in Virtual Agent with Microsoft Teams](../../now-assist-in-va/concept/integrating-now-assist-va-msteams.md).
-   [Integrate Now Assist in Virtual Agent with Microsoft Copilot](ms-copilot-na-va.md).

For more information about integrating Microsoft Copilot with Now Assist, see the following ServiceNow blog and community articles:

-   [https://www.servicenow.com/blogs/2024/now-assist-microsoft-copilot](https://www.servicenow.com/blogs/2024/now-assist-microsoft-copilot)
-   [https://www.servicenow.com/community/virtual-agent-nlu-articles/microsoft-copilot-integration-with-now-assist-faq-zurich-release/ta-p/3048238](https://www.servicenow.com/community/virtual-agent-nlu-articles/microsoft-copilot-integration-with-now-assist-faq-zurich-release/ta-p/3048238)

-   **[Plugins for Conversational Integration with Microsoft Teams](../reference/addtional-plugins-msteams.md)**  
Activate the Glide Virtual Agent \[com.glide.cs.chatbot\] plugin, the Conversational Integration with Microsoft Teams \[sn\_va\_teams\] plugin, and verify its additional plugins to enable other features for conversation design.

**Parent Topic:**[Conversational Integration with Microsoft Teams](teams-conv-integration.md)

