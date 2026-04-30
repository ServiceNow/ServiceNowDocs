---
title: Register the standard push notification
description: Register your standard push notification in a push application to use it in your mobile apps.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile push notification components, Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Register the standard push notification

Register your standard push notification in a push application to use it in your mobile apps.

## Before you begin

Role required: admin

The push application handles sending notifications to mobile devices. Add your new notification to the **ServiceNow Mobile Application** push application so your mobile app users start receiving this notification.

## Procedure

1.  Switch to the **Global** scope.

2.  Navigate to **System Notification** &gt; **Push Application**.

3.  Open the record for the push application you want to modify.

    -   Open **ServiceNow Mobile Application** for the Mobile Agent app.
    -   Open **ServiceNow Request Application** for the Now Mobile app.
    -   Open **ServiceNow Onboarding Mobile Application** for the Mobile Onboarding app.
    If you are using a branded mobile application, select the record for the branded app. For example, select **ServiceNow Onboarding Intune Mobile Application** if you are using the Microsoft Intune branded application.

4.  Right-click the record header and choose **Configure** &gt; **Related Lists** from the menu.

5.  Add **Push Default Registration** &gt; **Push Application** to the list on the right, and then select **Save**.

6.  In the **Push Default Registrations** related list, click the **New** button to create a new **Push Default Registration** record.

7.  In the **Notification** field, select the notification you created in the previous steps.

8.  Click **Submit**.

    Your push message is rendered on mobile devices that it is registered to. To see how push notifications appear to end users, see [Mobile push notifications](../concept/sg-mobile-push-notifications.md).


**Parent Topic:**[Mobile push notification components](../concept/configure-mobile-push-notifications.md)

