---
title: Log time and submit time sheets of your resources
description: As a user manager, you can log time and submit the time sheet of your resources.
locale: en-US
release: yokohama
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Time Sheet Portal, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Log time and submit time sheets of your resources

As a user manager, you can log time and submit the time sheet of your resources.

## Before you begin

A user manager must have time card approver role to create and edit time cards, and submit the time sheet of other time card users. The user manager has either of the required roles and is the one listed as the manager of the time card users.

Role required: timecard\_approver

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Time Sheet Portal**.

2.  Click **My Time Sheet** choice list and select the user for whom you want to approve or reject time sheet for under **My Resources**.

    The **My Resources** section lists the time card users reporting to you.

    **Note:** The choice list with **My Time Sheet** is available only for a user manager.

3.  [Create time cards and log time through Time Sheet Portal](create-timecards-through-worker-portal.md) as required.

4.  Click **Submit**.


## Result

-   The time sheet of the selected user moves to the Submitted state. The [time sheet policy](../concept/time-sheet-policies.md) assigned to the time card user is used for validation when you submit the time sheet.
-   All the time cards associated with the time sheet are also submitted automatically and move to the Submitted state.
-   The **Approve** and **Reject** buttons appear in the Time Sheet section. The two buttons appear only for a user manager.

## What to do next

Once you have submitted the time sheet for your resource, you can click **Approve** or **Reject** to approve or reject it. Only the time cards that are routed to the user manager, are approved or rejected. The routing for approval happens based on the **Non-project time approver** and **Project time approver** fields in the time sheet policy of the time card user.

**Parent Topic:**[Time Sheet Portal](../concept/worker-portal.md)

