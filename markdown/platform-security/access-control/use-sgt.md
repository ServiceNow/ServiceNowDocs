---
title: Use SGT
description: Use the Scripting Governance Tool \(SGT\) to provide a single, centralised control for managing scripting access across your ServiceNow AI Platform.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 2
keywords: [Scripting Governance Tool, SGT, scripting, Conditional Script Writer]
breadcrumb: [Scripting Governance Tool, Access Management]
---

# Use SGT

Use the Scripting Governance Tool \(SGT\) to provide a single, centralised control for managing scripting access across your ServiceNow AI Platform.

## Before you begin

Role required: security\_admin

**Important:** You must have elevate your role `security_admin`. See [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md).

The **Scripting Governance Tool** helps you review user scripting governance your ServiceNow AI Platform. The **Conditional Script Writer** group grants scripting permissions to its members via the `snc_required_script_writer_permission` role. Users are added to the group by either an automated assignment or manual configuration. You can manage both of these settings from the **Scripting Governance Tool**.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Scripting Governance Tool**.

2.  Use the following features to learn more:

<table id="table_j3q_mjm_w3c"><thead><tr><th>

Features

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Users in Conditional Script Writer Group

</td><td>

Displays the number of users in the **Conditional Script Writer** group. These users are granted the `snc_required_script_writer_permission` until removed from the group.

</td></tr><tr><td>

Auto-assignment

</td><td>

Auto-assignment assigns new users to the **Conditional Script Writer** group if the users are `internal users` and has one functional role. You can select the slider to de-activate.**Note:** It is recommended to de-activate auto-assignment.

</td></tr><tr><td>

Scan for users who have scripted \(Recommended\)

</td><td>

Scans for users in the ServiceNow AI Platform who have modified records containing script fields such as business rules, script includes, or client scripts. When running the scan, you can define a time period for which the scan checks.

</td></tr><tr><td>

Manual Configuration

</td><td>

You can manually select users that stay in the **Conditional Script Writer** group. Select the **Manage scripting access** button and enter the users into the text field for manually managing the user removal process from the **Conditional Script Writer** group.

</td></tr><tr><td>

Groups containing a scripting role

</td><td>

Displays the number of groups that contain a scripting role. By default the **Conditional Script Writer** group has a scripting role.**Note:** It is recommended to manage scripting access exclusively through the **Conditional Script Writer** group. Adding the `snc_required_script_writer_permission` role as a child role to other roles or groups reduces your ability to centrally control who can script on your instance.

</td></tr><tr><td>

Roles containing a scripting role

</td><td>

Displays the number of roles that contain a `snc_required_script_writer_permission` role.**Note:** It is recommended to manage scripting access exclusively through the **Conditional Script Writer** group. Adding the `snc_required_script_writer_permission` role as a child role to other roles or groups reduces your ability to centrally control who can script on your instance.

</td></tr><tr><td>

View scans

</td><td>

After you run the scan, the details of the scan are displayed on the View scans.

</td></tr><tr><td>

View removals

</td><td>

When you schedule for removal of user from the **Conditional Script Writer** group, the details are displayed on the View removals.

</td></tr></tbody>
</table>    ![Scripting Governance Tool dashboard](../image/scripting-governance-dashboard.png)


## Result

You can view the following topics to understand how you can:

-   [Scan for users who have scripted](scan-for-users-who-have-scripted.md)
-   [Remove users from the Conditional Script Writer group](remove-conditional-script-writer-users.md)

