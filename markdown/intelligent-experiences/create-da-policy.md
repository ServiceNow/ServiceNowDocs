---
title: Create a desktop action policy
description: Desktop action policies control which users are subject to resource access rules. Configure a policy to define the user criteria and link the rules that govern automated resource access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-da-policy.html
release: australia
topic_type: task
last_updated: "2026-08-21"
reading_time_minutes: 2
breadcrumb: [Control resource access, Adaptive desktop actions for desktop and web, Configure, AI Desktop Actions, Enable AI experiences]
---

# Create a desktop action policy

Desktop action policies control which users are subject to resource access rules. Configure a policy to define the user criteria and link the rules that govern automated resource access.

## Before you begin

This task must be performed in the ServiceNow instance.

Role required: sn\_aia.admin

## About this task

The Desktop action policy form includes the following fields and the Resource Access Rules related list.

\[Omitted image "da-resource-policy-form.png"\] Alt text: Desktop action policy with form fields and rules related list.

## Procedure

1.  Navigate to **All** &gt; **AI Desktop Actions** &gt; **Desktop Action Policies**.

2.  Select **New**.

3.  On the Desktop action policy form, fill in the fields.

<table id="table_wfy_wzv_hkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

A descriptive name for the policy. Use concise, role-specific or function-specific names so administrators can identify the policy's purpose.Example: Finance Team Policy, IT Operations Policy, Sales Read-Only

</td></tr><tr><td>

Active

</td><td>

Option to enforce the policy. Only active policies are applied to the users. Deactivated policies are stored but not enforced.**Note:** You must add at least one resource access rule to the policy before activating it.

To use an existing rule: Save your policy first, then navigate to the Resource Access Rule record and link this policy from its Policies related list. This saves you from recreating the same rule. Once linked, return to the policy and activate it.

</td></tr><tr><td>

User criteria

</td><td>

Defines users who are subject to this policy.Supports Users, Groups, Roles, Departments, Locations, Companies, and Match All. When left blank, no restriction is applied.

Example: "members of Finance group" or "users assigned to Accounting role" or "users in Marketing department"

</td></tr><tr><td>

Description

</td><td>

Description of the policy explaining the policy's purpose, affected resources, and rationale.Example: "Restricts automated access to payroll, HR records, and financial reports for non-Finance users. Finance team members can manually access these resources when needed."

</td></tr></tbody>
</table>4.  From the form header, select **Save**.

5.  Add rules to the policy.

    You can either create rules for this policy or link existing rules. Rules can be linked to multiple policies, so you can reuse rules across different policies.

    -   From the Resource Access Rules related list, select **New** to create a resource access rule. For more information, see [Create a desktop action access rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-da-access-rule.md).
    -   To link an existing resource access rule, navigate to the Resource Access Rule record. On the Policy related list, select **Edit** to add the policies to link to this rule. For more information, see [the step for linking policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-da-access-rule.md).
6.  On the Desktop action policy form, select **Active**.

7.  Select **Submit**.


**Parent Topic:**[Controlling what AI Desktop Actions can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/security_policy_governance_concept.md)

