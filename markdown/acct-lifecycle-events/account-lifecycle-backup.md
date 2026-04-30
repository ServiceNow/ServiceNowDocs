---
title: Run scheduled job to back up staging table
description: You can take a backup of the data on the staging table at periodic intervals.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring account onboarding, Account onboarding, Account Lifecycle Events]
---

# Run scheduled job to back up staging table

You can take a backup of the data on the staging table at periodic intervals.

## Before you begin

Role required: admin

## About this task

Data present in the staging table backed up if:

-   Import tasks are in an **Active** state.
-   Data creation date is earlier than the current date.

**Note:** Import tasks that are in a **Canceled** or **Closed** state aren’t backed up.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Find the **Scheduled Staging Data Backup Job** scheduled job.

    **Note:** The job is inactive by default. Select the **Active** check box to run the scheduled job at the scheduled time.

3.  Select **Execute Now**.

    To configure the backup period, specify a number in the Value field for the `sn_accct_lc.BackupDays` system property. For example, if the Value field is set to 2, data that is more than two days old is included in the backup.


## Result

A CSV file is created and attached to the import task. The file name includes the name of the staging file and the creation date in the format `stagingTable-dateCreated.csv`.

