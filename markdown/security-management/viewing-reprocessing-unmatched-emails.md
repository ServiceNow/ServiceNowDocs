---
title: View and reprocess unmatched Security Operations emails
description: You can review Unmatched Emails for discontinued filters or as candidates for a new filter to maintain or improve the rate at which you catch email threats.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Unmatched Security Operations email events, Security Operations email processing, Security Operations common functionality, Security Operations]
---

# View and reprocess unmatched Security Operations emails

You can review Unmatched Emails for discontinued filters or as candidates for a new filter to maintain or improve the rate at which you catch email threats.

## Before you begin

Role required: sn\_sec\_cmn.read

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Unmatched Emails**.

    If any unmatched emails have been found, they are listed.

2.  The fields on the form are as follows:

    |Field|Description|
    |-----|-----------|
    |From|Email address of the sender.|
    |To|Email address of the recipients.|
    |Subject|Subject line in the email.|
    |Body|Contents of the body of the email.|
    |Matched|Indicates if this email event was matched.|

3.  To reprocess this email, create an email record or edit an existing email record to match the information in this email.

    See [Create email parsers in Security Operations](parsing-emails.md).

4.  Navigate back to **Security Operations** &gt; **Unmatched Emails**.

5.  Click **Reprocess Email Event** to attempt to process this email.

    It returns you to the Unmatched Emails main list. If the new email record matches, the email event is no longer in the list. A message indicates if it was matched or not.


**Parent Topic:**[Unmatched Security Operations email events](../concept/umatched-emails.md)

