---
title: Create a policy using the Compliance Workspace
description: A policy defines an internal practice that processes must follow. You can define policies using the Compliance Workspace as policies, procedures, standards, plans, checklists, frameworks, and templates.
locale: en-US
release: zurich
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage control objectives and policies, Use, GRC Compliance Workspace, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a policy using the Compliance Workspace

A policy defines an internal practice that processes must follow. You can define policies using the Compliance Workspace as policies, procedures, standards, plans, checklists, frameworks, and templates.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst or sn\_compliance\_ws.corporate\_compliance\_manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Select the **Create** list and select **Policy** from the **Home** page.

3.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the policy.

</td></tr><tr><td>

Type

</td><td>

List of options:

 -   Policy
-   Procedure
-   Standard
-   Plan
-   Checklist
-   Framework
-   Template


</td></tr><tr><td>

Parent

</td><td>

The policy containing this policy. If you create a control objective from within a policy, this field is automatically filled.

</td></tr><tr><td>

Policy categories

</td><td>

Select the lock icon and select one or more categories for filtering policies. For example, select Vulnerability Response to view policies associated with that application.

</td></tr><tr><td>

Description

</td><td>

A general description of the policy.

</td></tr><tr><td>

Policy text

</td><td>

A detailed description of the policy.

</td></tr><tr><td>

State

</td><td>

The state is a read-only field. Possible choices are: -   **Draft** In this state, all compliance users can modify the policy and control objectives. All compliance users can select **Request review** button. Enter a message in the Request review pop-up and select **Request**, which sets the state to Review.
-   **Review** In this state, the owner, owning group, and reviewers can modify the policy and control objectives. The owner, owning group, and reviewers select **Request approval**, starting the workflow by sending approvals to the users in the Approvers list. The owner, owning group, and reviewers move the policy back to Draft, by selecting **Back to draft**, as well.
-   **Awaiting approval** In this state, the policy and control objectives are read-only for all. Approvers can approve the policy by updating the approval state in the Approvals related list of the policy form, or by viewing **My Approvals**. If the policy is approved, the policy goes to the **Published** state. If the policy is rejected, then it goes back to the **Draft** state.
-   **Published** In this state, the policy and control objectives are read-only for all. Admins can select **Retire** which sets the state of the policy to **Retired**
-   **Retired** In this state, the policy is read-only for all.


</td></tr><tr><td>

Compliance Score Percentage

</td><td>

The compliance score percentage assigned to this policy.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Owning Group

</td><td>

Group that owns the policy.

</td></tr><tr><td>

Approvers

</td><td>

The users you want to be included in the approval process.

</td></tr><tr><td>

Approval method

</td><td>

Approval method for dynamic approval configuration. Available options are:-   Manually select approvers
-   Use approval rules


</td></tr><tr><td>

Approvers

</td><td>

Approvers to be selected for the policy.

</td></tr><tr><td>

Reviewers

</td><td>

Select the users that you want to be included in the review process.

</td></tr><tr><td>

Contributors

</td><td>

Contributors selected for the policy.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Valid from

</td><td>

The date and time for which the policy becomes valid.

</td></tr><tr><td>

Valid to

</td><td>

The date and time for which the policy is no longer valid.

</td></tr><tr><td class="sub-head" colspan="2">

Knowledge Base

</td></tr><tr><td>

Policy template

</td><td>

The article template to use for the publication of this policy.

</td></tr><tr><td>

Policy knowledge base

</td><td>

The knowledge base article related to this policy.

</td></tr><tr><td>

Published policy

</td><td>

The KB article number and link where the policy is published.

</td></tr><tr><td class="sub-head" colspan="2">

Acknowledgement setup

</td></tr><tr><td>

Audience

</td><td>

Select the default audience responsible for acknowledging this policy.

</td></tr><tr><td>

Reference Material URL

</td><td>

Select the lock icon to add the URL for any needed reference materials, such as certification or training materials.

</td></tr><tr><td>

Allow users to decline policy

</td><td>

Select this check box to give users the option of declining policy acknowledgements.

</td></tr><tr><td>

Allow users to request exception

</td><td>

Select this check box to give users the option of requesting exceptions for policy acknowledgements.

</td></tr><tr><td class="sub-head" colspan="2">

Exception Setup

</td></tr><tr><td>

Maximum exception duration \(days\)

</td><td>

Enter the maximum number of days for which a policy exception can be requested for a given policy.

</td></tr></tbody>
</table>4.  Select **Save**.

    In the reporting overview page of the policy, you can see the description of the policy, its state, and its status of overall compliance, entities, control objectives, and control. It also gives you the tracking information of policy acknowlegements, policy exceptions, and issues. The non-compliant entities widget also lists all the non-compliant reliant entities, each with its compliance score. For more information, see [Manage compliance of a policy from the overview page](../concept/policy-overview-pc-ws.md)

5.  Select any of the related lists to provide more information for the policy.

6.  From the **Overview** page, select the **Issues** tab.

    You can add existing one or more related issues to the policy that you created. By mapping the existing issues to the policy, you can reduce the count of open issues.

    1.  Select the **Add** button.

    2.  Select a related issue or issues from the Issues pop-up.

    3.  Select **Add**.

        The selected issues are added to the policy as related issues and an m2m relationship is created between the policy and the issues in the Issue to Document \[sn\_grc\_m2m\_issue\_document\] table. You can also create an issue for the policy by selecting the **New** button, which takes you to the Create New Issue form.

    4.  To remove an issue that is mapped to the policy, select the issue and select **Remove**.

        The remove action only removes the mapping or the association between the policy and the issue in the m2m table and doesn’t delete the issue record.

        **Note:** The UI action buttons such as New, Add, Remove aren’t available if the policy is in Draft or Retired state. A policy in draft state is considered inactive and becomes active when it moves to Review state.

7.  To mark the policy ready for review, select **Request review**.


