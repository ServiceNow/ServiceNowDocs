---
title: Manage Scripting Governance Tool
description: Enable or disable the Scripting Governance Tool on your instance by running the appropriate script. Only users with the security\_admin role can run these scripts and modify the associated properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/manage-sgt.html
release: zurich
product: Access Control
classification: access-control
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 2
keywords: [Scripting Governance Tool, SGT, scripting, Conditional Script Writer]
breadcrumb: [Scripting Governance Tool, Access Management]
---

# Manage Scripting Governance Tool

Enable or disable the Scripting Governance Tool on your instance by running the appropriate script. Only users with the `security_admin` role can run these scripts and modify the associated properties.

## Scripting Governance Tool states

Scripting Governance Tool operates in one of two states. The active state determines whether scripting governance policies are enforced and whether users are provisioned to the Conditional Script Writer group.

**Note:**

-   Scripting Governance Tool is enabled by default. You can choose to disable.
-   You must elevate your role to `security_admin` to enable or disable Scripting Governance Tool.

<table id="table_chd_vxm_djc"><thead><tr><th>

States

</th><th>

Behavior of Scripting Governance Tool

</th></tr></thead><tbody><tr><td>

Enabled

</td><td>

-   Scripting Governance Tool and all associated ACLs are active on the instance.
-   Users are evaluated against scripting access rules and assigned to the appropriate script writer groups.
-   The `security_admin` can run scans to identify users with scripting access and manage group membership.
-   Scripting governance policies are enforced across all applicable records and transactions.
-   Audit logs and visibility into scripting access are available to the security admin.

</td></tr><tr><td>

Disabled

</td><td>

-   Scripting Governance Tool and all associated ACLs are deactivated on the instance.
-   No scripting governance policies are enforced. Users are not evaluated or assigned to script writer groups.
-   Existing group memberships from a prior enabled state are preserved but have no enforcement effect.
-   The Scripting Governance Tool interface remains accessible to the security admin but scanning and access management actions are inactive.
-   Scripting Governance Tool can be re-enabled by the `security_admin` at any time without data loss.

</td></tr></tbody>
</table>## Disable scripting governance

To disable Scripting Governance, navigate **All** &gt; **Scheduled Script Executions** \(`sysauto_script_list.do`\) and run the **Disable Scripting Governance** script to deactivate Scripting Governance Tool on your instance.

Running this script performs the following actions:

-   Disables the `glide.security.scripting_role.provisioning_job_running` property.
-   Disables the `glide.security.scripting_role.auto_provisioning` property.
-   Disables the `glide.security.scripting_governance.enabled` property.
-   Disables the **Add Users** to **Conditional Script Writer Group** and **Update Users** in **Conditional Script Writer Group** scheduled jobs.
-   Removes all users from the **Conditional Script Writer Group** through a scheduled job.

## Enable scripting governance

To enable Scripting Governance, navigate **All** &gt; **Scheduled Script Executions** \(`sysauto_script_list.do`\) and execute the **Enable Scripting Governance** script to activate Scripting Governance Tool on your instance.

Running this script performs the following actions:

-   Enables the `glide.security.scripting_role.provisioning_job_running` property.
-   Enables the `glide.security.scripting_governance.enabled` property.
-   Enables the **Add Users** to **Conditional Script Writer Group** and **Update Users** in **Conditional Script Writer Group** scheduled jobs.
-   Schedules the **Add Users** to **Conditional Script Writer Group** job to run.

