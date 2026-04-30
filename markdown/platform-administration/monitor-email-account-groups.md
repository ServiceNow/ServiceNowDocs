---
title: Monitor email account groups
description: Use the Email Account Groups \[sys\_email\_account\] table to check the status of email account groups processed by email reader jobs.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multiple email readers, Email accounts, Creating an email account, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Monitor email account groups

Use the Email Account Groups \[sys\_email\_account\] table to check the status of email account groups processed by email reader jobs.

## Before you begin

1.  [Create email account groups](create-email-account-group.md).
2.  [Enable email account group processing](enable-group-processing.md).

Role required: email\_account\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Email Account Groups**.

2.  Review the processing details for each account group:

<table id="table_rcw_zgq_nfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the email account group.

</td></tr><tr><td>

Active

</td><td>

The operational state of the email account group. The value true indicates that the account is enabled for email account processing.

</td></tr><tr><td>

Claimed by

</td><td>

The ID of the email reader job if the job is running on the account group.

</td></tr><tr><td>

Default

</td><td>

The default indicator. The value true indicates that the email account group is the default.

</td></tr><tr><td>

Email Accounts

</td><td>

The names of the email accounts contained in the email account group.

</td></tr><tr><td>

Last Processed

</td><td>

The day and time that the email reader job last processed this account group.

</td></tr><tr><td>

Processing Duration

</td><td>

The length of time \(in hours, minutes, seconds\) to process the account group.

</td></tr><tr><td>

Status

</td><td>

Processing state of the email account group: -   Unclaimed: The account group is available for processing by the next email reader job.
-   Claimed: An email reader job is processing the current account group.


</td></tr></tbody>
</table>
## Example

![An email account group not yet processed by the email reader job](../image/email-acct-group-unclaimed.png "Email account group — unclaimed processing state")

![An email account group that was recently processed by the email reader job](../image/email-acct-group-claimed.png "Email account group — claimed processing state")

## What to do next

If fine-tuning email accounts, consider doing one of the following:

-   Create another [email account group](create-email-account-group.md).
-   Create another [email reader job](create-email-reader-job.md) to process email account groups concurrently.

