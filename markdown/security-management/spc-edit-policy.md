---
title: Edit an activated policy in Security Posture Control
description: You can edit activated policies to help you customize their conditions to better match your assets.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Edit an activated policy in Security Posture Control

You can edit activated policies to help you customize their conditions to better match your assets.

## Before you begin

You cannot edit the policies that are included with the application, but you can clone and create child policies from them. See [Clone a policy or create a child policy in Security Posture Control](spc-clone-policy.md).

If you edit policies and publish your changes, versions are tracked and version numbers are displayed on the policy record and its related test results.

Before you edit an activated policy, you might prefer to deactivate it so that the policy does not continue to evaluate your assets while you edit.

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **List** &gt; **Policies** &gt; **All**.

2.  Select a policy record to open it.

3.  Select **Edit policy**.

    If you are editing for the first time, two deactivated buttons are displayed next to the active **Exit edit mode** button: **Save changes** and **Publish changes**. If you have previously edited this policy and saved it as a draft, the notification, `You have an unpublished edit` is also displayed.

4.  Make your edits and choose one to continue.

<table id="id_qyh_1yy_hbc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Save changes

</td><td>

Save your changes as a draft and return to editing mode. Your changes are not published at this point, and you can return to the policy and continue editing later.

</td></tr><tr><td>

Publish changes

</td><td>

Publish your changes as a new version of the policy and automatically exit edit mode. It may take some time for findings to display on your new version of the policy on the View findings button on the policy.

If you publish a new version of a policy, you have the option to close any existing findings for the policy that you changed. You might prefer to close any existing findings from the original policy if you only want to view findings for your changed policy.

If you cancel at this point or exit edit mode, a message is displayed that you have an unpublished edit for this policy.

If you choose to close its existing related test results \(findings\), test result and remediation task states transition in accordance with the state transition processes of the Configuration Compliance application. See [Test result and remediation task state transitions in the Security Posture Control application](../concept/spc-findings-state-transition.md) for more information.

</td></tr><tr><td>

View version history

</td><td>

For published changes, versions are tracked and version numbers are displayed on the policy record and its related test results.

</td></tr><tr><td>

Exit edit mode

</td><td>

Exit without saving your changes or save your changes and exit without publishing. If you save your changes and don’t publish them, you must publish your new version before it can create findings.

</td></tr><tr><td>

Deactivate policy \(Displayed on activated policies only\)

</td><td>

Deactivate an active policy if you don’t want any assets to be monitored or evaluated against that policy. This editing option is only visible on active policy records.

</td></tr><tr><td>

View findings

</td><td>

Open a new tab and view the matching assets if available. Findings are also referred to CTRs or test result records for the policy.

</td></tr></tbody>
</table>5.  After you save the policy as a draft and exit edit mode, select from the following options:

<table id="table_ecf_wxl_dcc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Edit policy

</td><td>

Return to edit mode.

</td></tr><tr><td>

Deactivate policy \(Displayed on activated policies only\)

</td><td>

Deactivate an active policy if you don’t want any assets to be monitored or evaluated against that policy.

 This option is only visible on active policy records.

</td></tr><tr><td colspan="2">

More options menu

</td></tr><tr><td>

Configure findings

</td><td>

Select **Yes** in the modal to generate findings for the policy. See [View findings for Security Posture Control](spc-view-findings.md).

</td></tr><tr><td>

Clone policy

</td><td>

Create a copy of the policy record. See [Clone a policy or create a child policy in Security Posture Control](spc-clone-policy.md).

</td></tr><tr><td>

Create child policy

</td><td>

Create a new policy using this policy as a base. See [Clone a policy or create a child policy in Security Posture Control](spc-clone-policy.md).

</td></tr><tr><td>

Delete policy

</td><td>

Remove the policy record from the policy list.

</td></tr><tr><td>

View findings

</td><td>

Open a new tab and view the matching assets if available. Findings are also referred to test result records \(CTRs\) for the policy.

</td></tr><tr><td>

View linked records

</td><td>

For published policies, view custom insights if available. See [Create and activate a configured insight for Security Posture Control](spc-create-custom-insight.md)

</td></tr></tbody>
</table>
