---
title: Configure push applications for iOS branded apps using a token
description: Use push notifications on your branded ServiceNow mobile apps for iOS using token-based authentication.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Push notifications, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure push applications for iOS branded apps using a token

Use push notifications on your branded ServiceNow mobile apps for iOS using token-based authentication.

## Before you begin

Create an [Apple](https://developer.apple.com/) developer account.

Ensure you have your Team ID, Key ID, and signing key from Apple. For more information, see the Apple developer documentation topic [Obtain an Encryption Key and Key ID from Apple](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_token-based_connection_to_apns#2943371).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Application**.

2.  Open the record for the push application that you want to modify.

    -   For the Mobile Agent app, select **ServiceNow Mobile Application**.
    -   For the Now Mobile app, select **ServiceNow Request Application**.
    If you are using a branded mobile application, select the record for the branded app. For example, select **ServiceNow Intune Mobile Application** if you are using the Microsoft Intune branded application.

3.  In the **Push** field, change the value to **Direct**.

4.  In **Apple Authentication Type** field, select **Token Based**.

5.  In the Apple-Token Based Authentication tab, select the reference icon \(![Reference icon](../image/reference-lookup-icon.png)\) next to the **Push Token Auth** field.

6.  In the Push Token Based Authentication list, select **New**.

7.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|Name for your token.|
    |Team Id|Unique identification code provided by Apple.|
    |Key Id|The 10-character Key ID you obtained from your developer account.|
    |Signing Key|An authentication token signing key, consisting of the content of the `.p8` text file.|

    **Note:**

    For each Apple developer account using the Team ID and Key ID, you can generate two signing keys. Apps created are mapped to the same Team ID and Key ID.

    One combination can be used for one instance only. For example, the combination used for a test instance can’t be used for a production instance and vice versa.

8.  Select **Submit**.

9.  On the push application form, select **Update**.


**Parent Topic:**[Mobile push notifications](../concept/sg-mobile-push-notifications.md)

