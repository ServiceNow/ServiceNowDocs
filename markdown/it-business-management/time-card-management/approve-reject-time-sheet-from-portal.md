---
title: Approve or reject a time sheet through Time Sheet Portal
description: Review, approve, or reject a time sheet submitted by a time card user that you manage.
locale: en-US
release: australia
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Time Sheet Portal, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Approve or reject a time sheet through Time Sheet Portal

Review, approve, or reject a time sheet submitted by a time card user that you manage.

## Before you begin

Role required: timecard\_approver or timecard\_admin

## About this task

A user manager can review, approve, or reject the time sheets or time cards submitted by the time card users. The user manager has either of the required roles and is the one listed as the manager of the time card users.

During out-of-office time, the user manager can [delegate another user](delegate-time-sheet-approvals.md) with the required roles as the time sheet approver. For the specified time period, the delegated user also receives all the time sheets submitted by the time card users to process.

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Time Sheet Portal**.

2.  Click the **My Time Sheet** list and select a time card user under **My Resources**.

    The **My Time Sheet** list is available only for a user manager.

3.  Select the appropriate time sheet period by navigating through the calendar.

4.  Click **Approve** or **Reject**.

<table id="choicetable_z2p_nk2_zfb"><thead><tr><th align="left" id="d304631e116">

Action

</th><th align="left" id="d304631e119">

Result

</th></tr></thead><tbody><tr><td id="d304631e125">

**Approve**

</td><td>

-   Time sheets that have time cards with multiple approvers as defined by the [time sheet policy](create-time-sheet-policy.md#time_sheet_policy_form), remain in the **Submitted** state. When all the approvers approve the respective time cards, then the time sheet moves to the **Approved** state.
-   Time sheets that have time cards with a single approver move from the **Submitted** to the **Approved** state.
-   A Time Card Daily record is created for each time card to record the time logged.


</td></tr><tr><td id="d304631e162">

**Reject**

</td><td>

-   Time cards in the **Submitted** state are rejected automatically. Time cards in the **Approved** and **Processed** state remain unaffected.
-   A notification about the rejected time sheet is sent to the associated time card user. The user can view the notification from the show notifications icon \(![Show notifications icon](../../../product/project-management/image/NotificationIcon.png)\).

The user can then modify the rejected time sheet and submit it again for approval.

</td></tr></tbody>
</table>
**Parent Topic:**[Time Sheet Portal](../concept/worker-portal.md)

