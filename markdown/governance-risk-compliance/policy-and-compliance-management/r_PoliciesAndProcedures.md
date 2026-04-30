---
title: Manage control objectives and policies
description: The Policies and Procedures module contains overview and detailed information related to policy approvals, policies, and control objectives.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Using the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manage control objectives and policies

The Policies and Procedures module contains overview and detailed information related to policy approvals, policies, and control objectives.

## Policies and Procedures Overview

**Policies and Procedures Overview** is contained in the **Policies and procedures** module and provides an executive view into compliance requirements, overall compliance, and compliance breakdowns so areas of concern can be identified quickly. Users with the compliance administrator and compliance manager roles view the **Policies and Procedures Overview**.

|Name|Visual|Description|
|----|------|-----------|
|Control compliance|Donut chart![Donut icon](../../../use/performance-analytics/image/donut-icon.png)|Displays the overall compliance of all the controls in the system.|
|Control details|Donut chart![Donut icon](../../../use/performance-analytics/image/donut-icon.png)|Displays a breakdown of controls grouped by owner, category, or type.|
|Control Overview|Column Chart![Column icon](../../../use/performance-analytics/image/column-icon.png)|Displays the total number of controls related to each policy. The chart is stacked to display the overall control compliance status for each policy.|
|Control Issues by Policy \(Opened Date\)|Line Chart![Line icon](../../../use/performance-analytics/image/line-icon.png)|Displays the number of control issues opened each week, grouped by policy.|
|Policy Exceptions|List|Displays a list of control issues that have been closed with a response value of accept, meaning the issue was not remediated.|
|Total Control Objectives by Policy|Bar graph|Displays a count of the overall number of control objectives in each policy. The chart is stacked to display control objectives by type.|

## Policy approval process

Policies are part of a strict approval process that ensures compliance and reduces exposure to risk. When a policy is published, it is automatically incorporated in the approval process. Compliance managers set the length of time that policies are valid, ensuring that the team reviews the policy often to affirm its validity. Policies have a type, such as a policy, procedure, standard, plan, checklist, framework, or template.

![The image depicts the approval process flow that is shown at the top of each policy record.](../image/GRCPolicyApprovalProcess.png)

<table id="table_amh_4kb_cv"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

All policies start in **Draft** state. In this stage, all compliance users can modify the policy and control objectives.

</td></tr><tr><td>

Review

</td><td>

The owner, owning group, and reviewers can modify the policy and control objectives and send it on to the next state.

</td></tr><tr><td>

Awaiting Approval

</td><td>

The policy is read only in this state. Approved policies transition to the **Published** state. Unapproved policies return to **Review**. If no approvers are identified on the policy form, the state is skipped and the policy is published without an approval.

</td></tr><tr><td>

Published

</td><td>

Approved policies are automatically published to a template-defined KB article, and the policy remains in a read-only state. The **Valid to** field on the policy form defines how long the policy is valid. **Note:** After the policy is published and when the valid to date on the policy is reached, then based on the value of the **Number of days after reaching a policy "Valid to" date in which the expired policy will automatically move from its Published state back to a Draft/Review state** property, the policy moves back to the Draft/Review state. For example, if the value of the property is 10, then the policy moves back to review state 10 days after the valid to date is reached.

 When a policy reaches the end of the **Review** state and is **Approved** for publishing, it is automatically published to the GRC knowledge base \(as defined in **Policy and Compliance** &gt; **Administration** &gt; **Properties**. The **Article template** field on the policy form defines the style of the published policy.

</td></tr><tr><td>

Retired

</td><td>

When a policy is put into the **Retired** state, its associated KB article is removed.

</td></tr></tbody>
</table>## Policies

Compliance managers catalog and publish internal policies that define a set of business processes, procedures, and or standards.

## Control objectives

Compliance managers catalog the control objectives and generate controls from those control objectives.

**Note:** UCF refers to control objectives as controls. When UCF data is imported, controls are imported into the control objectives table.

-   **[Create a policy](../task/t_DefineAPolicy.md)**  
A policy defines an internal practice that processes must follow. Policies are defined as policies, procedures, standards, plans, checklists, frameworks, and templates.
-   **[Approve and publish a policy](../task/t_ApprovePolicy.md)**  
When a policy is approved, it is automatically published.
-   **[Acknowledge a policy](../concept/ack-policy.md)**  
After a policy has been published, you can create an acknowledgement campaign to define a group of your employees who must provide an acknowledgement that a particular policy is in compliance. When the campaign has been defined, you can submit the request to the audience.
-   **[Retire a policy](../task/t_RetireAPolicy.md)**  
Retiring a policy is part of the policy management process.
-   **[Create a GRC article template](../task/t_CreateArticleTemplate.md)**  
Policy and Compliance managers can create templates for policy article publishing.
-   **[Create a control objective](../task/t_CreateAPolicyStatement.md)**  
A control objective is an objective, direction, or standard that acts as guidance for company interactions and operations. Control objectives can be categorized, classified, and related to policies.
-   **[Deactivate a control objective](../task/t_DeactivateAPolStatement.md)**  
Deactivate control objectives that are no longer relevant to their citation or parent control objective.
-   **[Relate a control objective to a policy](../task/t_RelatePolicyStateToPolicy.md)**  
Associate the control objective to a policy individually when the policy is in the review or draft state by clicking the edit button in the Control Objective related list.
-   **[Relate a control objective to a citation](../task/t_RelatePSToACitation.md)**  
A single control objective can be mapped to many citations from different authority documents. This function allows you to test a control objective once while complying with many different citations.
-   **[Create or deactivate a citation](../task/t_CreateCitations.md)**  
Usually, authority documents, citations, and control objectives are downloaded from a third-party provider. However, citations can be created manually from an authority document. The **Active** option in a citation indicates whether the citation is active or inactive.
-   **[Create an authority document](../task/t_CreateAnAuthorityDocument.md)**  
Authority documents manage a process and citations are created within them to manage points of the process. For example, the process called Building Security contains a citation for Entry Control.
-   **[Deactivate an authority document](../task/t_DeactivateAnAuthorityDoc.md)**  
The **Active** option in an authority document indicates whether the authority documents have been retired.

**Parent Topic:**[Using the Classic user interface for Policy and Compliance tasks](../concept/using-policy-compliance-legacy-ui.md)

