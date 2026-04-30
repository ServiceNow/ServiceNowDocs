---
title: Notification example: notify task assignees
description: Notify users who are assigned a Task \[task\] record.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Notification example: notify task assignees

Notify users who are assigned a Task \[task\] record.

## Before you begin

Role required: admin

Set up your email as a test email address. Navigate to **System Properties** &gt; **Email Properties**, and then enter your email address under **Send all email to this test email address**.

## Procedure

1.  Navigate to **System Notification** &gt; **Email** &gt; **Notifications**, and then click **New**.

2.  On the form, enter the following values:

    |Field|Value|
    |-----|-----|
    |Name|Task Assigned|
    |Table|Task \[task\]|
    |Active|Selected|
    |Category|Uncategorized|
    |Send when|Record inserted or updated|
    |Inserted|Selected|
    |Updated|Selected|
    |Conditions|\[Assigned to\]\[changes\]|
    |Users/Groups in fields|Assigned to|
    |Subject|Task Assigned|

3.  In the **Message HTML** field, add a message to send to whomever the task is assigned to.

4.  From the form context menu, click **Save**.

5.  To see a mock version of the system email that you created, click **Preview Notification** on the notification form.

6.  Test the notification sends to a task assignee.

    1.  Assign some task records.

    2.  Check your email for assignment notifications.


**Parent Topic:**[Create an email notification](t_CreateANotification.md)

