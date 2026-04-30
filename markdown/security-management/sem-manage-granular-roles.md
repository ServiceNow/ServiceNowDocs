---
title: Manage persona and granular roles for Vulnerability Response
description: After you complete your initial assignment of persona roles using Setup Assistant, manage additional granular role assignments to users or groups from the User Administration module in your instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Assign the Vulnerability Response persona roles using Setup Assistant, Security Exposure Management Workspace personas and granular roles, Implement, Unified Security Exposure Management, Security Operations]
---

# Manage persona and granular roles for Vulnerability Response

After you complete your initial assignment of persona roles using Setup Assistant, manage additional granular role assignments to users or groups from the User Administration module in your instance.

## Before you begin

If you have not already completed your initial set up and configuration for Vulnerability Response using Setup Assistant, or assigned persona roles to users and groups, navigate to **Vulnerability Response** &gt; **Administration** &gt; **Setup Assistant**. See [Assign the Vulnerability Response persona roles using Setup Assistant](../../vulnerability-response/task/vr-assign-personas_SA.md).

For key terms and an overview of persona roles, see [Vulnerability Response personas and granular roles](../../vulnerability-response/concept/vr-persona-overview.md#).

A persona role is pre-configured role in the application that is made up of multiple granular roles. The persona roles in Setup Assistant, Vulnerability Admin, Vulnerability Analyst, Remediation Owner, Configuration Item Manager, and Exception Manager, are designed to correspond to common job titles for managers, analysts, and service owners in an IT organization or vulnerability remediation group.

If you want your users and groups to have more access than one of the roles permits, you can add more granular roles to users and groups. Conversely, if you want to limit access for specific users and groups at the task level, you can remove granular roles. Also, you can build custom roles to suit your needs.

Role required: admin

## Procedure

1.  To manage granular roles for users and groups, choose one to continue.

<table id="choicetable_m51_vw5_tlb"><thead><tr><th align="left" id="d44858e111">

Option

</th><th align="left" id="d44858e114">

Description

</th></tr></thead><tbody><tr><td id="d44858e120">

**Edit the granular roles for a user or group**

</td><td>

Assign or remove granular roles for users or groups, or edit granular roles so that only select users within a group have expanded or limited permissions.An example follows the table.

</td></tr><tr><td id="d44858e132">

**Create a new role**

</td><td>

Create a new role using one or more granular roles from the library for a specific job title, or to fulfill a specific requirement.An example follows the table.

</td></tr></tbody>
</table>    The names for the granular roles in Vulnerability Response usually describe what users can do and see. To view descriptions of specific granular roles, navigate to **All** &gt; **User Administration** &gt; **Roles** and locate the role that you want. Role description, roles that are automatically inherited when a role is assigned, and any roles that depend on other roles are also listed.

2.  To assign or remove a granular role for a user or a group, follow these steps.

    As an example, assume you want to assign an IT manager with a role that permits this manager to view records but not update or edit them. To view records in Vulnerability Response, Performance Analytics for Vulnerability Response, and for all third party integrations, you assign this user with the sn\_vul.read\_all granular role.

    1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

    2.  Locate the user, and, in the Name column, click the record to open it.

        The user's record is displayed.

    3.  If not selected, select the Roles tab.

        The roles currently assigned to the user are displayed.

    4.  Click **Edit**.

        The Edit members form is displayed.

    5.  In the Collection field of the slushbucket, enter the name of the role if you know it, or, enter `*sn_vul` to view only the granular roles available for Vulnerability Response.

    6.  Locate and move sn\_vul.read\_all to the Roles List.

        **Note:** Use the same process to remove specific granular roles from users in the slushbucket by moving the role from the Roles list to the Collection list.

    7.  Click **Save**.

        The user record is displayed with the new granular role.

    8.  Click **Update** to save your changes and return to the Users list.

        You have provided a user with permission to read but not update records in Vulnerability Response, Performance Analytics for Vulnerability Response, and for third party integrations.

3.  To edit a group so that only specific members have expanded access with more granular roles, follow these steps.

    As example, assume you want to permit certain users in the Remediation Owner \(sn\_vul.remediation\_owner\) group to create vulnerable items manually, but you don't want to expand that permission to all users in the group. The permission to create vulnerable items manually is granted by the sn\_vul.create\_vulnerable\_items granular role. To grant this permission to only select users from this group, follow these steps.

    1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

    2.  Locate the Remediation Owner group, and, in the Name column, click the group to open the record.

        The group record is displayed.

    3.  If not selected, select the Group Members tab.

        The current members of the group are displayed.

    4.  Click a name from the list you want to assign the granular role to and open the record.

    5.  On the record, scroll to the Roles tab and select it.

        The roles assigned to the user are displayed.

    6.  Click **Edit**.

        The Edit members form is displayed.

    7.  In the Collection field, enter the name of the role if you know it, or, enter `*sn_vul` to view all the granular roles available for Vulnerability Response.

    8.  Locate and move sn\_vul.create\_vulnerable\_items to the Roles List.

        ![Moving the sn_vul.create_vulnerable_items role from the Collection list to the Roles List.](../../vulnerability-response/image/vr-persona-new-role-1.png)

    9.  Click **Save**.

        The user record is displayed with the new granular role.

    10. Click the back arrow to return to view the users in the record for the Remediation Owner group

    11. Click names from the list you want to assign this granular role to, open their records, and use the slushbucket to assign the role.

    12. After you complete your edits, Click **Update** to save your changes and return to the groups list.

        You have provided some users in the Remediation Owner \(sn\_vul.remediation\_owner\) group permission to create vulnerable items manually.

4.  To create a new role using only granular roles you select, follow these steps.

    For this example, assume you want to create role for a compliance auditor. This role works closely with Governance, Risk, and Compliance \(GRC\), and the job requires the following permissions and tasks within Vulnerability Response:

    -   Manages remediation deadlines for vulnerable items and vulnerability groups
    -   Approves exception requests for extending deadlines or deferring remediation
    -   Manages the clean up of older vulnerable items with auto-delete
    -   Define risk scores
    -   Reads all records in Vulnerability Response but is not permitted to edit them.
    1.  Navigate to **All** &gt; **User Administration** &gt; **Roles**.

    2.  In the Roles list, click **New**.

    3.  In the Role record, fill out the fields.

        Create a name, select the application that contains this record, and enter a short description for your new role. For more information about the other fields on the form, see [Create a role](https://www.servicenow.com/docs/access?context=t_CreateARole&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

        **Note:** When creating a name for your new role, you may prefer to use a name that is easily recognized in the roles list and describes the functionality of the role. For this example, you may prefer a title such as, Compliance Auditor - GRC-VR.

    4.  Click **Submit**.

        The Roles list is displayed.

    5.  Locate your new role and click it to open the record.

    6.  Click **Edit**.

        The Edit Members form is displayed.

    7.  Use the slushbucket to add granular roles to your new role.

        For this example, the required roles for this new role are displayed in the right column in the following figure.

        To display only the granular roles for Vulnerability Response, in the Collection field, enter `*sn_vul`.

        ![Moving the granular roles for a new role from the Collection list to the Contains Roles List.](../../vulnerability-response/image/vr-persona-new-role.png)

    8.  Click **Save**.

        The record for your new role is displayed. Starting with the Contains Roles tab, continue editing the role as required.

    9.  Click **Update** to save your changes.

        Your new role is displayed on the Roles list.


