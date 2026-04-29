---
title: Activate a policy included with the Security Posture Control application
description: Policies that are included with the application must be activated before Security Posture Control can monitor the assets that match that policy. By default, none of the policies included with the application are activated.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Activate a policy included with the Security Posture Control application

Policies that are included with the application must be activated before Security Posture Control can monitor the assets that match that policy. By default, none of the policies included with the application are activated.

## Before you begin

You must verify that all the required prerequisites are met before you activate the policies that are included with the application.

-   Verify required Service Graph Connectors activated.
-   Verify any required applications such as Vulnerability Response are installed and activated, if applicable.
-   For more information about policies used for mitigation controls monitoring, see [Mitigation controls policies](../concept/spc-mitigation-policies.md).

**Note:**

You cannot edit the policies that are included with the application, but you can create new policies based on their criteria with the **Clone policy** and **Create child policy** features. These features are available in the More options menu \(three vertical dots\).

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **Policies and findings** &gt; **All**.

    To determine if a policy is activated, confirm its status \(`true` or `false`\) in the Active column.

2.  Select a policy record to open it.

3.  You have the following options on policy records that are included with the application:

<table id="table_msw_fz5_lzb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate policy

</td><td>

Activate a policy if you want to monitor any assets that match the policy conditions and generate findings.

 If available, select Deactivate policy to stop asset evaluations and findings generation for this policy.

</td></tr><tr><td>

Configure findings

</td><td>

Select **Yes** in the modal to generate findings for the policy.

 Select the **Configure assignment rules** link to set up assignment rules in the Configuration Compliance application to assign any findings for your policy for resolution.

 **Note:** For policies you create with ‘Software’ as the Asset type, you can save the policy and create custom insights, but you cannot configure findings from the policy record.

</td></tr><tr><td>

Clone policy

</td><td>

Create a new policy with all the conditions from the displayed policy as a starting point.

 See [Create and activate custom policies for Security Posture Control](spc-create-policy.md) for more information.

</td></tr><tr><td>

Create a child policy

</td><td>

Create a child policy that inherits the conditions of the current policy. The current policy conditions are displayed in the 'Base policy' field on the new record, and you add more conditions.

</td></tr><tr><td>

Deactivate policy \(Displayed on activated policies only\)

</td><td>

Deactivate an active policy if you don’t want any assets to be monitored or evaluated against that policy. This editing option is only visible on activated policy records.

</td></tr><tr><td>

View findings

</td><td>

Open a new tab and view the matching assets if available. Findings are also referred to CTRs, or test result records for the policy.

</td></tr></tbody>
</table>
