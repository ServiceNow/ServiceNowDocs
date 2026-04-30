---
title: Approve or reject a time card
description: As a time card approver, you can view and approve or reject a submitted time card.
locale: en-US
release: zurich
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Time cards, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Approve or reject a time card

As a time card approver, you can view and approve or reject a submitted time card.

## Before you begin

Role required: timecard\_approver or timecard\_admin

## About this task

You can view only those time cards that are submitted to you for approval or you have been delegated as the time card approver by one of the other user managers. The [time sheet policy](create-time-sheet-policy.md#time_sheet_policy_form) assigned to the user governs the approval process.

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Time Cards** &gt; **Pending Approval**.

2.  Select the time card to approve or reject.

3.  Click **Approve** or **Reject**.


## Result

-   The time card moves to the Approved or Rejected state.
-   Expense line is created for an approved time card.
-   For an approved time card, a Time Card Daily record is created.

**Note:**

-   A user manager can also approve the time cards within a time sheet by selecting one or more time cards and approving them. When all the time cards in a time sheet are approved, the time sheet automatically moves to the Approved state.

    A user manager is one who is selected in the **Manager** field on User form of the time card user.

-   If a time card is in the Rejected state, the associated time sheet also moves to the Rejected state irrespective of the state of other time cards in the time sheet.

    **Note:** If a time sheet is rejected, it gets listed in the notifications for the rejected time sheets under notifications icon ![screenshot for notification icon](../../../product/project-management/image/NotificationIcon.png) on [Time Sheet Portal](../concept/worker-portal.md#section_sth_2wd_vz).

-   If **Project time approver** is set to **Both** in the assigned time sheet policy, the time card is in the Submitted state only if both approvers approve it. If one of the approver rejects, the time card state is set to Rejected and the **Approved by** field is cleared, requiring approval of both approvers on resubmission.

**Parent Topic:**[Time cards](../concept/c_TimeCards.md)

