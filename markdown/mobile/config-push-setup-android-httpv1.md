---
title: Configure push applications for Android branded apps using HTTP v1
description: Enter your Google Firebase Cloud Messaging push token authentication in your push application record to use push notifications on your branded ServiceNow mobile apps for Google Android.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Push notifications, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure push applications for Android branded apps using HTTP v1

Enter your Google Firebase Cloud Messaging push token authentication in your push application record to use push notifications on your branded ServiceNow mobile apps for Google Android.

## Before you begin

To use push notifications on your branded ServiceNow mobile apps for Android, you must enter your Google Firebase Cloud Messaging HTTP v1 API in your push application record. For information about generating the service account JSON in your Firebase console, see ServiceNow knowledge base article [KB1639289](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1639289). You must be logged in to your ServiceNow support account to access this information.

**Note:** These steps are only necessary if you're using a custom branded mobile app. For more detail on custom branding, see [Request, test, and publish a branded mobile app](../concept/request-test-pub-branded-mob-app.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Application**.

2.  Open the record for the push application you want to modify.

    -   Open **ServiceNow Mobile Application** for the Mobile Agent app.
    -   Open **ServiceNow Request Application** for the Now Mobile app.
    If you are using a branded mobile application, select the record for the branded app. For example, select **ServiceNow Intune Mobile Application** if you are using the Microsoft Intune branded application.

3.  In the **Push** field, change the value to **Direct**.

4.  In the **Google Authentication Type** field, change the value to **HTTP V1 Oauth**.

5.  On the **Google-HTTP V1 API** tab, copy the JSON content from your private key file obtained from the service account.

6.  Select **Submit**.


**Parent Topic:**[Mobile push notifications](../concept/sg-mobile-push-notifications.md)

