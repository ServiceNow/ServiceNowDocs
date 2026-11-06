---
title: Notifications in Arc
description: Arc lets you know when an action is waiting for your approval or response, or when a schedule is due, even when you're working in another chat or another app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/notifications-arc.html
release: australia
topic_type: concept
last_updated: "2026-10-26"
reading_time_minutes: 2
keywords: [notifications, desktop notifications, in app banner, pending approvals, reminders, awaiting input, schedule notifications]
breadcrumb: [Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Notifications in Arc

Arc lets you know when an action is waiting for your approval or response, or when a schedule is due, even when you're working in another chat or another app.

## Types of notifications

Arc reaches you in two ways, depending on where you are.

-   **In app banner**

    Appears at the top of the Arc window when you're in a different chat from the one that needs you. The banner names the action, shows how long you have to respond, and lets you approve or reject it without switching chats.

-   **Desktop notification**

    Appears from your operating system when you're working in another app. It names the action and the chat, says Arc needs your permission to continue, and lets you approve or reject the action from the notification.

    **Note:** Desktop notifications are available on macOS only. On Windows, Arc uses in app banners.


## What you're notified about

-   **Pending approvals**

    An action is waiting for you to approve it before it times out. You get one notification for each approval. If the approval times out, the notification updates so you can still resume the task.

-   **Awaiting input**

    Arc is waiting for your response, such as when it asks whether a draft looks right before it sends it.

-   **Schedules or reminders**

    A scheduled job or reminder you asked Arc to set is due, at the time you chose.


## Notification settings

You choose which notifications you get in Arc settings. One setting turns all desktop notifications on or off, and separate settings control notifications for approvals, requests for your input, and schedules. You can also choose how long Arc waits before it notifies you about approvals and input requests. For macOS, the settings must allow Arc to show notifications. For more information, see [Turn notifications on or off in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/manage-notification-settings.md).

While notifications are off, Arc shows a prompt in the app that offers to turn them on. On macOS, turning them on also asks macOS for permission. If you choose not to turn them on, the prompt doesn't appear again, and you can turn notifications on later in settings.

-   **[Turn notifications on or off in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/manage-notification-settings.md)**  
Choose whether Arc notifies you about approvals, requests for your input, and schedules, and check that macOS lets Arc show notifications.
-   **[Approve or reject an action from a notification in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/respond-approval-notification.md)**  
Respond to an action that's waiting for your approval from an in app banner or a desktop notification, without going back to the chat it came from.

**Parent Topic:**[Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)

