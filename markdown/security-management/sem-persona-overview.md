---
title: Security Exposure Management Workspace personas and granular roles
description: Before you can successfully remediate vulnerabilities with the Security Exposure Management Workspace plugin, you must assign personas and roles to your users and groups in Setup Assistant.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Security Exposure Management Workspace personas and granular roles

Before you can successfully remediate vulnerabilities with the Security Exposure Management Workspace plugin, you must assign personas and roles to your users and groups in Setup Assistant.

One of the first configuration steps required for the Security Exposure Management Workspace plugin is to assign roles to users and groups. Roles define what users and groups can see and do in Security Exposure Management Workspace, Performance Analytics for Vulnerability Response, and all third party integrations with Security Exposure Management Workspace.

You assign persona roles to existing users and groups in Setup Assistant. See [Assign the Vulnerability Response persona roles using Setup Assistant](../task/sem-assign-personas_SA.md).

**Note:**

If you are an upgrade customer, you can continue using your existing roles for the Vulnerability Response application. Access for users and groups assigned with the sn\_vul.vulnerability\_read and sn\_vul.vulnerability\_write permissions and remediation owner prior to v10.3 has not changed.

However, for more control over what users and groups can do and see in the Security Exposure Management Workspace plugin at the task level, you may prefer using granular roles. For more information, see [Manage persona and granular roles for Vulnerability Response](../task/sem-manage-granular-roles.md).

If you have already assigned roles using Setup Assistant and you want to manage granular role assignments for all users and groups from the User Administration module, see [Manage persona and granular roles for Vulnerability Response](../task/sem-manage-granular-roles.md) for more information.

## Persona roles and granular roles starting

Key terms.

-   **Role**

    Roles define what users and groups can see and do in the Security Exposure Management Workspace plugin.

-   **Group**

    A set of users who share certain roles and a common purpose.

-   **Persona role**

    A pre-configured role in the application that is made up of multiple granular roles. The persona roles in Setup Assistant, Vulnerability Admin, Vulnerability Analyst, Remediation Owner, Configuration Item Manager, and Exception Manager, are designed to correspond to common job titles for managers, analysts, and service owners in an IT organization or vulnerability remediation group.

-   **Inherited roles**

    A term that describes roles that users automatically acquire when they are assigned other roles. For example, any users or groups assigned with the sn\_vul.remediation\_owner persona role also inherit the sn\_vul.read\_assigned,sn\_vul.write\_assigned granular roles.

-   **Access control list \(ACL\)**

    Access control lists restrict access to data by requiring users to pass a set of requirements before they can interact with it.

    Starting from Vulnerability Response v16.5, to protect reports from being exposed, set the **All report\_view ACLs** as **active=true**. This ACL ensures that the protected data is only available to authorized users.


You assign groups and users to persona roles in Setup Assistant.

**Note:** In Setup Assistant, the system admin role \(admin\) is required for the tasks in the first section, assigning roles and installing integrations. After you assign persona roles in Setup Assistant and install integrations, you may prefer to assign a user or group with the sn\_vul.vulnerability\_admin role to finish any remaining tasks in Setup Assistant and to manage the Vulnerability Response application.

The following table lists Vulnerability Response persona roles installed with the application.

<table id="table_z5k_bwb_glb"><thead><tr><th>

Persona roles for Vulnerability Response

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assign sn\_vul.vulnerability\_admin - Vulnerability Admin to users or groups.

</td><td>

Users with this role have complete access to the Vulnerability Response \(VR\) application and its records. Users with this role configure all VR applications and rules and install third party integrations.

</td></tr><tr><td>

Assign sn\_vul.vulnerability\_analyst - Vulnerability Analyst to users and groups.

</td><td>

Users and groups with this role view and update all records for VI remediation.

</td></tr><tr><td>

Assign sn\_vul.remediation\_owner - Remediation Owner to users and groups.

</td><td>

