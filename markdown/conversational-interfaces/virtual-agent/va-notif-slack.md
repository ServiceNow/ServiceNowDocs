---
title: Virtual Agent notifications supported in Slack
description: Slack app supports Virtual Agent notifications during conversations.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [VA feature support in Slack conversations, Conversational Integration with Slack, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent notifications supported in Slack

Slack app supports Virtual Agent notifications during conversations.

-   Subscription management
    -   Requesters - Use the **notification** \(or **notifications**\) command to subscribe to or unsubscribe from notifications.
    -   Admins - Enable notifications for messaging users in the Messaging Apps Integration page.
-   Notification content - Create notifications with rich content, images, and action buttons. Actionable notifications enable recipients to perform certain actions and respond to the notification, such as adding a comment or requesting a live agent.
-   Notification delivery
    -   Message notifications are delivered immediately to end users, even if the user is chatting with a virtual or live agent.
    -   Actionable notifications are delivered only when the user is not in an active conversation with a virtual or live agent. Users can choose to:
        -   Review the notifications later by using the **show notification** command.

            For example, with the **show notification** command, users can select the notification they want to view.

            ![The user enters "show notification" in the Slack window, and the bot responds with, "Thanks, select the notification you'd like to view," followed by two choices.](../images/Show-Notification-Buttons-slack.png)

        -   Perform or skip the actions for the notification. If users decide to skip the actions, users can return later to the notification by using the **show notification** command.

For detailed information on Virtual Agent notifications, see [Configuring Virtual Agent notifications](configuring-va-notifications.md).

**Parent Topic:**[Virtual Agent features supported in Slack conversations](va-slack-other-features.md)

