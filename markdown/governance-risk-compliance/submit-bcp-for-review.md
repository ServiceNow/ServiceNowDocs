---
title: Submit the BCP for approval
description: Submit the business continuity plan \(BCP\) for an approval. You can then view the details in BCM UIB Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Submit the BCP for approval

Submit the business continuity plan \(BCP\) for an approval. You can then view the details in BCM UIB Workspace.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Planning** and select the link to the plan record in the **Name** column.

3.  Select **Submit for review**.

    The business continuity plan is in the **Review** state.

4.  Select **Submit for approval**.

    The business continuity plan is updated to the **Pending approval** state. The business continuity plan is submitted for a review to the business continuity plan owner.

5.  Select **Approve**.

    **Note:** If an approval record is created for the BCP, the **Approve** or **Reject** actions are not displayed on the BCP form. For a user to view the **Approve** or **Reject** actions, these conditions must be fulfilled:

    -   The user should have the sn\_bcp.plan\_manager role.
    -   The BCP should be in the **Pending approval** state.
    -   The BCP should not have any approval records created.
    If you have the BCM lead or BCM program manager role, you can approve the plan. The information is displayed on the **Approval levels** and **Approvals** tabs as shown in the example.

    ![Approvals tab.](../image/approval-levels-approvals.png)

    To configure multiple approval levels for the plan, see [Set up approval levels](setup-bcm-approval-levels.md).

    The example shows the Approvals tabs and the Approve and Reject buttons are not displayed.

    ![Approve and Reject not displayed.](../image/approve-reject-not-displayed.png)

    When you approve the business continuity plan, its state is updated to **Approved**.


**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

