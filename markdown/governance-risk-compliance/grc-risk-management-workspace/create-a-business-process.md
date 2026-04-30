---
title: Create a business process
description: Create a business process and define the owners, approvers, business criticality, and review frequency for the process.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage a business process, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a business process

Create a business process and define the owners, approvers, business criticality, and review frequency for the process.

## Before you begin

Role required: business\_process\_admin

## Procedure

1.  Navigate to **All** &gt; **CSDM** &gt; **Design** &gt; **Business Process**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the business process.

</td></tr><tr><td>

Parent

</td><td>

Parent business process. **Note:** If a parent process exists, it creates a hierarchy of business processes.

</td></tr><tr><td>

Life cycle stage

</td><td>

Stage of the business process in the business life cycle. The stage determines the status and displays the actions. **Note:** This field is automatically set to **Ideation** when you save the form for a process in the Draft state.

</td></tr><tr><td>

Review frequency

</td><td>

Frequency for reviewing the business process.

</td></tr><tr><td>

Life cycle stage status

</td><td>

Status of the business process within the life-cycle stages. **Note:** This field is automatically set to **Under Evaluation** when you save the form for a process in the Draft state.

</td></tr><tr><td>

Next review date

</td><td>

Planned date on which the business process must be reviewed. The value in this field is automatically set only after the business process is approved.

</td></tr><tr><td>

Description

</td><td>

Short description of the business process. The description can include the background, the actual steps, and the interaction of the process.

</td></tr><tr><td class="sub-head" colspan="2">

Ownership

</td></tr><tr><td>

Managed by group

</td><td>

Group that maintains the business process.

</td></tr><tr><td>

Approval group

</td><td>

Group that must review and approve the business process.

</td></tr><tr><td>

Owned by

</td><td>

User responsible for the business process. This user is a member of the Managed by group.

</td></tr><tr><td class="sub-head" colspan="2">

Business Impact

</td></tr><tr><td>

Business criticality declared

</td><td>

Criticality of the business process based on your subjective assessment. The choices are:-   **1- most critical**
-   **2- somewhat critical**
-   **3- less critical**
-   **4- not critical**


</td></tr><tr><td>

Impact to confidentiality

</td><td>

Risk rating for the risk of loss of confidentiality. Confidentiality loss leads to leakage of confidential information. The choices are the following:-   **High**
-   **Medium**
-   **Low**


</td></tr><tr><td>

Impact to availability

</td><td>

Risk rating for the risk of loss of availability. Unavailability of the system may cause delays in decision making, business interruptions, loss of revenue, and customer dissatisfaction. The choices are the following:-   **High**
-   **Medium**
-   **Low**


</td></tr><tr><td>

Business criticality determined

</td><td>

Computed criticality of the business process based on the assessment of the subprocesses. The choices are the following:-   **1- most critical**
-   **2- somewhat critical**
-   **3- less critical**
-   **4- not critical**


</td></tr><tr><td>

Impact to integrity

</td><td>

Risk rating for the risk of impact to integrity. Impact to integrity has consequences for businesses and employees, including fines and damage to your brand, reputation, and people. The choices are the following:-   **High**
-   **Medium**
-   **Low**


</td></tr></tbody>
</table>4.  Right-click on the form header and click **Save**.

    The record moves to the Draft state.

5.  To send the record for review and approval, click **Review**.

    The values in the **Life cycle stage** field and the **Life cycle stage status** field change. The Approvals related list appears, and the members of the Approval list can view the record in their list of approvals.


-   **[Approve, reject, or delete a business process](review-a-business-process.md)**  
If a new business process has identified approvers, then the approvers must review and approve the process before it can be published. The approvers can also reject or delete the process as necessary.

**Parent Topic:**[Manage a business process](../concept/use-business-process.md)

