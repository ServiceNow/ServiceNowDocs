---
title: Create a business process in the Risk Workspace
description: Create a business process in the Risk Workspace and define the owners, approvers, business criticality, and review frequency for the process.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Create a business process in the Risk Workspace

Create a business process in the Risk Workspace and define the owners, approvers, business criticality, and review frequency for the process.

## Before you begin

Role required: Enterprise architect or service owner or itil

## About this task

When you create a business process, it is important to ascertain the CIA triad. CIA triad refers to confidentiality, integrity, and availability. The CIA triad is a common model that forms the basis for the development of security systems and policies. These are used for the identification of vulnerabilities and methods for addressing problems and creating solutions.

## Procedure

1.  Navigate to **All** &gt; **Risk Workspace** &gt; **Lists** &gt; **Business Processes**.

2.  Click **Create New**.

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

Description

</td><td>

Description of the business process.

</td></tr><tr><td>

Parent

</td><td>

Parent business process, if it exists, to create a hierarchy of business processes.

</td></tr><tr><td>

Review frequency

</td><td>

Frequency for reviewing the business process.

</td></tr><tr><td class="sub-head" colspan="2">

Ownership

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Life cycle stage

</td><td>

Stage of record in the business life cycle. The stage determines the status and displays the actions. This field is automatically set to **Ideation** when you save the form for a process in **Draft** state.

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

</td></tr><tr><td>

Life cycle stage status

</td><td>

Status of business process within the life cycle stage. This field is automatically set to **Under Evaluation** when you save the form for a process in **Draft** state.

</td></tr><tr><td>

Next review date

</td><td>

Planned date on which the business process must be reviewed. The value in this field is automatically set only after the business process is approved.

</td></tr><tr><td>

Description

</td><td>

Short description of the business process. The description can include the background, the actual steps, and the interaction of the process.

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

Business criticality determined

</td><td>

Computed criticality of the business process based on the assessment of the sub-processes. The choices are:-   **1- most critical**
-   **2- somewhat critical**
-   **3- less critical**
-   **4- not critical**


</td></tr><tr><td class="sub-head" colspan="2">

CIA triad

</td></tr><tr><td>

Impact to confidentiality

</td><td>

Risk rating for the risk of loss of confidentiality for the process. The choices are:-   **High**
-   **Medium**
-   **Low**


</td></tr><tr><td>

Impact to integrity

</td><td>

Risk rating for the risk of impact to integrity for the process. The choices are:-   **High**
-   **Medium**
-   **Low**


</td></tr><tr><td>

Impact to availability

</td><td>

Risk rating for the risk of loss of availability for the process. The choices are:-   **High**
-   **Medium**
-   **Low**


</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>4.  Right-click and save the form.

    The record moves to the **Draft** state.


-   **[Add related assets to a business process](add-related-assets-to-a-bp.md)**  
Add related business assets to a business process to gain visibility into the IT assets and their performance.

**Parent Topic:**[Using the Risk Workspace](../concept/using-risk-workspace.md)

**Related topics**  


[Add related assets to a business process](add-related-assets-to-a-bp.md)

