---
title: Recall a processed time sheet
description: You can recall an incorrect time sheet in the Approved or Processed state to return it to the submitter. The submitter can then make the necessary changes and resubmit the time sheet.
locale: en-US
release: australia
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Time Sheets, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Recall a processed time sheet

You can recall an incorrect time sheet in the Approved or Processed state to return it to the submitter. The submitter can then make the necessary changes and resubmit the time sheet.

## Before you begin

Role required: timecard\_approver or timecard\_admin

## About this task

The recall option is available only if the **Allow recall** option is selected on the associated [time sheet policy](create-time-sheet-policy.md).

## Procedure

1.  Navigate to the approved or processed time sheet you want to recall using one of the following options.

<table id="choicetable_s4y_wb4_xgb"><thead><tr><th align="left" id="d247666e78">

Option

</th><th align="left" id="d247666e81">

Description

</th></tr></thead><tbody><tr><td id="d247666e87">

**From the Time Sheet Portal**

</td><td>

1.  Navigate to **Time Sheets** &gt; **Time Sheet Portal**.

2.  Click the **My Time Sheet** list and select a user under **My Resources**.

3.  Navigate through the **Calendar** widget to select the time sheet.

The time sheet must be within the recall period specified in the time sheet policy.

</td></tr><tr><td id="d247666e132">

**From the Time Sheet form**

</td><td>

1.  Navigate to **Time Sheets** &gt; **Time Sheets** &gt; **All**.

2.  Open the time sheet.

The time sheet must be within the recall period.

</td></tr></tbody>
</table>2.  Click **Recall**.


## Result

-   Changes the state of the time sheet and associated time cards to **Recalled**.
-   Reverts the actual effort and resource hours in a project or demand created when time cards that have task types were approved.
-   Creates negative expense lines to zero out the corresponding expense lines created when the time sheet was approved.
-   Returns the time sheet to its submitter for modifications.

**Parent Topic:**[Time Sheets](../concept/time-sheets.md)

