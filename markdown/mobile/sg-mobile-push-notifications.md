---
title: Mobile push notifications
description: Mobile push notifications are configurable pushed messages that appear directly in a mobile app. These push notifications are non-actionable or actionable, and are configured by administrators to meet the needs of their users.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile push notifications

Mobile push notifications are configurable pushed messages that appear directly in a mobile app. These push notifications are non-actionable or actionable, and are configured by administrators to meet the needs of their users.

Non-actionable notifications are created by configuring a mobile push notification and then using the mobile deep link generator to generate links that navigate users into any screen type within a mobile app. To learn more about the mobile deep link generator, see [Deep linking for mobile](deep-link-mobile.md).

Actionable push notifications require you to perform additional steps, such as mapping functions for each push action. For more information about actionable notifications, see [Configure actionable push notifications](actionable-push-notification.md).

Define push notifications as critical when you require users to be immediately alerted to an event. Critical alerts override Do Not Disturb or Silent mode settings on your users' mobile device. For more information, see [Mobile critical alerts](../task/mobile-critical-alerts-create.md).

You can target mobile push notifications for any of the specific ServiceNow Mobile Platform mobile apps.

## Push notifications structure overview

![Diagram showing how push notifications are created in an instance and sent directly to users to interact with on the device of their choice.](../image/SNMobileAppPushNotificationStructureOverview.png)

You must configure mobile push notifications in your ServiceNow instance before they can be sent to users on their mobile devices.

## Add push notifications to mobile apps with Mobile App Builder

In the Washington DC family release and later, you can now add push notifications to your mobile apps with Mobile App Builder:

![Mobile app builder menu showing available push notifications](../image/push-notif-in-mab.png)

Select **Mobile notifications** in the menu and then select the push notification you want to use. For more information about Mobile App Builder, see [Mobile App Builder](mab-concept.md).

-   **[Mobile push notification components](configure-mobile-push-notifications.md)**  
Configure mobile push notifications to target a specific screen in one of the ServiceNow Mobile Platform applications.
-   **[Reuse push notifications across mobile apps](../task/add-push-notifications-mobile-apps.md)**  
Reuse push notifications across mobile apps with Mobile App Builder \(MAB\). Push notifications are configurable pushed messages that appear directly in mobile apps. Using MAB to manage push notifications streamlines your mobile application development into one tool.
-   **[Configure push applications for iOS branded apps using certificate based authentication](../task/sg-push-setup-ios.md)**  
Install an iOS push certificate to use push notifications on your branded ServiceNow mobile apps for iOS.
-   **[Configure push applications for iOS branded apps using a token](../task/config-push-ios-token.md)**  
Use push notifications on your branded ServiceNow mobile apps for iOS using token-based authentication.
-   **[Configure push applications for Android branded apps using HTTP v1](../task/config-push-setup-android-httpv1.md)**  
Enter your Google Firebase Cloud Messaging push token authentication in your push application record to use push notifications on your branded ServiceNow mobile apps for Google Android.
-   **[Configure actionable push notifications](actionable-push-notification.md)**  
Include actions with your push notifications. Users can perform push notification actions without opening the app.
-   **[Configure notifications for mobile activity stream mentions](notification-activity-stream.md)**  
Configure your instance to send an email notification or a push notification when a user mentions a contact’s name within a mobile activity stream record.
-   **[Mobile critical alerts](../task/mobile-critical-alerts-create.md)**  
Send your users critical alerts, even if they set their mobile device to Do Not Disturb or Silent mode. Configure these visual and audio alerts to be sent when an issue needs immediate attention. Example scenarios can be to inform the user of an essential update, or to publicize a major incident that requires a speedy response.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

