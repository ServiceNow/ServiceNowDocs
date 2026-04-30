---
title: Configure actionable push notifications
description: Include actions with your push notifications. Users can perform push notification actions without opening the app.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
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

![image.actionable-notifications]

</td></tr></tbody>
</table>## Creating actionable push notifications

Create actionable push notifications using the following process:

1.  Create a push notification that your users will see on their mobile devices.

2.  Add a push action category to determine what actions your users can take in a notification.

3.  Create functions for each push action in the selected action category. These actions perform tasks on your instance based on what the user selects in the notification.

4.  Map functions with push actions on the actionable push notification. Associate functions to the actions in your notification so the instance uses the correct function for each action.

5.  Create push message content by creating a record to determine what information the notification displays to your users.

6.  Create a standard notification on your instance using the platform notifications.


