---
title: Configure the note banner for translated emails
description: Configure the content for a translated email note banner displayed at the top of the page to display a customized message to the recipient.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dynamic translation, Multilingual email notifications, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the note banner for translated emails

Configure the content for a translated email note banner displayed at the top of the page to display a customized message to the recipient.

## Before you begin

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Search for and select the properties to configure and customize the note banner.

    |System property|Description|
    |---------------|-----------|
    |**glide.email.translation.dynamic.note.html\_body**|Displays the message as a header for the translated email html body.|
    |**glide.email.translation.dynamic.note.text\_body**|Adds the message to the text body of the translated email body text.|
    |**glide.email.translation.dynamic.note.html\_body.styles**|Applies CSS styles to the note.|

    **Note:** If you want to disable the note banner, set the **glide.email.translation.dynamic.note.enabled** system property to false.


**Parent Topic:**[Dynamic translation](../concept/dynamic-translation.md)

**Related topics**  


[Enable dynamic translation](enable-email-notification-translation.md)

[Enable dynamic translation for email notifications](enable-dynamic-translation.md)

