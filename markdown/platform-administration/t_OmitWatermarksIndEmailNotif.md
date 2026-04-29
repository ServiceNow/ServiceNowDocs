---
title: Omit an email notification watermark
description: You can omit watermarks on email notifications if you do not want the instance to match the notification to an existing record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Watermarks on notification emails, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Omit an email notification watermark

You can omit watermarks on email notifications if you do not want the instance to match the notification to an existing record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Select the email notification to update.

3.  Click the **Advanced View** related link.

4.  In the **What it will contain** section, select the **Omit watermark** check box.


## What to do next

When incoming email does not contain a watermark, the system searches the subject line and message body for a record number. The system attempts to match any record number that it finds to an existing record. If there is a matching record number, the system updates the record with the values in the incoming email. To ensure that response email messages don't update records, remove the record number variable `${number}` from the **Subject** and **Message HTML** fields.

**Parent Topic:**[Watermarks on notification emails](../concept/c_WorkingWithWatermarks.md)

