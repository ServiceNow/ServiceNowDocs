---
title: Change scope to Service Portfolio Management Premium
description: Grant access to a dedicated user to enable switching the scope from Global to Service Portfolio Management Premium to create a custom automated indicator.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Change scope to Service Portfolio Management Premium

Grant access to a dedicated user to enable switching the scope from Global to Service Portfolio Management Premium to create a custom automated indicator.

## Before you begin

Role required: admin

## About this task

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](../concept/SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Set up Service Owner Workspace](../image/SOWSetupBanner2.png "Navigate")

</td></tr></tbody>
</table>Both the indicator and the job must be in the same scope. Provide a user with delegated developer access and the pa\_admin role to change the scope from Global to Service Portfolio Management Premium when creating custom indicators for Service Portfolio Management Premium jobs.

![Assign access to change scope](../image/SOW_assignaccess.gif)

## Procedure

1.  In the Navigator, type `sys_scope.list` and press Enter.

    The Applications list appears.

2.  Search by name for Service Portfolio Management Premium and click the application name to open the associated Store Application form.

3.  In Related Links, click **Manage Developers**.

4.  Search for the user or group you want to grant delegated developer access to.

    The **Permissions** configuration screen appears.

5.  Configure delegated developer access for the user or group.

    1.  In the **File Type Access** section, toggle the **Reporting** category radio button to grant this type of access.

    2.  Click **Save**.

    Grant access to any other section category by toggling the associated radio button.

6.  Assign the pa\_admin role to the user or group with delegated developer access.


