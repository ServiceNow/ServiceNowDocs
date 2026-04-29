---
title: Add adhoc approvers to an HR case in the Agent Workspace for HR Case Management
description: Provide your agents with the flexibility to add adhoc approvers to a case that is part of an HR service.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Add adhoc approvers to an HR case in the Agent Workspace for HR Case Management

Provide your agents with the flexibility to add adhoc approvers to a case that is part of an HR service.

## Before you begin

For example, in certain scenarios where in an employee's requests falls outside the bounds of the standard process or the agent needs to take an additional approval, an HR agent might need to request an adhoc approval before proceeding with its fulfillment.

Role required: sn\_hr\_core.case\_writer

## Procedure

1.  Navigate to **Workspace** &gt; **HR Agent Workspace**.

2.  Open the case that is assigned to you.

3.  Click **More actions** and select **Add an approval**.

    **Note:**

    -   Administrator must have configured the **Agent Can Add An Approval** option on the HR service to which the HR case is associated.
    -   This option appears only to the **Assigned to** user when the case is in the **Ready** or **Work in progress** state.
4.  Fill in the required fields in the **Add an approval** window.

<table id="table_pwm_pr2_mtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approver users

</td><td>

Users who must approve the request.

</td></tr><tr><td>

Wait for

</td><td>

Conditions that you want to set for the approval flow. -   **Anyone to approve**: If any one of the approvers approves the request, the approval flow will be complete.
-   **Everyone to approve**: Only if all the approvers approve the request, the approval flow will be complete.
-   **First response from anyone**: The first response of any one approver is taken into consideration. For example, if one of the approvers first rejects the request, the flow will be rejected; if one of the approvers first approves the request, the flow will be approved.


</td></tr><tr><td>

On rejection

</td><td>

Conditions that you want to set when an approver rejects a request, for example, allow resubmission of approvals, or mark it as close incomplete.

</td></tr><tr><td>

Reason

</td><td>

Reason for initiating the approval flow.

</td></tr><tr><td>

Additional Comments

</td><td>

Any other information that you want to share with the approvers.

</td></tr></tbody>
</table>5.  Click **Submit**.


