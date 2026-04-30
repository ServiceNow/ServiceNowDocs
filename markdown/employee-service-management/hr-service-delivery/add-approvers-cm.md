---
title: Add adhoc approvers to a case
description: Provide your agents with the flexibility to add adhoc approvers to a case that is part of an HR service.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work an HR case, HR Case Management, Explore and use HR Case and Knowledge Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add adhoc approvers to a case

Provide your agents with the flexibility to add adhoc approvers to a case that is part of an HR service.

## Before you begin

For example, in certain scenarios where in an employee's requests falls outside the bounds of the standard process or the agent needs to take an additional approval, an HR agent might need to request an adhoc approval before proceeding with its fulfillment.

Role required: sn\_hr\_core.case\_writer

## Procedure

1.  Navigate to **HR Case Management** &gt; **Assigned to me**.

2.  Open a case that is in Ready or Work in progress state.

3.  In the **Related links** list, click **Add an approval**.

    **Note:**

    -   This option appears only to the Assigned to user, when the case is in Ready or Work in progress state.
    -   Administrator must have configured the **Agent Can Add An Approval** option on the HR service to which the HR case is associated.
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
</table>5.  Click **Send for approval**.


**Parent Topic:**[Work an HR case](t_CreateAnHRCase.md)

