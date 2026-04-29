---
title: Request a translation for an email notification, template or layout
description: Request a translation to send an email in the recipient’s preferred language.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Static translation, Multilingual email notifications, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Request a translation for an email notification, template or layout

Request a translation to send an email in the recipient’s preferred language.

## Before you begin

An email notification must exist. For more information, see [Create an email notification](t_CreateANotification.md).

You must activate the Glide Notification Translation \(com.glide.notification.translation\) plugin.

The [Localization Framework settings](../../localization-framework/concept/localization-settings.md) should be configured to request the translation for the artifact configurations and add languages.

Role required: admin

## About this task

Notification recipients must be defined as active users in the User \[sys\_user\] table and have a valid email address defined for their primary channel \(device\) in the Notification Device \[cmn\_notif\_device\] table.

## Procedure

1.  Navigate to the email item for which you want to request a translation.

    -   For notifications, navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**
    -   For templates, navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Templates**.
    -   For layouts, navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Layouts**.
    **Note:** Static translation is not supported for email notifications of type **Meeting Invitation**.

2.  Select the item you want to translate from the list.

3.  Select **Request Translation** and select the languages to translate into.

4.  Select **Submit**.


**Parent Topic:**[Static translation](../concept/static-translation.md)

**Related topics**  


[Enable static translation](enable-static-translation.md)

