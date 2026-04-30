---
title: Hide email watermarks globally
description: Rather than omitting watermarks, it is possible to hide watermarks for global application using HTML markup.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Watermarks on notification emails, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Hide email watermarks globally

Rather than omitting watermarks, it is possible to hide watermarks for global application using HTML markup.

## Before you begin

Role required: admin

## About this task

Watermarks can only be hidden in the HTML message for the global application. The text version of the message, because it does not have markup allowing show/hide semantics, will always have the watermark.

## Procedure

1.  In the **Filter Navigator**, enter `sys_properties.list`.

2.  Select **New** to create a new property.

3.  In the **Name** field, enter `glide.email.watermark.visible`.

4.  From the **Type** drop-down list, select **true \| false**.

5.  In the **Value** field, enter false.

6.  Select **Submit**.

    This ensures that all watermarks are hidden on all email messages. This cannot be done on a per-email basis.


**Parent Topic:**[Watermarks on notification emails](../concept/c_WorkingWithWatermarks.md)

