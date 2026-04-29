---
title: Exploring Conversational Integration with Workplace from Facebook
description: The Conversational Integration with Workplace from Facebook app supports Virtual Agent features such as Virtual Agent Designer controls for creating conversations, notifications, AI Search results, and more.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Conversational Integration with Workplace from Facebook, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Exploring Conversational Integration with Workplace from Facebook

The Conversational Integration with Workplace from Facebook app supports Virtual Agent features such as Virtual Agent Designer controls for creating conversations, notifications, AI Search results, and more.

**Note:** The Conversational Integration with Workplace from Facebook is not supported for on-prem instances.

This section highlights relevant Virtual Agent features that are supported in the Workplace from Facebook app.

## Virtual Agent Designer user input and bot response controls

The Virtual Agent Designer user input and bot response controls for creating conversation topics are supported in Workplace conversations, including the table bot response and the card control that can display images.

Starting with Version 2.0.0, the card and video bot response controls are supported in Workplace conversations. The video control displays a thumbnail image of the video that users can select to open the video in their preferred web browser.

For more information about user input controls and bot responses, see [Assistant Designer user input controls](../reference/va-user-inputs.md) and [Assistant Designer bot responses](../reference/va-bot-responses.md), respectively.

## AI Search results

Virtual Agent can generate AI Search results that are displayed as Genius Result Cards and multi-link outputs in conversations. For details on how Virtual Agent generates AI Search results, see [Improving the user experience with AI Search](va-ai-search.md). The default AI Search configuration for Virtual Agent enables search results for Q&amp;A \(knowledge base\) and Catalog items.

## Virtual Agent notifications

For detailed information on Virtual Agent notifications, see [Configuring Virtual Agent notifications](configuring-va-notifications.md).

-   Subscription management
    -   Requesters - Use the **notification** \(or **notifications**\) command to subscribe to or unsubscribe from notifications.
    -   Admins - Enable notifications for messaging users in the Messaging Apps Integration page.
-   Notification content - Create notifications with rich content, images, and action buttons. Actionable notifications enable recipients to perform certain actions and respond to the notification, such as adding a comment or requesting a live agent.
-   Notification delivery
    -   Message notifications are delivered immediately to end users, even if the user is chatting with a virtual or live agent.
    -   Actionable notifications are delivered only when the user is not in an active conversation with a virtual or live agent. Users can:
        -   Review the notifications later by using the **show notification** command.

            For example, with the **show notification** command, users can view their notifications.

            ![The user enters "show notification" in the chat window, and the bot responds with, "Thanks, select the notification you'd like to view," followed by three choices.](../images/show-notifications-workplace.png)

        -   Perform or skip the actions for the notification. If users decide to skip the actions, users can return later to the notification by using the **show notification** command.

## URL navigation for chat links

In Virtual Agent and Live Agent conversations on the Workplace app, links to ServiceNow records open automatically in base system portals—including links displayed in output cards, Virtual Agent notifications, and AI Search results. If needed, admins can change the portals in which these links are opened. For configuration details, see [Configure URL navigation for chat links](../../conversational-interfaces/task/ac-configure-url-navigation.md).

## Trusted Domains

In custom chat integrations, the values specified in the Trusted media domains field of the Provider Channel Identities table \[sys\_cs\_provider\_application\] takes precedence over the Connections table \[sys\_cs\_provider\] and hence overrides.

## Unsupported features

-   Promoted topics and Connect Support are not supported.
-   Geolocation topic block is not supported.
-   Account pre-linking is not supported in Workplace from Facebook.

**Parent Topic:**[Conversational Integration with Workplace from Facebook](../task/mssg-workplace.md)

