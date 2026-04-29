---
title: Assign the Vulnerability Response persona roles using Setup Assistant
description: Assign the Vulnerability Response persona roles to groups or users with Setup Assistant.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Security Exposure Management Workspace personas and granular roles, Implement, Unified Security Exposure Management, Security Operations]
---

# Assign the Vulnerability Response persona roles using Setup Assistant

Assign the Vulnerability Response persona roles to groups or users with Setup Assistant.

## Before you begin

If you have already assigned persona roles in Vulnerability Response using Setup Assistant and you want more information about editing and managing your granular roles and role assignments in the User Administration module, see [Manage persona and granular roles for Vulnerability Response](../../vulnerability-response/task/vr_manage_granular-roles.md).

If you are an upgrade customer, you can continue using your existing roles for the Vulnerability Response application. Access for users and groups assigned with the sn\_vul.vulnerability\_read and sn\_vul.vulnerability\_write permissions and remediation owner roles available in previous versions of Vulnerability Response has not changed.

However, for more control over what users and groups can do and see in the Vulnerability Response application at the task level, you may prefer using persona and granular roles.

If you have not already assigned the sn\_vul.vulnerability\_admin persona role using Setup Assistant, follow the steps below to assign it. Once assigned, the vulnerability administrator with this persona role has permission to complete the Setup Assistant tasks after the first section, and manage rules and third-party integrations in the Vulnerability Response application.

