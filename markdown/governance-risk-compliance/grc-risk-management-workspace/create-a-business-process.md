---
title: Create a business process
description: Create a business process and define the owners, approvers, business criticality, and review frequency for the process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/create-a-business-process.html
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage a business process, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a business process

Create a business process and define the owners, approvers, business criticality, and review frequency for the process.

## About this task

Business processes are a foundational component of the Common Services Data Model \(CSDM\) design framework within GRC Risk Management. They represent key operational processes within your organization that support business objectives and are subject to risk assessment and governance.

The criticality assessment captured when creating a business process provides an initial subjective evaluation of the process's importance to your organization. This assessment complements the formal Business Impact Analysis \(BIA\) process performed by your risk and business continuity teams, which occurs separately as part of your broader business impact assessment workflow. The system automatically computes a "determined" criticality based on subprocess assessments, which can differ from your initial declared assessment.

**Note:** Organizational context such as Business Unit, Department, and Location are captured in the CSDM Entity records rather than in the Business Process form itself. When setting up process ownership and governance, ensure these organizational entities are properly configured to link to your business processes.

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

Your subjective assessment of the business process criticality based on business judgment. This is separate from the formal Business Impact Analysis \(BIA\) assessment performed by risk teams. The choices represent increasing levels of organizational dependency: -   **1- most critical** \(essential to business operations\)
-   **2- somewhat critical** \(important but with some redundancy\)
-   **3- less critical** \(limited business impact if interrupted\)
-   **4- not critical** \(minimal business impact\)
This value may be revised after the formal BIA process is completed.

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

System-computed criticality based on the aggregate assessment of all subprocesses using the same scale \(1- most critical through 4- not critical\). This calculated value may differ from your initially declared criticality and provides a data-driven perspective on process importance across your process hierarchy. The determined value is updated automatically when subprocess assessments change.

</td></tr><tr><td>

Impact to integrity

</td><td>

Risk rating for the risk of impact to integrity. Impact to integrity has consequences for businesses and employees, including fines and damage to your brand, reputation, and people. The choices are the following:-   **High**
-   **Medium**
-   **Low**


</td></tr><tr><td class="sub-head" colspan="2">

Organizational Context

</td></tr><tr><td>

Business Unit

</td><td>

The Business Unit is not captured directly on the Business Process form. Instead, business unit ownership is managed through the CSDM Entity hierarchy. Associate your business process to the appropriate organizational entity \(such as Finance, Operations, IT\) by linking the process to that entity in the CSDM design. This allows the system to track process ownership by organizational unit and supports reporting by business unit.

</td></tr><tr><td>

Department

</td><td>

The Department context is captured in the CSDM Entity records. When setting up your business process hierarchy, ensure the parent entity or owner is assigned to the appropriate department. This provides visibility into which departments manage and depend on specific processes.

</td></tr><tr><td>

Process Location

</td><td>

The location or locations where the business process is executed are captured in the associated CSDM Entity records, not in the Business Process form itself. If your process operates across multiple geographic locations \(e.g., office locations, data centers\), ensure the entity records associated with process ownership reflect all relevant locations. This supports location-based risk assessment and regulatory compliance mapping.

</td></tr></tbody>
</table>4.  Right-click on the form header and click **Save**.

    The record moves to the Draft state.

5.  To send the record for review and approval, click **Review**.

    The values in the **Life cycle stage** field and the **Life cycle stage status** field change. The Approvals related list appears, and the members of the Approval list can view the record in their list of approvals.


-   **[Approve, reject, or delete a business process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-management-workspace/review-a-business-process.md)**  
If a new business process has identified approvers, then the approvers must review and approve the process before it can be published. The approvers can also reject or delete the process as necessary.

**Parent Topic:**[Manage a business process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-management-workspace/use-business-process.md)

