---
title: Enable static translation
description: Enable static translation of notifications for the global application.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Static translation, Multilingual email notifications, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable static translation

Enable static translation of notifications for the global application.

## Before you begin

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the system property, which is `glide.email.outbound.static_translation.enabled`.|
    |Application|Application for the system property. **Global** applies the system property to all applications when the system property is set to true.|
    |Description|Description displayed in the System Properties list.|
    |Choices|Description displayed in the System Properties list.|
    |Type|Type of system property, either true or false.|
    |Value|Value for the **Type** selected, which should be set to true.|
    |Ignore cache|Option to ignore the cache.|
    |Private|Option to keep the system property private.|
    |Read roles|Roles that can read the system property.|
    |Write roles|Roles that can modify the system property.|

4.  Select **Submit**.


**Parent Topic:**[Static translation](../concept/static-translation.md)

**Related topics**  


[Request a translation for an email notification, template or layout](request-translation-and-send-email-notification.md)

