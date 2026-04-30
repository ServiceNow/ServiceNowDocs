---
title: Submit a time sheet
description: Once the time sheet is updated with time worked, you can submit the time sheet for the week to submit all the time cards for the week together.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Time Sheets, Time Card management, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Submit a time sheet

Once the time sheet is updated with time worked, you can submit the time sheet for the week to submit all the time cards for the week together.

## Before you begin

Role required: timecard\_user

## About this task

When a user submits a time sheet, the [time sheet policy](../concept/time-sheet-policies.md) assigned to the user is used for validation. If there is no time sheet policy assigned to the user, the default time sheet policy is used. Business rules prevent a user from submitting a time sheet in case any violation is found.

**Note:** You can also perform this task from the [Time Sheet Portal](submit-timesheet-workerportal.md).

## Procedure

1.  Navigate to the time sheet using one of the following options:

    -   To submit a time sheet in the Pending state, navigate to**Time Sheets** &gt; **My Time Sheets** &gt; **Pending**.
    -   To submit the time sheet for the current week, navigate to **Time Sheets** &gt; **My Time Sheets** &gt; **Current Time Sheet**.
    -   To submit a time sheet in the Rejected state, **Time Sheets** &gt; **My Time Sheets** &gt; **Rejected**. You can make required changes as suggested in the rejection comments to resubmit a rejected time sheet.
2.  To submit in the Time Sheets list, open the time sheet.

3.  Add comments, if required.

4.  Click **Submit Time Sheet**.


## Result

-   The time sheet moves to the Submitted state.
-   All the time cards associated with the time sheet are also submitted automatically and move to the Submitted state.

**Parent Topic:**[Time Sheets](../concept/time-sheets.md)

