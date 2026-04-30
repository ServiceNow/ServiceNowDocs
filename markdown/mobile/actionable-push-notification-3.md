---
title: Create functions for each push action
description: Create mobile function for each function in the selected action category. These actions perform tasks on your instance based on what the user selects in the notification.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure actionable push notifications, Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Create functions for each push action

Create mobile function for each function in the selected action category. These actions perform tasks on your instance based on what the user selects in the notification.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Functions**.

2.  Click **New** to create a new function record.

3.  Create a new function for one of your push actions. When selecting a function type in the **Type** field, you must select one of the type supported for actionable push notifications.

    -   Action item
    -   Navigation
    -   URL
    -   Chat launcher
    For information on function types, and detailed steps for creating functions, see [Mobile functions](../concept/sg-studio-mobile-button-types.md).

4.  Create additional functions for each push action.

    For example, if you have selected `ack-escalate-ignore-back` as your push notification category, your notification displays **Acknowledge**, **Escalate** and **Ignore** buttons. You need to create a function to determine the behavior of each of these buttons.


## Result

You have functions to perform actions for each of the buttons that display in your push notification. In the next steps, you will associate these functions to the notification actions so your functions trigger when users tap the buttons.

**Parent Topic:**[Configure actionable push notifications](../concept/actionable-push-notification.md)

