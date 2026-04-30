---
title: Configure email and comment notifications
description: As an admin, you can add a script to notification and reply templates so that the activity shown in the thread matches the value set in \[number\_of\_activities\_in\_notification\].
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-08"
reading_time_minutes: 1
breadcrumb: [Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Configure email and comment notifications

As an admin, you can add a script to notification and reply templates so that the activity shown in the thread matches the value set in \[number\_of\_activities\_in\_notification\].

## Before you begin

Role required: admin

## About this task

You can use the script to update the number of activities shown in any notification and reply template. The `case.commented.for.customer` and `reply-recieved` templates are only two examples.

## Procedure

1.  To update comment notifications, do the following:

    1.  Navigate to **All** &gt; **System Notifications** &gt; **Notifications**.

    2.  In the **Email template** column, enter `case.commented.for.customer`.

    3.  In the `case.commented.for.customer` template, add the following script to the **Message HTML** field: `${mail_script:get_emails_comments_activity_history}`, and save.

2.  To update email notifications, do the following:

    1.  Navigate to **All** &gt; **Email client templates** &gt; **Reply**.

    2.  In the `reply-recieved` template, add the following script to the **Body HTML** field: `${mail_script:get_emails_comments_activity_history}`, and save.


## Result

Emails and comments match the value set in \[number\_of\_activities\_in\_notification\].

