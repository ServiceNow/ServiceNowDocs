---
title: Create a push application record for your custom app
description: Register your customized mobile application with your instance to receive push notifications for the application.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setup using custom push app, Push notifications, System notifications, Notifications, Configure core features, Administer]
---

# Create a push application record for your custom app

Register your customized mobile application with your instance to receive push notifications for the application.

## Before you begin

Complete the following:

1.  [Activate push notifications](t_ActivatePushNotifications.md)
2.  \(iOS only\) [Upload a push certificate to your instance](upload-push-cert.md)

Role required: admin or push\_admin

**Note:** This process describes configuration used in the ServiceNow mobile app. Push Notification configuration for the current ServiceNow mobile UI can be found at [Mobile push notifications](https://www.servicenow.com/docs/access?context=sg-mobile-push-notifications&version=zurich&pubname=zurich-mobile&ft:locale=en-US)

## About this task

Push notifications are application-specific: They are sent to one type of mobile application, regardless of how many users have this application installed. If you develop your own mobile application, you must configure it for use by creating a record for it in the Push Application \[sys\_push\_application\] table. By default, ServiceNow mobile applications are automatically set up and ready to use.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Application**, and then click **New**.

2.  On the form, fill in the fields.

<table id="table_wdd_2rs_ks"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the push application.

</td></tr><tr><td>

Name

</td><td>

Database name of the push application. Enter a name that doesn't include spaces.

</td></tr><tr><td>

Push

</td><td>

Type of push service to enable for the application. Because you're setting up a custom push app, select **Direct**.

</td></tr><tr><td>

Feedback

</td><td>

Type of push feedback to use for the application. Because custom push apps don't receive push feedback, select **None**.

</td></tr><tr><td class="sub-head" colspan="2">

Apple

</td></tr><tr><td>

Certificate

</td><td>

The X.509 certificate that you created on the Apple notifications portal. The certificate enables a device to talk to the APNs.

</td></tr><tr><td>

Sandbox Certificate

</td><td>

Sandbox certificate that you created on the Apple notifications portal. The certificate enable a device to talk to the APNs.

</td></tr><tr><td>

APNS Bundle Id

</td><td>

Bundle ID included in the certificate that you created on the Apple notifications portal. The system populates this field automatically after you specify a certificate.

</td></tr><tr><td class="sub-head" colspan="2">

Google

</td></tr><tr><td>

API key

</td><td>

FCM API key you obtained from Google for the Android push notification.

</td></tr></tbody>
</table>3.  Click **Submit**.


## What to do next

[Create push message content](t_CreateAMobileMessageLayout.md) that contains the JSON content in the push notification payload.

In the Push Default Registrations related list, you can select the notifications that you want automatically subscribed to users who use this application. Users are subscribed to only active notifications.

