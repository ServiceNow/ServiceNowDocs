---
title: Delete import sets
description: Delete import sets to clean up your database on a scheduled basis, one time only, or on demand.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Delete import sets

Delete import sets to clean up your database on a scheduled basis, one time only, or on demand.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Import Set Tables** &gt; **Scheduled Cleanup**.

2.  Fill out the form.

    |Field|Description|
    |-----|-----------|
    |Name|Defaults to **Import Set Deleter**. You can change the name if desired.|
    |Active|Checked if the schedule is active. Unchecked if the schedule is not active.|
    |Application|Defaults to **Global** and can't be changed.|
    |Conditional|Checked if the Import Set Deleter must meet specified conditions. Unchecked if the Import Set Deleter doesn't have to meet any conditions.|
    |Run|Specifies the frequency of the Import Set Deleter: **Daily**, **Weekly**, **Monthly**, **Periodically**, **Once**, or **On Demand**.|
    |Time zone|For scheduled job types that require an entered time, you can enter an associated time zone. If no time zone is selected, the job runs at the specified time in the time zone of the user who entered the time. If **Use System Time Zone** is selected, the job runs at the specified time in the time zone of the instance running the job.|
    |Time|The time of day to run the Import Set Deleter.|
    |Run this script|The script that performs the deletion. Defaults to deleting import sets and their related import set rows that were created more than seven days ago.|
    |Day|The day of the week for weekly runs, or the day of the month for monthly runs.|
    |Repeat Interval|The number of days in the repeat interval and up to three times of day for the repeat interval.|
    |Starting|The starting date and time for the periodical run or the one-time run.|

3.  Click **Update** to update the schedule, or click **Execute Now** to run the Import Set Deleter immediately.


**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