For an overview about persona roles and granular roles, see [Vulnerability Response personas and granular roles](../../vulnerability-response/concept/vr-persona-overview.md#).

If you are an upgrade customer, use the following table as a reference.

<table id="table_z5k_bwb_glb"><thead><tr><th>

Prior to v10.3

</th><th>

Starting with v10.3

</th></tr></thead><tbody><tr><td>

If you assigned sn\_vul.admin

</td><td>

You may prefer to assign sn\_vul.vulnerability\_admin - Vulnerability Admin to users or groups.Users with this role have complete access to the Vulnerability Response \(VR\) application and its records. Users with this role configure all VR applications and rules and install third-party integrations.

</td></tr><tr><td>

If you assigned sn\_vulnerability\_write for users and groups.

</td><td>

You may prefer to assign sn\_vul.vulnerability\_analyst - Vulnerability Analyst to users and groups. Users and groups with this role view and update all records for VI remediation.

</td></tr><tr><td>

If you assigned sn\_vul.remediation\_owner

</td><td>

You may prefer to assign sn\_vul.remediation\_owner - Remediation Owner to users and groups.Users and groups with this role remediate vulnerabilities assigned to them or to a group they belong to. Groups or users with this role view and update the records assigned to them or to a group they belong to.

</td></tr><tr><td>

If you assigned sn\_vul.admin for management of unmatched configuration items \(CI\)s

</td><td>

You may prefer to assign sn\_vul.ci- CI Manager to users and groups.Users and groups with this role manage unmatched configuration items \(CIs\) not found in the Configuration Management Database \(CMDB\). Groups or users with this role update discovered items.

</td></tr><tr><td>

If you assigned sn\_vul.admin for deferrals and exception approvals.

</td><td>

You may prefer to assign sn\_vul.exception\_approver - Exception Approver to users and groups.Users and groups with this role approve exceptions, deferrals, and closures of remediation tasks and vulnerable items.

Starting from v20.0, the granular role, sn\_vul.read\_all, has been removed for this role so that you can access the vulnerable items and remediation tasks assigned to you and your group instead of all the vulnerable items and remediation tasks.

</td></tr><tr><td>

If you assigned sn\_vul.vulnerability\_read to provide visibility into vulnerability management.

</td><td>

You may prefer to assign read access to specific areas in the application by task. For example, assign sn\_vul.read\_all so a user can view all VR records. For read access to view remediation task rules, assign sn\_vul.read\_group\_rules. Users and groups with this role do not update records.

</td></tr></tbody>
</table>To view the granular roles a user or groups with a persona role inherits by default, navigate to **All** &gt; **User Administration** &gt; **Roles**. Locate the role you want, and click it to open the record. The Contains Roles tab lists all the granular roles of the persona role as well as any inherited roles.

You may prefer to verify that you have all your required users and groups created before you assign roles in Setup Assistant. Alternatively, to add new users and groups from inside Setup Assistant, click the **User Administration module** link in the form shown in the following figure.

For the following example, to limit access to the Vulnerability Response application, this example shows how to assign a user with the vulnerability admin persona. Usually, you may prefer to assign persona roles other than sn\_vul.vulnerability\_admin to groups.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **Administration** **Setup Assistant**.

    The Setup Assistant page is displayed.

2.  Click Vulnerability Response User and Groups.

    The System Administration Vulnerability Response Users and Groups page is displayed.

    ![System Administration Vulnerability Response Users and Groups page with no personas assigned.](../../vulnerability-response/image/vr-setup-persona-1.png)

3.  With Assign roles to a user selected, choose an existing user from the list.

    You can only assign a user or a group with one persona role.

    On the right of the form, after you select a user or group, the default persona, Remediation owner \[sn\_vul.remediation\_owner\] is assigned by default and remains displayed in the list until you change it.

    **Note:** If you are upgrading to a newer version of Vulnerability Response and you previously assigned the sn\_vul.vulnerability\_read or sn\_vul.vulnerability\_write role to a user or group prior to the upgrade, it is displayed along with the new persona roles, as shown in the following figure.

    If you are an upgrade customer, you can keep using your existing roles for the Vulnerability Response application. Access for users and groups assigned with the sn\_vul.vulnerability\_read and sn\_vul.vulnerability\_write permissions and remediation owner prior to v10.3 has not changed.

    Note that for existing users or a groups currently assigned with the sn\_vul.vulnerability\_read or sn\_vul.vulnerability\_write roles, these roles are displayed along with the persona roles in the list. Once you assign a persona role, the old role is no longer available going forward. For example, as shown in following figure, the Write \[sn\_vul.vulnerability\_write\] role is no longer displayed as an option for this user or group after it is assigned one of the persona roles.

    ![List of available roles prior to version 10.3.](../../vulnerability-response/image/vr_roles_prev11..png)

4.  From the list on the right of the form, select **Vulnerability Admin \[sn\_vul.vulnerability\_admin\]**.

    A message is displayed that indicates the user or group is successfully assigned with the persona.

    ![User assigned vulnerability admin persona.](../../vulnerability-response/image/vr-setup-persona-2.png "Remediation Owner persona assigned to a group, and Vulnerability admin persona assigned to a user")

5.  Using the descriptions of the persona roles listed above, continue to assign any users and groups to the remaining persona roles: Remediation Owner, Vulnerability Analyst, CI Manager, and Exception Approver.

    You have successfully completed assigning persona roles to users and groups using Setup Assistant.

6.  To edit the users in a group from Setup Assistant, follow these steps.

    1.  With the group displayed on the form, click the name of the group you want to edit.

        The Group record is displayed.

    2.  With the Group Members tab selected, click **Edit**.

        The Edit Members form is displayed

    3.  Use the slushbucket to select or remove users.

    4.  Click **Save** to save your changes and return to the Group record.

    5.  Click **Update** to return to Setup Assistant.

    6.  On the Setup Assistant page, click **Vulnerability Response Users and Groups** to continue with your configuration in Setup Assistant.


## What to do next

As system admin, continue with the configuration of Vulnerability Response in Setup Assistant. Note that after the first section is completed, you can have a user you assigned with the vulnerability admin persona role complete the tasks in Setup Assistant. For more information about managing granular roles and examples, see [Manage persona and granular roles for Vulnerability Response](../../vulnerability-response/task/vr_manage_granular-roles.md).

