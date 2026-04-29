---
title: Reprocess received emails
description: When a email has been processed incorrectly, fix the underlying problem, then reprocess the email. You can reprocess emails individually or in a batch.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Reprocess received emails

When a email has been processed incorrectly, fix the underlying problem, then reprocess the email. You can reprocess emails individually or in a batch.

## Before you begin

Role required: admin

## About this task

Various scenarios can result in improperly processed emails. After taking corrective action, reprocess the emails to get correct email records. Two of the most common scenarios are:

-   The inbound action failed to trigger correctly. After you update or fix the inbound action, reprocess the affected emails to create the correct records.
-   Emails have accidentally ended up on a development instance, usually due to the username or password of a production or test instance being reused on the development instance. In this case, you first export the emails from the development instance as XML and import them to the correct instance. On the correct instance, reprocess the imported emails to obtain correct email records.

You can reprocess emails with the types `received` or `received-ignored`. Such emails are processed to the system mailboxes **Received** and **Junk**, respectively.

Take the following steps only after fixing the underlying problem. This procedure only reprocesses the emails.

## Procedure

1.  Navigate to the relevant **System Mailbox** or navigate to **All** &gt; **System Logs** &gt; **Email**.

2.  Decide whether to reprocess emails individually or in a batch.

    -   To reprocess an individual email, open that email and click **Reprocess email**.
    -   To reprocess several emails at once, select them from the mailbox or the email log and apply the **Reprocess received emails** action.
    Remember that you can reprocess only `received` or `received-ignored` emails.


**Parent Topic:**[Use Inbound email actions](../concept/use-inbound-email-action.md)

