---
title: Virtual Agent feature support in Microsoft Teams conversations
description: The Microsoft Teams app supports Virtual Agent features, such as Virtual Agent Designer controls for creating conversations, notifications, AI Search results, and more.The Virtual Agent Designer user input and bot response controls for creating conversation topics are supported in Microsoft Teams conversations, including the table bot response, the card control that can display images, and the image bot response controls.Microsoft Teams app supports Virtual Agent notifications during conversations.Refer to the unsupported features of Virtual Agent in Conversational Integration with Microsoft Teams.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-08-06"
reading_time_minutes: 8
keywords: [Virtual Agent, feature, support, Microsoft Teams, MSTeams, Designer]
breadcrumb: [Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent feature support in Microsoft Teams conversations

The Microsoft Teams app supports Virtual Agent features, such as Virtual Agent Designer controls for creating conversations, notifications, AI Search results, and more.

## Emojis and text

Starting with Version 4.0.1, when a user chats with a live agent and sends a message that contains emojis, the text gets delivered and the emoji is displayed on the agent workspace.

**Note:** Due to the difference in the platforms \(app or web browser\) used by the end user and the live agent, there's a difference between the emojis that are sent by the end user and the emojis that are received by the live agent.

A user can understand how emojis look like in a chat conversation and in the Agent Workspace from the following examples.

![Emojis appear in line with text as the user enters them.](../images/msteams-user-chat-emojis.png "Emojis in a chat conversation")

![Live agents may see slightly different emojis in Agent Workspace.](../images/msteams-agent-chat-emojis.png "Emojis in Agent Workspace")

## Message pagination

Microsoft Teams has a limit on the maximum message size before paginating the message. You can adjust the number of characters allowed in a message before paginating by going to the system properties \[sys\_properties\] table and setting the number in the system property **sn\_va\_teams.picker\_char\_limit**.

## AI Search results

Now Assist in Virtual Agent can generate AI Search results that are displayed as Genius result cards and multi-link outputs in conversations. For details on how Virtual Agent generates AI Search results, see [Improving the user experience with AI Search](va-ai-search.md). The default AI Search configuration for Virtual Agent enables search results for Q&amp;A \(Knowledge Base and catalog items\). The user has the option to like or dislike the information presented in the card. For more information, see [Genius Results](https://www.servicenow.com/docs/access?context=genius-results-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## URL navigation for chat links

In the Virtual Agent and Live Agent conversations on the Microsoft Teams app, the links to ServiceNow records open automatically in base system portals, including the links that are displayed in the output cards, Virtual Agent notifications, and AI Search results. If needed, as the administrator, you can change the portals where these links are opened in. For configuration details, see [Configure URL navigation for chat links](../../conversational-interfaces/task/ac-configure-url-navigation.md).

## Masking of sensitive user data

Starting with Version 2.0.0, passwords that are entered by users and confirmed in bot responses are masked during the password reset conversations in the Microsoft Teams app.

A user can understand how a password is masked in Microsoft Teams from the following example.

![When the user enters their password in a Microsoft Teams conversation, the characters are hidden by dots.](../images/pw-mask-teams.png "Example of password masking")

## Support for file uploads

Starting with Version 2.0.0, users can upload their file attachments with the paper clip icon ![Paperclip icon](../../conversational-interfaces/image/paperclip.png) in the Microsoft Teams conversations.

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

When a Virtual Agent sends a message in Microsoft Teams with HTML tags, only those HTML tags supported by Microsoft Teams are rendered as normal tags for a great conversational experience to the end user. For more information about the Microsoft Teams supported HTML tags for bot messages, see [Formatting bot messages](https://learn.microsoft.com/en-us/microsoftteams/platform/resources/bot-v3/bots-text-formats).

## Custom controls in Microsoft Teams

Using the Custom Control utility will cause failure in Microsoft Teams conversations with the message `channel is not supported`. See [Custom control utility](../reference/va-custom-control-util.md) for more information on the utility.

## Virtual Agent Designer user input and bot response controls in Microsoft Teams

The Virtual Agent Designer user input and bot response controls for creating conversation topics are supported in Microsoft Teams conversations, including the table bot response, the card control that can display images, and the image bot response controls.

Starting with Version 2.0.0, the updated card and new video bot response controls are supported in Microsoft Teams conversations. The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

For more information about user input controls and bot responses, see [Virtual Agent Designer user input controls](../reference/va-user-inputs.md) and [Virtual Agent Designer bot responses](../reference/va-bot-responses.md), respectively.

Starting with Version 3.0.10, to improve the bot performance and enable a better conversational experience with Virtual Agent on Microsoft Teams, the non-card bot response controls such as text, links, and date cards are converted into adaptive cards.

As part of converting all controls to adaptive cards, the content displayed on notifications received through bot responses is customized. The Microsoft Teams bot displays a preview of the notification content on the card, such as the message content, card title, or description, where applicable.

![In Microsoft Teams, this notification shows the title "New Date/Time" and a date/time picker to schedule an appointment. When done, the user selects the Submit button.](../images/notification-title-msteams.png "Notification with title")

Starting with Version 3.0.10, during a conversation with the Microsoft Teams bot, you can search for a particular choice from the list using the drop-down picker controls.

![Start typing in the choice list to find the correct response. For example, start typing "s" to find the "Software" choice.](../images/msteams-type-head-option.png)

Starting from Version 4.1.0, you have the option to turn off the confirmation banner that appears when you send a response to Virtual Agent in Microsoft Teams conversation.

Set the **sn\_va\_teams.hide\_teams\_response\_message** system property value to **true** to turn off the confirmation banner \(by default the value of the system property is set to **false**\).

## Virtual Agent notifications supported in Microsoft Teams

Microsoft Teams app supports Virtual Agent notifications during conversations.

-   Subscription management
    -   Requesters - Use the **notification** \(or **notifications**\) command to subscribe to or unsubscribe from notifications.
    -   Admins - Enable notifications for messaging users in the Messaging Apps Integration page.
-   Notification content - Create notifications with rich content, images, and action buttons. Actionable notifications enable recipients to perform certain actions and respond to the notification, such as adding a comment or requesting a live agent.
-   Notification delivery
    -   Message notifications are delivered immediately to end users, even if the user is chatting with a virtual or live agent.
    -   Actionable notifications are delivered only when the user is not in an active conversation with a virtual or live agent. Users can do the following:
        -   Review the notifications later by using the **show notification** command.

            ![The user enters "show notification" in the chat window, and the bot responds with, "Thanks, select the notification you'd like to view," followed by three choices.](../images/shw-notifications-teams.png "Show notifications in Microsoft Teams")

        -   Perform or skip the actions for the notification. If users decide to skip the actions, users can return later to the notification by using the **show notification** command.

For detailed information on Virtual Agent notifications, see [Configuring Virtual Agent notifications](configuring-va-notifications.md).

## Unsupported Virtual Agent features in Microsoft Teams

Refer to the unsupported features of Virtual Agent in Conversational Integration with Microsoft Teams.

### Unsupported features

Virtual Agent does not support the following functionalities during a conversation in Microsoft Teams.

-   Connect Support
-   Geo-location topic block

