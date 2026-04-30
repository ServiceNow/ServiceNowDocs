---
title: Configure email and comment notifications
description: Add a script to the email reply or case comment template to include all activities \(emails and comments\) on a case record in email replies and in email notifications.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Email to case, Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Configure email and comment notifications

Add a script to the email reply or case comment template to include all activities \(emails and comments\) on a case record in email replies and in email notifications.

## Before you begin

Role required: admin

## Procedure

1.  Update comment notifications.

    1.  Navigate to **All** &gt; **System Notifications** &gt; **Notifications**.

    2.  In the **Email template** column, enter `case.commented.for.customer`.

    3.  In the **case.commented.for.customer** system property, add the following script to the **Message HTML** field: `${mail_script:get_emails_comments_activity_history}`.

    4.  Save the field.

2.  Update email notifications.

    1.  Navigate to **All** &gt; **Email client templates** &gt; **Reply**.

    2.  In the **reply-recieved** system property, add the following script to the **Body HTML** field: `${mail_script:get_emails_comments_activity_history}`.

    3.  Save the field.


## Result

All emails and comments are now included in the email replies and notifications.

