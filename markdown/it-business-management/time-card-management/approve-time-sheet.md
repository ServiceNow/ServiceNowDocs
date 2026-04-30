---
title: Approve or reject a time sheet
description: View, approve, or reject time sheet or time cards for your user, for the given week, in a single step.
locale: en-US
release: zurich
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Time Sheets, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Approve or reject a time sheet

View, approve, or reject time sheet or time cards for your user, for the given week, in a single step.

## Before you begin

Role required: timecard\_approver or timecard\_admin

## About this task

A user manager is the one who has either of the required roles and is selected in the **Manager** field on User form of the time card user.

During out-of-office time, the user manager can [Delegate time sheet approvals to another user](delegate-time-sheet-approvals.md) with the required roles as the time sheet approver. For the specified time period, the delegated user also receives all the time sheets submitted by the time card users to process.

**Note:**

-   You can also approve or reject the time cards within a time sheet selectively by selecting one or more time cards and approving or rejecting them.
-   If a time sheet is rejected, all the associated time cards in the Submitted state are also rejected automatically. The time cards in the Approved and Processed state for the time sheet remain unaffected.
-   If all the time cards in a time sheet are approved, the time sheet automatically moves to the Approved state.
-   If a time card in a time sheet is in the Rejected state, then irrespective of the state of other time cards in the time sheet, the time sheet also moves to the Rejected state.

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Time Sheets** &gt; **Pending Approval**.

2.  In the Time Sheets list, open the time sheet to approve or reject.

3.  If required, add comments.

4.  Click **Approve** or **Reject**.


## Result

The time sheet moves to the Approved or Rejected state.

-   If a time sheet is rejected, it gets listed in the notifications for the rejected time sheets under the show notifications icon \(![Show notifications icon](../../../product/project-management/image/NotificationIcon.png)\) on [Time Sheet Portal](../concept/worker-portal.md#section_sth_2wd_vz) and is moved back to the submitter to adjust the corrections and resubmit it. For more information, see [Submit a time sheet](submit-time-sheet.md).
-   Once a time sheet is approved, all the time cards associated with the time sheet are also approved or rejected automatically.
-   If any time cards in the time sheet are pending approval by one of the approvers as defined by the [time sheet policy](create-time-sheet-policy.md#time_sheet_policy_form), the time sheet remains in the Submitted state.

**Parent Topic:**[Time Sheets](../concept/time-sheets.md)

