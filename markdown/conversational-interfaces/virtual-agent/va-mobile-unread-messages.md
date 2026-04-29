---
title: Now Mobile notification of unread chat and Virtual Agent messages
description: When Now Mobile app users navigate away from the app after starting an active conversation, they can automatically receive Virtual Agent mobile push notifications informing them of new, unread chat messages and  Virtual Agent notifications that have arrived.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Mobile, Virtual Agent, notifications, Android, iOS]
breadcrumb: [Configure Virtual Agent for a mobile application, Configure, Virtual Agent, Conversational Interfaces]
---

# Now Mobile notification of unread chat and Virtual Agent messages

When Now® Mobile app users navigate away from the app after starting an active conversation, they can automatically receive Virtual Agent mobile push notifications informing them of new, unread chat messages and  Virtual Agent notifications that have arrived.

Now Mobile users might need to leave an active conversation for various reasons. They could be waiting for an available agent and decide to handle other tasks instead. Or, they could be engaged in a long-running \(asynchronous\) conversation and do not need to be online concurrently with an agent. Now Mobile users can check Virtual Agent push notifications to get timely information about their current conversations when they’re away from the app. These push notifications enable them to stay engaged with live and virtual agents and avoid unnecessary conversation closures \(timeouts\).

## Enabling Virtual Agent message push notifications

To receive Virtual Agent mobile push notifications, your users must enable push notifications for the Now Mobile app on their iOS or Android devices.

In base system instances, the Virtual Agent Message Push notification is automatically enabled for all Now Mobile users. Users can modify their [notification preferences](https://www.servicenow.com/docs/access?context=next-experience-notifications-preferences&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) by navigating to **All** &gt; **Self-Service** &gt; **My Notification Preferences**.

![In Notifications settings, users can toggle the Push option to turn on or turn off mobile push notifications.](../images/va-mobile-push-notif-pref.png)

## How Virtual Agent mobile push notifications work

Virtual Agent push notifications display information about incoming, unread chat messages from agents and any Virtual Agent messages. The push notifications are listed in the notification center \(lock screen\) of mobile devices. Users tap a push notification in the list to open the Now Mobile app and continue the corresponding conversation.

![1. Virtual Agent push notification displays in the mobile banner. 2. The user taps the notification on the screen. 3. The chat opens in the mobile app.](../images/mobile-chat-notif.png "Example Virtual Agent push notifications in the Now Mobile app")

**Note:** Virtual Agent push notifications are not displayed under the **notifications** tab in the Now Mobile app. These push notifications also do not generate associated badge numbers on the Now Mobile app icon. However, badge numbers are displayed on the Virtual Agent quick launch icon within the app.

To process unread chat or Virtual Agent messages and deliver them to Now Mobile users, the system does the following:

-   Checks which user accounts are registered to receive push notifications.
-   Determines the mobile clients \(devices\) that are not in use.
-   Runs the **Generate Virtual Agent Push Notification** scheduled job every 60 seconds to:
    -   Identify and batch new unread messages.
    -   Add unread messages records to the Push Notifications \[sys\_cs\_message\_notification\] table, which generates the Virtual Agent push notifications.
    -   Delivers Virtual Agent push notifications to Now Mobile users away from the app.

        Depending on when the **Generate Virtual Agent Push Notification** scheduled job processes new unread messages, push notifications might not arrive in the order that they were generated, and it might take slightly longer than one minute for push notifications to arrive.


## Virtual Agent push notification message content

The content of Virtual Agent push notification messages sent to Now Mobile users reflects the actual text from the live or virtual agent. If a text representation of the message, such as a rich control, cannot be generated, the text `New Message` is displayed instead.

**Note:** System action messages that are displayed to users during live chat or virtual agent conversations are not included in Virtual Agent push notifications or in the count of unread messages. The exception is the system message for the live agent timeout: `The conversation is timing out, are you still there?` This message is sent as a push notification since it is time-sensitive and informs users that the conversation might be closed if they do not respond.

**Parent Topic:**[Configure Virtual Agent for a ServiceNow mobile application](../task/configure-va-mobile-web-client.md)

