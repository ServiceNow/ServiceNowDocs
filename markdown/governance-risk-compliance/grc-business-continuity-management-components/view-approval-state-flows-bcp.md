---
title: View approval state flows for a business plan
description: View the approval state transitions sent at each level of the approval process, and the details of the approvers as you direct the business plan through multiple levels of approvals.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# View approval state flows for a business plan

View the approval state transitions sent at each level of the approval process, and the details of the approvers as you direct the business plan through multiple levels of approvals.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager, sn\_bcm.viewer

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

    You can view approval records for a business plan that is any state except **Draft** and **In Review** states.

3.  Click the link to the business plan record in the **Name** column.

4.  To view the approval details of the plan, click the Approvals related list.

    If there are no approval records in requested state for the plan, then you can either **Reject** or **Approve** the plan.

5.  Click the link to the approval record in the **Name** column.

    You can view the name of the approval, approval level, its current state, and the details of approvers such as users and groups.

6.  To view the approval history of the plan, click the **Details** tab.

    1.  Click the Approval History related list.

        You can view the complete approval history with details of the approvers and the date and time of its creation.

    State transitions for multiple levels of plan approvals:

    -   **Not Yet Requested**

        State where an approval is not yet sent to the approvers at a respective level.

    -   **Requested**

        Approvals are sent to the approvers of that level. Correspondingly, the state of all successive levels of approvals turns to Not Yet Requested.

    -   **Approved**

        One or more approvers have approved the plan at the respective level. Correspondingly, the state of the succeeding level of approval moves to Requested.

    -   **Rejected**

        One or more approvers have rejected the plan at a particular level. Correspondingly, the state of all succeeding levels of approvals moves to No Longer Required.

    -   **No Longer Required**

        If the approvers at a level have rejected the plan, then the state moves to No Longer Required for all succeeding levels of approvals.


