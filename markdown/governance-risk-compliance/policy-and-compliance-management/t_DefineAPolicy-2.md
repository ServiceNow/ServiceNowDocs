---
title: Create a policy
description: A policy defines an internal practice that processes must follow. Policies are defined as policies, procedures, standards, plans, checklists, frameworks, and templates.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Mandatory setup, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a policy

A policy defines an internal practice that processes must follow. Policies are defined as policies, procedures, standards, plans, checklists, frameworks, and templates.

## Before you begin

Role required: sn\_compliance.admin or sn\_compliance.manager

Users with Compliance user \(sn\_compliance.user\) role can also create policies.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Policies**.

2.  Click **New**.

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

Owning Group

</td><td>

Group that owns the policy.

</td></tr><tr><td>

Owner

</td><td>

User that owns the policy.

</td></tr><tr><td>

Compliance Score Percentage

</td><td>

The compliance score percentage assigned to this policy.

</td></tr><tr><td>

Parent

</td><td>

The policy containing this policy. If you create a control objective from within a policy, this field is automatically filled.

</td></tr><tr><td>

Policy categories

</td><td>

Click the lock icon and select one or more categories for filtering policies. For example, select Vulnerability Response to view policies associated with that application.

</td></tr><tr><td>

State

</td><td>

The state is a read-only field. Possible choices are: -   **Draft** In this state, all compliance users can modify the policy and control objectives. All compliance users can click **Request review** button. Enter a message in the Request review pop-up and click **Request**, which sets the state to Review.
-   **Review** In this state, the owner, owning group, and reviewers can modify the policy and control objectives. The owner, owning group, and reviewers move the policy back to Draft, by clicking **Back to draft**, as well.

Reviewers cannot request approval for a policy. However, the owner of the policy with sn\_compliance.user, which is the minimum required role, and users with compliance manager role can request approval for a policy.

-   **Awaiting approval** In this state, the policy and control objectives are read- only for all. Approvers can approve the policy by updating the approval state in the **Approvals** Related List on the policy form, or by viewing **My Approvals**. If the policy is approved, the policy goes to the **Published** state. Otherwise, it goes back to the **Review** state.
-   **Published** In this state, the policy and control objectives are read-only for all. Admins can click **Retire** which sets the state of the policy to **Retired**
-   **Retired** In this state, the policy is read-only for all.


</td></tr><tr><td>

Valid from

</td><td>

Specifies the date and time when the policy becomes effective.

</td></tr><tr><td>

Valid to

</td><td>

Specifies the date and time until which the policy remains valid.**Note:**

By default, when a policy expires, it doesn't automatically trigger a new approval process. Instead, it remains in the **Published**state until the specified number of days \(configured in the **Policy and Compliance** &gt; **Administration** &gt; **Properties** page\) have passed.

After this period, the policy transitions to either the **Review** state \(if reviewers are assigned\) or the **Draft** state \(if no reviewers are assigned\).

The field specifying the number of days is labeled: **Number of days after reaching a policy 'Valid to' date in which the expired policy will automatically move from its Published state back to a Draft/Review state**.

</td></tr><tr><td>

Approvers

</td><td>

The users you want to be included in the approval process.

</td></tr><tr><td>

Reviewers

</td><td>

Select the users you want to be included in the review process.

</td></tr><tr><td>

Description

</td><td>

A general description of the policy.

</td></tr><tr><td>

Policy text

</td><td>

A detailed description of the policy.

</td></tr><tr><td class="sub-head" colspan="2">

Knowledge Base

</td></tr><tr><td>

Knowledge base

</td><td>

The knowledge base article related to this policy.

</td></tr><tr><td>

KB article

</td><td>

The KB article number and link where the policy is published.

</td></tr><tr><td>

Article template

</td><td>

The article template to use for the publication of this policy.

</td></tr><tr><td class="sub-head" colspan="2">

Acknowledgement Setup

</td></tr><tr><td>

Audience

</td><td>

Select the default audience responsible for acknowledging this policy.

</td></tr><tr><td>

Reference Material URL

</td><td>

Click the lock icon to add the URL for any needed reference materials, such as certification or training materials.

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
</table>4.  Continue with one of the following options.

    -   To save and submit the policy, click **Submit**.
    -   To mark the policy ready for review, click **Request review**.

## What to do next

If you are implementing the [Policy and Compliance Management](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) software, return to the [Policy and Compliance Management setup checklist](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) and proceed to the next step.

**Parent Topic:**[Policy and Compliance Management mandatory setup](../../grc-policy-compliance-implementation/concept/policy-compliance-mandatory-setup.md)

**Parent Topic:**[Manage control objectives and policies](../reference/r_PoliciesAndProcedures.md)

