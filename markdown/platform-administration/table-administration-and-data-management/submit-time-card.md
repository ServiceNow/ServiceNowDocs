---
title: Submit a time card
description: As a time card user, once a time card for the week is updated with the time worked, you can submit the time card individually.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Time cards, Time Card management, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Submit a time card

As a time card user, once a time card for the week is updated with the time worked, you can submit the time card individually.

## Before you begin

-   A time card in the Pending or Rejected state can be submitted.
-   Role required: timecard\_user

## About this task

When a user submits a time card, the [time sheet policy](../concept/time-sheet-policies.md) assigned to the user is used for validation. If there’s no time sheet policy assigned to the user, the default time sheet policy is used. Business rules help prevent a user from submitting a time card in case any violation is found.

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **My Time Sheets** &gt; **All**.

2.  Select the time sheet that you want to submit the time card for.

3.  In the Time Card related list, open the time card to submit.

4.  Select **Submit Time Card**.

    **Note:** Submit multiple time cards by selecting **Submit Time Card** from the actions on selected rows menu.


## Result

-   The time card moves to the Submitted state.
-   The time card is submitted to an approver based on the **Project time approver** and **Non-project time approver** field values in the assigned time sheet policy.

    **Note:** If the project or user manager is changed after submitting the time card, the time card is automatically redirected to the new project or user manager for approval.


**Parent Topic:**[Time cards](../concept/c_TimeCards.md)

