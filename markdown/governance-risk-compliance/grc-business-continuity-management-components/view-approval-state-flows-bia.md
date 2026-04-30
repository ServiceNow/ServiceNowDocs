---
title: View approval state flows for a business impact analysis
description: View the approval state transitions sent at each level of the approval process, and the details of the approvers as you direct the business impact analysis through multiple levels of approvals.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Assess impact categories and dependencies of process, Structured workflows for BIA, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# View approval state flows for a business impact analysis

View the approval state transitions sent at each level of the approval process, and the details of the approvers as you direct the business impact analysis through multiple levels of approvals.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager, sn\_bcm.viewer

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

    You can view approval records for a business impact analysis \(BIA\) that is any state except **Draft** and **In Review** states.

3.  Click the link to the business impact analysis record in the **Name** column.

4.  To view the approval details of the BIA, click the Approvals related list.

    If there are no approval records in the requested state for the BIA, then you can either **Reject** or **Approve** the BIA.

    **Note:** If you are a BCM Program Manager, then you can see the **Approve** and **Reject** buttons.

5.  Click the link to the approval record in the **Name** column.

    You can view the name of the approval, approval level, its current state, and the details of approvers such as users and groups.

6.  To view the approval history of the impact analysis, click the **Details** tab.

    1.  Click the Approval History related item.

        You can view the complete approval history of the approvers and the details as to when it was created.

    State transitions for multiple levels of BIA approvals:

    -   **Not Yet Requested**

        State where an approval is not yet sent to the approvers at a respective level.

    -   **Requested**

        Approvals are sent to the approvers of that level. Correspondingly, the state of all successive levels of approvals turns to Not Yet Requested.

    -   **Approved**

        One or more approvers have approved the BIA at the respective level. Correspondingly, the state of the succeeding level of approval moves to Requested.

    -   **Rejected**

        One or more approvers have rejected the BIA at a particular level. Even if one approver rejects the BIA, then it moves to **Rejected** state. Correspondingly, the state of all succeeding levels of approvals moves to No Longer Required.

    -   **No Longer Required**

        If the approvers at a level have approved or rejected the BIA, then the state moves to No Longer Required for all succeeding levels of approvals.


**Parent Topic:**[Assess impact categories and dependencies of a process](assess-impact-categories-bia.md)