Users and groups with this role remediate vulnerabilities assigned to them or to a group they belong to. Groups or users with this role view and update the records assigned to them or to a group they belong to.

</td></tr><tr><td>

Assign sn\_vul.ci\_manager to users and groups.

</td><td>

Users and groups with this role manage reclassification of unmatched configuration items \(CIs\) that are not found in the Configuration Management Database \(CMDB\).

</td></tr><tr><td>

Assign read access to specific areas in the application by task.

</td><td>

For example, assign sn\_vul.read\_all so a user can view all VR records. For read access to view remediation task rules, assign sn\_vul.read\_group\_rules. Users and groups with this role do not update records.

</td></tr></tbody>
</table>## Granular roles and persona roles

One way to think about persona roles is to consider how their descriptions may relate to job descriptions for various IT or vulnerability remediation positions in your organization. The following figure illustrates a possible job description for a remediation specialist in IT, and how the tasks associated with this job relate to the tasks of a remediation owner persona role in the Vulnerability Response application.

![Jobs in company compared to personas in Vulnerability Response.](../../vulnerability-response/image/job-tasks-personas.png "Job descriptions and a persona role")

Both the job description and the remediation owner persona role could be defined as a series of remediation tasks. In the preceding image, a job description and a persona role in green blocks sit atop the tasks that describe them. In this example, some of the typical job requirements for a specialist in a remediation group correspond directly to the tasks that make up the remediation owner persona in Vulnerability Response: Review and update records, track the remediation status of vulnerabilities, prioritize items for remediation, and apply fixes and patches with IT.

Sometimes, however, the jobs in your organization may not directly correspond to the tasks that make up one of the five persona roles in the Vulnerability Response application. For various reasons, such as protecting sensitive data, or complying with regulations, you must limit the broad access some of the persona roles provide to your users and groups. Or, conversely, you are required to provide users and groups with more access so they can perform their jobs. Using granular roles, you can easily customize roles and control the access users and groups have to Vulnerability Response, Performance Analytics for Vulnerability Response, and third party integrations.

## The granular roles define the tasks

The names for the granular roles in Vulnerability Response usually describe what users can do and see in the Vulnerability Response application. For example, in the previous image, users and groups with the Remediation owner persona assigned have the sn\_vul.read\_assigned and sn\_vul.write\_assigned granular roles. These granular roles permit users or groups to view and update vulnerable items and remediation task records that are assigned to them. To view descriptions of specific granular roles, as a user with the system admin role, navigate to **User Administration** &gt; **Roles** and locate the role that you want. Roles that are automatically inherited when a role is assigned are listed. Also, when a role depends on other role assignments, any required roles are also listed.

In the following image, the granular roles of both the remediation owner persona role and the vulnerability analyst persona are illustrated. Note that the remediation owner persona does not include the read\_all and write\_all permissions of the vulnerability analyst persona. The granular roles, read\_all and write\_all, are required before users and groups can read and edit all of the vulnerable item and remediation task records. To customize these roles, simply add or remove granular roles to expand or limit access.

![The granular roles you can add or remove for the remediation owner and vulnerability analyst personas. For example, the read all and write all roles for the vulnerability analyst.](../../vulnerability-response/image/vr-Persona.png "Granular roles and the remediation owner and vulnerability analyst personas")

If you want your users and groups to have more access than the persona roles permit, you can add more granular roles to users and groups. Conversely, if you want to limit access for specific users and groups at the task level, you can remove granular roles.

**Note:** To assign and edit granular roles in the User Administration module, the system admin role is required.

## Granular roles in the User Administration module

For an example of how to manage granular roles for a user or group, see [Manage persona and granular roles for Vulnerability Response](../../vulnerability-response/task/vr_manage_granular-roles.md).

To assign persona roles, see [Assign the Vulnerability Response persona roles using Setup Assistant](../../vulnerability-response/task/vr-assign-personas_SA.md).

