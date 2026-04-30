---
title: Virtual Agent notifications supported in Microsoft Teams
description: Microsoft Teams app supports Virtual Agent notifications during conversations.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Virtual Agent feature support in Microsoft Teams conversations, Integrating Virtual Agent with Microsoft Teams, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent notifications supported in Microsoft Teams

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

**Parent Topic:**[Virtual Agent feature support in Microsoft Teams conversations](va-teams-other-features.md)

