---
title: Customize behavior for sensitive data redaction
description: Customize sensitive data redaction behavior by creating system properties for flows that are triggered by inbound emails, sys\_email record, and inbound actions.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Sensitive data redaction, Use Inbound email actions, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Customize behavior for sensitive data redaction

Customize sensitive data redaction behavior by creating system properties for flows that are triggered by inbound emails, sys\_email record, and inbound actions.

## Before you begin

Role required: admin

## Procedure

1.  Create a system property to toggle redaction in flows.

    **Note:** When this property is enabled, then by default all inbound actions and sys\_email record are redacted irrespective of the below property values mentioned in Step 2 and Step 3.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Select **New** to create **glide.email.inbound.email\_redaction.trigger\_flow.enabled** property.

    3.  On the form, fill in the details.

        |Fields|Input|
        |------|-----|
        |Name|**glide.email.inbound.email\_redaction.trigger\_flow.enabled**|
        |Description|This is a global property to toggle redaction in Workflow Studio|
        |Type|true\|false|
        |Value|false|

    4.  Select **Submit**.

2.  Create a system property to toggle redaction in the sys\_email record.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Select **New** to create **glide.email.inbound.email\_redaction.sys\_email.enabled** property.

    3.  On the form, fill in the details.

        |Fields|Input|
        |------|-----|
        |Name|**glide.email.inbound.email\_redaction.sys\_email.enabled**|
        |Description|This property toggles redaction in sys\_email record|
        |Type|true\|false|
        |Value|true|

    4.  Select **Submit**.

3.  Create a system property to toggle redaction in all inbound actions.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Select **New** to create **glide.email.inbound.email\_redaction.email\_wrapper.enabled** property.

    3.  On the form, fill in the details.

        |Fields|Input|
        |------|-----|
        |Name|**glide.email.inbound.email\_redaction.email\_wrapper.enabled**|
        |Description|This property toggles redaction in all inbound emails|
        |Type|true\|false|
        |Value|false|

    4.  Select **Submit**.


**Parent Topic:**[Sensitive data redaction](../concept/sensitive-data-redaction.md)

