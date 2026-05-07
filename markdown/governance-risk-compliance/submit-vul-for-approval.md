---
title: Request an approval
description: Request an approval for the Operational vulnerability record. When you request an approval, the state of the vulnerability is updated to the Pending approval state and then to the Requested state respectively.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Request an approval

Request an approval for the Operational vulnerability record. When you request an approval, the state of the vulnerability is updated to the **Pending approval** state and then to the **Requested** state respectively.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All Operational Vulnerabilities**.

2.  Open the vulnerability that you want to submit for an approval.

    **Note:** All action tasks must be closed before an analyst or assignment group member can update the vulnerability state.

3.  In the vulnerability record, select **Update state**.

    If any of the action tasks for the vulnerability are not closed yet, a message is displayed that All action tasks must be closed before an analyst or assignment group member can update the vulnerability state.

    The following example shows that the action task for the vulnerability is in the **Review** state.

    ![Action task for the vulnerability.](../image/review-state-action-task.png)

4.  Select the open action task, review its details, and select the **Update state** UI action.

5.  To close the open action task, update its state to **Closed complete** in the Update state window, and select **Submit**.

    The state of the action task is now updated to **Closed complete**.

6.  In the vulnerability record, select **Update state** UI action, update the state to **Pending approval** in the Update state window, and select **Submit**.

    The state of the vulnerability record is updated to **Pending approval**.

    ![Pending approval.](../image/vul-pending-approval-state.png)

    The list of the approvers is displayed in the Approvers related list. The Operational vulnerability record owner requests an approval by updating the state to **Requested** as shown in the example.

    ![Approvers.](../image/vul-approvers.png)

    An email notification is sent to one or more reviewers with the Operational vulnerability details and a link to approve the Operational vulnerability. A sample email notification is shown in the example.

    ![Email to approve the vulnerability.](../image/vul-email-approval-request.png)

    The Operational vulnerability record is now in the **Pending approval** state.


## What to do next

The subsequent step requires the approver to review the email notification, select the approval link from the email, and approve the Operational vulnerability. For more information, see [Approve the operational vulnerability](approve-vul.md).

