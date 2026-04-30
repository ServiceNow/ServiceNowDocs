---
title: Mobile critical alerts
description: Send your users critical alerts, even if they set their mobile device to Do Not Disturb or Silent mode. Configure these visual and audio alerts to be sent when an issue needs immediate attention. Example scenarios can be to inform the user of an essential update, or to publicize a major incident that requires a speedy response.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile critical alerts

Send your users critical alerts, even if they set their mobile device to Do Not Disturb or Silent mode. Configure these visual and audio alerts to be sent when an issue needs immediate attention. Example scenarios can be to inform the user of an essential update, or to publicize a major incident that requires a speedy response.

## Before you begin

Role required: admin

## About this task

This task describes how to create a critical alert from an existing push notification. To create a push notification from scratch, see [Mobile push notifications](../concept/sg-mobile-push-notifications.md).

**Note:**

-   For users to receive critical alerts, the feature must be enabled on the user’s mobile device. If the feature is not enabled, the critical alert is delivered as a regular push notification, however it is labeled as critical in the notifications area. For more information, see the user-related topic, [Enabling critical alerts](../reference/critical-alert-enable.md).
-   On the Android platform, when a user receives a critical alert on certain phone types, they may experience the following device behavior:

    -   **OnePlus devices with hardware-controlled ringer mode:**

        On devices like OnePlus where the ringer mode is controlled by a physical switch, the app might not be able to override the notification sound volume if the device is set to silent or vibrate mode.

    -   **OnePlus or Oppo device Do Not Disturb mode behavior:**

        On certain devices, like Oppo and OnePlus, if Do Not Disturb \(DND\) mode is enabled, the DND setting might be temporarily turned off until the critical notification sound has finished playing.


## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select Notification \[sysevent\_email\_action\] and then select an existing push notification event.

    This is the notification record that you define with a critical status.

    **Note:** If you want to create a push notification from scratch, refer to [Mobile push notifications](../concept/sg-mobile-push-notifications.md). You then must follow these subsequent steps to define the push notification as critical.

5.  Select the Push notification message content record within the Push notification event.

    ![Location of the push notification message content in the MAB hierarchy tree.](../image/push-notif-mess-content.png)

6.  Within the **Push message content** area, define and configure your critical alert.

    For information on how to configure a critical alert, see [Configure code for critical alerts](../reference/mobile-citical-alert-code.md).

7.  Select **Save**.

8.  Complete these steps if you need the same push notification to be pushed to different mobile applications.

    1.  Select the Push notification message you want to duplicate.
    2.  Select the more button \(![More button.](../image/mab-button-more.png)\) and select **Duplicate**.

        The Create a push notification message window displays.

    3.  Rename the name of the copied notification in the **Push notification message name** field, and select **Create**.
    4.  Select the **Go to record** button in the Success window.

        A duplicate of both the push notification message record and the push notification message content record are created.

    5.  Select the push notification message record, and in the **Application to push notification** field in the **Settings** section, select which other application you want the critical notification message sent to.
    6.  Select the push notification message content record.
    7.  In the **Push app** field in the Push application area, select the same application you selected for the push notification message record.
    8.  In the Pull message content area, you have the option to edit the critical alert parameters.

        **Note:** If the push message content contains a mobile deep link in the code, then you must change the application this alert is used for, either `Request` or `Agent`. Mobile deep links are written in the code as `MobileDeepLinkGenerator('<application type>')`. For more information, see [Mobile deep link structure](../reference/deep-link-mobile-structure.md).

    9.  Select **Save**.
    10. Repeat these steps for each mobile application where you want to add a critical notification.

-   **[Configure code for critical alerts](../reference/mobile-citical-alert-code.md)**  
You can make a push notification into a critical alert with the addition of some JSON code. Different JSON code is used for iOS and Android operating systems and for the ITSM business unit.

**Parent Topic:**[Mobile push notifications](../concept/sg-mobile-push-notifications.md)

