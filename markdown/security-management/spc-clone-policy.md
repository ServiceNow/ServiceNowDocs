---
title: Clone a policy or create a child policy in Security Posture Control
description: Clone an existing policy and add conditions to it to create your own custom policy. You can also create child policies from existing policies.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Clone a policy or create a child policy in Security Posture Control

Clone an existing policy and add conditions to it to create your own custom policy. You can also create child policies from existing policies.

## Before you begin

You can clone policies to create your own custom policies. You can clone a policy or create a child policy using any policy as a base to help you extend the existing policies without having to enter in the conditions again. All the conditions in the base policy are also inherited in the child policy. See [Clone a policy or create a child policy in Security Posture Control](spc-clone-policy.md) for more information.

You can clone any policies that are included with the application but policy matches are not reflected as key insights on the dashboard on the Home landing page. Only key insights for policies that are included with the application are displayed on the Home landing page.

After you clone and activate any policies you create, you must create your own configured insight record in the Custom insight builder module in the workspace \(the last module in the navigator panel\). Only then can you view the data from your policies on the Configured insights dashboard \(the second icon from the top in the workspace\).

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **List** &gt; **Policies** &gt; **All**.

2.  Select the policy record that you want to clone.

3.  Select one from the more options menu next to **Activate policy**.

<table id="choicetable_mvf_ylm_dcc"><thead><tr><th align="left" id="d231837e120">

Option

</th><th align="left" id="d231837e123">

Description

</th></tr></thead><tbody><tr><td id="d231837e129">

**Clone policy**

</td><td>

Select this option if you want to use the conditions of an existing policy as a starting point for your new policy.

 A new tab with the cloned policy record is displayed with 'copy' in the name.

 \(Optional\) Select Base policy and add one from the list for your new policy.

</td></tr><tr><td id="d231837e147">

**Create child policy**

</td><td>

Select this option if you want to create a new policy using the current policy as a starting point.

 A new tab with a blank policy record with a base policy you choose is displayed.

</td></tr></tbody>
</table>4.  Select **Base policy** and select a policy as the base for your new policy.

    You might choose this option if you want to inherit the conditions of an existing policy as a starting point for your new policy.

5.  Select **Exclusion Policies** and select policies that you want to exclude from the findings of this policy.

    Any findings in your new policy that match any excluded policies are not included in your findings.

6.  For a cloned policy, edit the conditions.

    For more information about the Asset-connection-entity relationships in the condition builder, see [Policies for Security Posture Control](../concept/spc-policies-overview.md). For more information about the decorators in the condition builder, see [Creating your own policies in the Security Posture Control application](spc-creating-policies.md).

7.  Edit and Save your policy with **Save changes**.

    Your policy is displayed on the All list in the List module in the workspace.

8.  To activate a policy, follow the steps described in [Create and activate custom policies for Security Posture Control](spc-create-policy.md).

9.  Select Delete policy to delete a policy.

    The delete option is not supported for any policies that come with the application or for any policies that have generated findings. You can only deactivate policies with findings.


