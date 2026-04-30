---
title: Create an email reader job
description: If you created email account groups to fine-tune inbound email account processing, you can create an email reader job to process those account groups concurrently, in addition to the default email reader job.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Multiple email readers, Email accounts, Create, Email Administration, Notifications, Configure core features, Administer]
---

# Create an email reader job

If you created email account groups to fine-tune inbound email account processing, you can create an email reader job to process those account groups concurrently, in addition to the default email reader job.

## Before you begin

1.  [Create email account groups](create-email-account-group.md).
2.  [Enable email account group processing](enable-group-processing.md)

Role required: email\_account\_admin or admin

## Procedure

1.  In the Navigation filter, type `sys_trigger.list`.

2.  In the sys\_trigger table, select the Email Reader job record.

3.  In the Email Reader job form:

    1.  Enter a unique name for the email reader job to be added so that you can differentiate it from the default email reader job.
    2.  If needed, change the time interval for this email reader job.
4.  From the form context menu, click **Insert**.

    Another email reader job is created. This job runs concurrently with the default email reader job to process email account groups.


## What to do next

[Monitor email account group processing](monitor-email-account-groups.md) and determine if the additional reader job reduces processing time. If needed, you can continue fine-tuning email account processing. For example, you might consider adding another email account group.

