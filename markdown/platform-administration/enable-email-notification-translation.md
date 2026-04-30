---
title: Enable dynamic translation
description: Enable dynamic translation of notifications for the instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dynamic translation, Multilingual email notifications, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Enable dynamic translation

Enable dynamic translation of notifications for the instance.

## Before you begin

Role required: admin

You must activate the Glide Notification Translation \(com.glide.notification.translation\) plugin.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the system property, which should be `glide.notifications.translation.dynamic`.|
    |Application|Application for the system property. **Global** applies the system property to all applications when the system property is set to **true**.|
    |Description|Description displayed in the System Properties list.|
    |Choices|Description displayed in the System Properties list.|
    |Type|Type of system property, which should be **true \| false**.|
    |Value|Value for the **Type** selected, which should be. `true`.|
    |Ignore cache|Option to ignore the cache.|
    |Private|Option to keep the system property private.|
    |Read roles|Roles that can read the system property.|
    |Write roles|Roles that can write the system property.|

4.  Select **Submit**.


**Parent Topic:**[Dynamic translation](../concept/dynamic-translation.md)

**Related topics**  


[Configure the note banner for translated emails](config-email-notification-banner.md)

[Enable dynamic translation for email notifications](enable-dynamic-translation.md)

