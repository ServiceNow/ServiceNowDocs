---
title: Integrating Virtual Agent with Microsoft Teams
description: Enable requesters to chat with Microsoft Teams or live agents using the Microsoft Teams application. Use the Conversational Integration with Microsoft Teams app, available from the ServiceNow Store, to associate your instance with Microsoft Teams.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Integrating Virtual Agent with Microsoft Teams

Enable requesters to chat with Microsoft Teams or live agents using the Microsoft Teams application. Use the Conversational Integration with Microsoft Teams app, available from the ServiceNow Store, to associate your instance with Microsoft Teams.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Use the Conversational Integration with Microsoft Teams application to connect your end users with Virtual Agent or live agents through your company’s Microsoft Teams account. To get started, see [Install Conversational Integration with Microsoft Teams](../task/teams-install.md).

**Important:**

-   If your instance is in our GovtCommunityCloud \(GCC\) environment, see to [Integrating Virtual Agent with Microsoft Teams using the self-configured bot](va-integ-teams-self-configured-bot.md) for more information.
-   If your instance is in our Australia SPP \(ServiceNow Protected Platform\) environment, see [Enable Microsoft Teams integration in ServiceNow Protected Platform \(SPP\)](enable-msteams-integ-spp.md) for more information.
-   The Microsoft Teams Graph spoke consumes Integration Hub transactions, thus, usage of Virtual Agent in Microsoft Teams does count against Integration Hub transactions. Microsoft is also monetizing Microsoft Teams API usage, therefore such usage will also count against their Microsoft 365 subscription. For further information, see [Sidebar and Microsoft Teams](../../conversational-interfaces/concept/sidebar-teams-overview.md).

![Workflow describing the sequence of processes carried out in Conversational Integration with Microsoft Teams.](../images/workflow-ci-ms-teams.png "Workflow of Conversational Integration with Microsoft Teams")

-   **[Integrating ServiceNow Virtual Agent with Microsoft Teams](va-integ-msteams.md)**  
Enables ServiceNow Virtual Agent to integrate with Microsoft Teams application.
-   **[Specialized Virtual Agent integrations for Microsoft Teams](specialized-va-integs-msteams.md)**  
The specialized Virtual Agent integrations for Microsoft Teams support different users as per their need.
-   **[Configure Virtual Agent for Microsoft Teams](../task/configure-va-msteams-settings.md)**  
Configure your Microsoft Teams bots that are integrated with Virtual Agent to enable notifications, to link ServiceNow user profiles, and to set up system messages and contextual actions.
-   **[Using Now Assist in Virtual Agent conversations with Microsoft Teams](na-va-llm-teams.md)**  
The Now Assist provides you with the large language model \(LLM\)-based conversational experience during your conversations with a Now Virtual Agent bot or a Self-configured bot that is integrated with Microsoft Teams.
-   **[Virtual Agent feature support in Microsoft Teams conversations](va-teams-other-features.md)**  
The Microsoft Teams app supports Virtual Agent features, such as Virtual Agent Designer controls for creating conversations, notifications, AI Search results, and more.
-   **[Capture common errors and provide resolution steps for Microsoft Teams using the Conversational Interfaces Diagnostic Tool](troubleshoot-msteams-diagnostic-tool.md)**  
The Conversational Interfaces Diagnostic Tool runs a health report to define and capture information for different categories of the Conversational Integration with Microsoft Teams app, such as plugin details, configuration settings, system properties, integration failures, and so on, and lets the user validate and review these settings to start a bot-conversation.
-   **[Remove Conversational Integration with Microsoft Teams](../task/uninstall_va_msteams.md)**  
Remove the integrations between your ServiceNow Virtual Agent bot or the Self-configured bots and Microsoft Teams to disassociate the app with your ServiceNow instance.

**Parent Topic:**[Integrating Virtual Agent with messaging apps](va-integration-messaging-apps.md)

