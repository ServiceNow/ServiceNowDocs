---
title: Archive email manually
description: You can archive email messages manually on demand instead of waiting for the instance to archive them based on a scheduled job.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Email retention, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Archive email manually

You can archive email messages manually on demand instead of waiting for the instance to archive them based on a scheduled job.

## Before you begin

Role required: admin

## About this task

Email Retention provides this email archive rule:

You can manually archive email messages that meet these archive rules or any additional archive rules that you create.

**Note:** An archive record must be active for the instance to be able to process records with it.

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  Open the email archiving rule that you want to modify.

3.  Select **Recalculate Archive Estimate** to see how many records in the Email \[sys\_email\] table are going to be archived.

    **Note:** The estimate appears in the **Record estimate** field.

4.  Select **Run Archive Now**.

    **Note:** You can also [Create an archive rule](../../database-rotation/task/t_CreateAnArchiveRule.md#).


**Parent Topic:**[Email retention](../concept/email-retention.md)

