---
title: View scheduled jobs
description: You can view scheduled jobs for the process that you configured password expiration for. When you configure password expiration for a process, two scheduled jobs are created automatically.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure password expiration reminder, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View scheduled jobs

You can view scheduled jobs for the process that you configured password expiration for. When you configure password expiration for a process, two scheduled jobs are created automatically.

## Before you begin

Role required: admin

## About this task

One scheduled job creates a record in the password expiration table, which has the prefix as **Sync password expiration records for pwd\_process\_** followed by a sys\_id.

**Note:** This job runs only once. This scheduled job only creates a record in the password expiration table. It doesn’t fetch information about each user’s password expiration by calling the external credential store. For example, the values for the **Last Password Reset Date** or **Password Expiration Date** field remain empty. The expiration reminder scheduled job retrieves the dates for all the expiration records with empty dates before sending the expiration notifications.

The second scheduled job runs periodically based on configuration. The scheduled job that has a prefix as **pwd\_expiration\_reminder\_** followed by a sys\_id does the following two actions:

-   Fetches the latest information about the user’s password expiration.
-   Sends a notification when the user’s password is going to expire.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    The Scheduled Jobs page shows the scheduled jobs, which are created after you configure the password expiration.

2.  Select any of the scheduled jobs with the following prefixes:

    -   **Sync password expiration records for pwd\_process\_**
    -   **pwd\_expiration\_reminder\_**
    These prefixes are followed by the sys\_id of the password reset process.


**Parent Topic:**[Configure password expiration reminder](password-reset-expiration-setup.md)

