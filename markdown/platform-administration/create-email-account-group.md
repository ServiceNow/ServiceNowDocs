---
title: Create email account groups
description: Define an email account group that contains a subset of your POP3/IMAP email accounts. The email reader job automatically processes each email account group as scheduled.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multiple email readers, Email accounts, Creating an email account, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create email account groups

Define an email account group that contains a subset of your POP3/IMAP email accounts. The email reader job automatically processes each email account group as scheduled.

## Before you begin

Role required: admin or email\_account\_admin

## Procedure

1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Email Account Groups** and click **New**.

2.  Fill in the form.

<table id="table_rcw_zgq_nfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the account group.

</td></tr><tr><td>

Email Accounts

</td><td>

A subset of POP3/IMAP email accounts. Select the email accounts that make up the group. **Note:** When you add an email account to a group, it cannot be reused in other account groups.

</td></tr><tr><td>

Active

</td><td>

Check box that enables the email account group for processing. New account groups are active by default.

</td></tr><tr><td>

Default

</td><td>

Read only. Check box that indicates the account is the default email account.

</td></tr><tr><td>

Status

</td><td>

Read only. Processing state of the email account group: Unclaimed or Claimed.

</td></tr><tr><td>

Claimed by

</td><td>

Read only. ID of the email reader job currently in progress.

</td></tr><tr><td>

Last Processed

</td><td>

Read only. The last time that the email reader job processed this group.

</td></tr><tr><td>

Processing Duration

</td><td>

Read only. The length of time taken by an email reader job to process the account group.

</td></tr></tbody>
</table>3.  Click **Create**.

    The system updates the Email Account Group \[sys\_email\_account\_group\] table with the new account group. Use the this table to monitor email account group processing.


## What to do next

-   Review [email account group processing](create-email-account-group.md).
-   Determine if you want to continue fine-tuning email account processing. You could add another email account group or another email reader job to process email account groups concurrently.

