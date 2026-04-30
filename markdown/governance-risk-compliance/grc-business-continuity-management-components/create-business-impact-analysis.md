---
title: Create a business impact analysis
description: Create a business impact analysis \(BIA\) to get the necessary information for a plan. Use the BIA to identify the recovery time objective for an item and prioritize assets that have most and least critical dependencies. Use the information to establish their recovery strategies during the planning phase.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BIA, Using BCM Classic Workspace, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a business impact analysis

Create a business impact analysis \(BIA\) to get the necessary information for a plan. Use the BIA to identify the recovery time objective for an item and prioritize assets that have most and least critical dependencies. Use the information to establish their recovery strategies during the planning phase.

## Before you begin

Role required: sn\_bcm.program\_manager or sn\_bcm.planner

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click **Start a BIA** in the **Actions** section.

3.  On the form, fill in the fields.

<table id="table_ok1_xrr_dnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the business impact analysis. Describe the BIA within 255 characters length.

</td></tr><tr><td>

Template

</td><td>

Template that you can use as a model to create the BIA.The template BIA has the primary elements \(applications, business processes, and locations\), impact categories, and the dependent assets identified for the type of assessment.

</td></tr><tr><td>

Applies to table

</td><td>

Table that stores the template's primary element data.

</td></tr><tr><td>

Applies to

</td><td>

Business process, business application, or any other asset that is assessed in the BIA.

</td></tr><tr><td>

Business Unit

</td><td>

Business unit that uses the business process and for which the BIA is assessed.

</td></tr><tr><td>

Department

</td><td>

Department which uses the business process.

</td></tr><tr><td>

BIA Owner

</td><td>

Person who owns and is responsible for completing the BIA. BCM lead can review the BIA.

</td></tr></tbody>
</table>4.  Click **Submit**.

    A BIA is created in **In Draft** state.

    State transitions for a BIA:

    -   **In Draft**

        It is the state where your BIA is under edit. Add RTO, RPO, and dependency assessments. Either you can submit the BIA for review, in which case confirm that a BCM Lead is assigned to the BIA. Or, as a BIA owner you can submit the BIA for approval.

    -   **In Review**

        Review the BIA and submit it for approval. In this state, the BCM admin can modify the BIA owner and BCM lead.

    -   **Pending Approval**

        When you click **Submit for Approval**, the BIA is set to **Pending Approval** state. The approval configurations, approval levels, and approval rules are evaluated against the BIA to determine the approvers. If there are no approval records in the requested state for the BIA, then as a BCM program manager you can either **Reject** or **Approve**. You must add RTO, RPO, and dependency assessments before you submit for approval. In pending approval state, the BIA is read only and the RTO, RPO, and dependency assessment details cannot be modified. The state of the plan and its related tables becomes read only.

    -   **Returned**

        BIA is editable. BCM admin can change the BIA owner in this state. When the BIA is rejected, it is set to **Returned** state.

    -   **Approved**

        When a BIA is in an approved state, it becomes read only and the RTO, RPO, and dependency assessment details cannot be modified. Your only option to change the status is to move it to **Archived** state.

    -   **Archived**

        When the BIA is archived, it becomes read only. All the underlying tables like impact dependency groups, impact category results, and dependencies from where the BIA retrieves data to populate in the impact assessment and dependency assessment tabs become read only. You can no longer edit the information in these tabs. In this state, you can also generate a PDF of the BIA.

    **Note:** A scheduled job runs weekly to move the BIAs that have expired to **Archived** state.


**Parent Topic:**[Structured workflows for Business Impact Analysis](../concept/structured-workflows-bia.md)

