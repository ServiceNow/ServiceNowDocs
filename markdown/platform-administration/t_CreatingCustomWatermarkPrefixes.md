---
title: Create a custom watermark prefix for email notifications
description: By default, email notifications use the watermark prefix MSG, but you can create a custom watermark prefix.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Watermarks on notification emails, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Create a custom watermark prefix for email notifications

By default, email notifications use the watermark prefix **MSG**, but you can create a custom watermark prefix.

## Before you begin

Role required: admin

## About this task

Any email notifications that are forwarded from one instance to another might be more easily distinguished with different prefixes for each instance. To avoid unintentionally triggering events in the wrong instance, create a unique watermark prefix for each instance.

**Note:** Do not use colons \(:\) in custom watermark prefixes. Colons are a reserved character and may cause the watermark to be ignored.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Number Maintenance**.

2.  Open the **MSG** record in the Email Watermark \[sys\_watermark\] table.

3.  Enter the unique **Prefix** for this instance.

4.  Click **Update**.


## Result

Your custom watermark applies to all new email notifications. Email notifications that existed before you created a custom watermark keep the same watermarks as before.

**Parent Topic:**[Watermarks on notification emails](../concept/c_WorkingWithWatermarks.md)

