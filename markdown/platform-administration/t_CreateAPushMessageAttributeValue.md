---
title: Create an attribute value or action for a push message
description: Attribute values are associated with push messages to provide a way for the message to include certain types of information in the push notification.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Push notification setup with a custom push application for ServiceNow mobile apps, Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an attribute value or action for a push message

Attribute values are associated with push messages to provide a way for the message to include certain types of information in the push notification.

## Before you begin

Complete the following:

1.  [Activate push notifications](t_ActivatePushNotifications.md)
2.  \( iOS only\) [Upload a push certificate to your instance](upload-push-cert.md)
3.  [Create a push application record for your custom app](t_CreateAMobileApplication.md)
4.  [Create push message content](t_CreateAMobileMessageLayout.md)
5.  [Create a push message attribute definition](t_CreateAPushMessageAttribute.md)

Role required: admin or push\_admin

**Note:** This process describes configuration used in the ServiceNow mobile app. Push Notification configuration for the current ServiceNow mobile UI can be found at Mobile push notifications

## About this task

These push message attribute values override values that you set in an [attribute definition](t_CreateAPushMessageAttribute.md) on the Push Content form.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Push** &gt; **Push Messages**.

2.  Select a message.

3.  In the Push Message Attribute Values related list, click **New**.

4.  Fill out the fields on the form \(see table\).

5.  Click **Submit**.

    |Field|Description|
    |-----|-----------|
    |Attribute|Select a [push message attribute definition](t_CreateAPushMessageAttribute.md).|
    |Value/Action|Enter the value for the attribute or select the push action. This field changes to Value or Action depending on the type of attribute you select in the Attribute field.|


## What to do next

\(Optional\) [Create a push action](t_CreateAMobileActionScript.md) to perform an action on the instance.

