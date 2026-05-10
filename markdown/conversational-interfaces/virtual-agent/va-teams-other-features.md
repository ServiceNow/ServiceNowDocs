---
title: Virtual Agent feature support in Microsoft Teams conversations
description: The Microsoft Teams app supports Virtual Agent features, such as Assistant Designer controls for creating conversations, notifications, AI Search results, and more.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Virtual Agent, feature, support, Microsoft Teams, MSTeams, Designer]
breadcrumb: [Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent feature support in Microsoft Teams conversations

The Microsoft Teams app supports Virtual Agent features, such as Assistant Designer controls for creating conversations, notifications, AI Search results, and more.

## Emojis and text

Starting with Version 4.0.1, when a user chats with a live agent and sends a message that contains emojis, the text gets delivered and the emoji is displayed on the agent workspace.

**Note:** Due to the difference in the platforms \(app or web browser\) used by the end user and the live agent, there's a difference between the emojis that are sent by the end user and the emojis that are received by the live agent.

A user can understand how emojis look like in a chat conversation and in the Agent Workspace from the following examples.

![Emojis appear in line with text as the user selects them.](../images/msteams-user-chat-emojis.png "Emojis in a chat conversation")

![Live agents may see slightly different emojis in Agent Workspace.](../images/msteams-agent-chat-emojis.png "Emojis in Agent Workspace")

## Message pagination

Microsoft Teams has a limit on the maximum message size before paginating the message. You can adjust the number of characters allowed in a message before paginating by going to the system properties \[sys\_properties\] table and setting the number in the system property **sn\_va\_teams.picker\_char\_limit**.

## AI Search results

Now Assist in Virtual Agent can generate AI Search results that are displayed as Genius result cards and multi-link outputs in conversations. For details on how Virtual Agent generates AI Search results, see [Improving the user experience with AI Search](va-ai-search.md). The default AI Search configuration for Virtual Agent enables search results for Q&amp;A \(Knowledge Base and catalog items\). The user has the option to like or dislike the information presented in the card. For more information, see [Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/genius-results-ais.md).

## URL navigation for chat links

In the Virtual Agent and Live Agent conversations on the Microsoft Teams app, the links to ServiceNow records open automatically in base system portals, including the links that are displayed in the output cards, Virtual Agent notifications, and AI Search results. If needed, as the administrator, you can change the portals where these links are opened in. For configuration details, see [Configure URL navigation for chat links](../../conversational-interfaces/task/ac-configure-url-navigation.md).

## Masking of sensitive user data

Starting with Version 2.0.0, passwords that are entered by users and confirmed in bot responses are masked during the password reset conversations in the Microsoft Teams app.

A user can understand how a password is masked in Microsoft Teams from the following example.

![When the user enters their password in a Microsoft Teams conversation, the characters are hidden by dots.](../images/pw-mask-teams.png "Example of password masking")

## Support for file uploads

Starting with Version 2.0.0, users can upload their file attachments with the paper clip icon ![Paper clip icon.](../images/paperclip.png) in the Microsoft Teams conversations.

A user can learn to attach an icon in the Microsoft Teams chat window from the following example.

![User selects the paper clip icon in the chat window to upload a file.](../images/teams-attach-icon.png "File attachment support")

## Trusted domains

The values that are specified in the Trusted media domains field of the Provider Channel Identities table \[sys\_cs\_provider\_application\] take precedence over the Connections table \[sys\_cs\_provider\] and overrides its values.

## Catalog opening experience in Microsoft Teams conversations

Starting with Version 4.1.0, users can request a catalog item from the Microsoft Teams app during a conversation.

A user can select the **Request this item** button in a conversation with Microsoft Teams that opens the catalog item in a pop-up window, the Task Module, where the user can view the information of the item and submit the request within Microsoft Teams.

The following examples show how a user can request and then view a catalog item.

![Catalog item displays on a card in the conversation. Users can select "Request this item" to open the pop-up window where they can complete the request.](../images/msteams-request-catalog.png "Request Catalog item")

![Catalog item displays in a pop-over window, where the user can view details and make the request.](../images/mstams-catalog-task-module.png "View Catalog item")

## Custom branding in the Microsoft Teams application

Microsoft Teams supports app customization, which enables you, as the administrator, to customize the branding of the Now Virtual Agent bot in the Conversational Integration with Microsoft Teams. To learn more about app customization, see these resources:

-   [Customize apps in Microsoft Teams](https://docs.microsoft.com/en-us/microsoftteams/customize-apps) in the Microsoft Teams documentation.
-   [MS Teams branding for the conversational integration](https://community.servicenow.com/community?id=community_article&sys_id=3b4f487edbe17490904fa9fb1396195b) in the ServiceNow Community.

## HTML rendering in Microsoft Teams

When a Virtual Agent sends a message in Microsoft Teams with HTML tags, only those HTML tags supported by Microsoft Teams are rendered as normal tags.

For more information about the Microsoft Teams supported HTML tags for bot messages, see [Formatting bot messages](https://learn.microsoft.com/en-us/microsoftteams/platform/resources/bot-v3/bots-text-formats).

## Custom controls in Microsoft Teams

Using the Custom Control utility will cause failure in Microsoft Teams conversations with the message `channel is not supported`. See [Custom control utility](../reference/va-custom-control-util.md) for more information on the utility.

-   **[Virtual Agent Designer user input and bot response controls in Microsoft Teams](va-designer-bot-controls.md)**  
The Virtual Agent Designer user input and bot response controls for creating conversation topics are supported in Microsoft Teams conversations, including the table bot response, the card control that can display images, and the image bot response controls.
-   **[Virtual Agent notifications supported in Microsoft Teams](va-notif-msteams.md)**  
Microsoft Teams app supports Virtual Agent notifications during conversations.
-   **[Unsupported Virtual Agent features in Microsoft Teams](../reference/limited-features-msteams.md)**  
Refer to the unsupported features of Virtual Agent in Conversational Integration with Microsoft Teams.
-   **[Capture common errors and provide resolution steps for Microsoft Teams using the Conversational Interfaces Diagnostic Tool](troubleshoot-msteams-diagnostic-tool.md)**  
The Conversational Interfaces Diagnostic Tool runs a health report to define and capture information for different categories of the Conversational Integration with Microsoft Teams app, such as plugin details, configuration settings, system properties, integration failures, and so on, and lets the user validate and review these settings to start a bot-conversation.

**Parent Topic:**[Conversational Integration with Microsoft Teams](teams-conv-integration.md)

