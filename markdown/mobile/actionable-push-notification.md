---
title: Configure actionable push notifications
description: Include actions with your push notifications. Users can perform push notification actions without opening the app.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure actionable push notifications

Include actions with your push notifications. Users can perform push notification actions without opening the app.

<table id="table_mtx_yvm_ylb"><tbody><tr><td>

Up to three actions can be associated with a push notification. These actions must refer to an existing mobile function. The following function types of actions are supported:

-   Action item
-   Navigation
-   URL
-   Chat launcher

</td><td>

![Actionable push notifications.](../image/actionable-notifications.png "Actionable push notification")

</td></tr></tbody>
</table>## Creating actionable push notifications

Create actionable push notifications using the following process:

1.  Create a push notification that your users will see on their mobile devices.

2.  Add a push action category to determine what actions your users can take in a notification.

3.  Create functions for each push action in the selected action category. These actions perform tasks on your instance based on what the user selects in the notification.

4.  Map functions with push actions on the actionable push notification. Associate functions to the actions in your notification so the instance uses the correct function for each action.

5.  Create push message content by creating a record to determine what information the notification displays to your users.

6.  Create a standard notification on your instance using the platform notifications.


-   **[Create an actionable push notification](../task/actionable-push-notification-1.md)**  
Create a push notification your users will see on their mobile devices.
-   **[Actionable push notification script example](../reference/actionable-push-notification-1a.md)**  
You can use this JSON script example to configure an actionable push notification for ServiceNow® mobile apps.
-   **[Add a push action category](../task/actionable-push-notification-2.md)**  
Select a push category to determine what actions your users can take in a notification. This category defines which actions your users can take when viewing a notification.
-   **[Create a push action](../task/actionable-push-notification-2-3.md)**  
Create push actions to suit your needs, when the base system actions do not meet your requirements.
-   **[Create functions for each push action](../task/actionable-push-notification-3.md)**  
Create mobile function for each function in the selected action category. These actions perform tasks on your instance based on what the user selects in the notification.
-   **[Map functions with push actions on the actionable push notification](../task/actionable-push-notification-4.md)**  
Associate functions to the actions in your notification so the instance uses the correct function for each action.
-   **[Create push message content](../task/actionable-push-notification-5.md)**  
Create a record to determine what information the notification displays to your users.
-   **[Create a standard notification](../task/actionable-push-notification-6.md)**  
Create a standard notification on your instance using the platform notifications.

**Parent Topic:**[Mobile push notifications](sg-mobile-push-notifications.md)

