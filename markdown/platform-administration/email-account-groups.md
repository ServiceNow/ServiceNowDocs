---
title: Multiple email readers
description: Organize POP3/IMAP email accounts into email account groups \(subsets of email accounts\) that can be processed by multiple email reader jobs. To improve the performance of inbound email account processing, you can incrementally add email account groups and if needed, email reader jobs to process email account groups concurrently.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Email accounts, Create, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Multiple email readers

Organize POP3/IMAP email accounts into email account groups \(subsets of email accounts\) that can be processed by multiple email reader jobs. To improve the performance of inbound email account processing, you can incrementally add email account groups and if needed, email reader jobs to process email account groups concurrently.

## How email account group processing works

By default, the email reader job processes POP3/IMAP email accounts serially, which can result in longer processing times when you have many email accounts. It can also be difficult to identify any problematic email accounts that might contribute to slower processing times.

To reduce email account processing time, you can create one or more email account groups that contain subsets of your email accounts. Organizing your email accounts into groups enables the default email reader job to process each email account group separately. After creating one or more email account groups, you can then add another email reader job to process account groups concurrently.

Use the **glide.email.inbound.account\_group\_processing** system property to activate email account group processing.

During email account group processing:

-   The system stores the email accounts in the Email Account Groups \[sys\_email\_account\_group\] table.
-   The default email reader job runs every two minutes. The email reader chooses the account group to be processed based on the account group processing state and the date and time that the group was last processed.
    -   Claimed state: If an account group has a claimed state, the email reader is processing the account group. If you defined other email reader jobs, no other email reader job can claim the group for processing.
    -   Unclaimed state: If an account group is unclaimed, the account group is available for processing by the email reader.
-   The email reader job processes the email accounts contained in the selected account group.
-   The email reader job chooses the next available account group for processing and continues processing that account group.

You can monitor the processing of each email account group by using the Email Account Groups \[\[sys\_email\_account\_group\]\] table. Each account group record includes the processing duration \(how long it takes for the email reader to process all the accounts in the group\).

After you review the processing times for your email account groups, determine whether to make further adjustments in email account group processing. For example, you can create another email account group or create another email reader job to process your email account groups in parallel. You define additional email reader jobs using the Schedule \[sys\_trigger\] table.

## Set up email account group processing

To set up email account group processing, you must have the email\_account\_admin or admin role.

-   **1. [Create email account groups](../task/create-email-account-group.md).**

    Define one or more email account groups that contain a subset of your POP3/IMAP email accounts. Your base system includes a default email account group. Any POP3/IMAP accounts not contained in an email account group are processed as part of the default email account group.

-   **2. [Enable email account group processing](../task/enable-group-processing.md)**

    Navigate to sys\_properties.list and locate the **glide.email.inbound.account\_group\_processing** system property. Set the **Value** to **true**. The email reader job starts processing the email account groups that you created.

-   **3. [Monitor email account group processing.](../task/monitor-email-account-groups.md)**

    Check the status of your email account groups to see if processing time has been reduced. Determine whether the additional groups sufficiently reduce account processing time or consider adding another email reader job to further reduce processing time.

-   **4. [Create an email reader job](../task/create-email-reader-job.md).**

    As part of fine-tuning email account group processing, create an email reader job to process email account groups concurrently, in addition to the default email reader job.


