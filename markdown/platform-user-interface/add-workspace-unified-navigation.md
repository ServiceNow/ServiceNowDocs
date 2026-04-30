---
title: Add a workspace to the Unified Navigation Workspaces menu
description: Configure the Unified Navigation to display a workspace in the Workspaces menu.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Add a workspace to the Unified Navigation Workspaces menu

Configure the Unified Navigation to display a workspace in the Workspaces menu.

## Before you begin

Role required: admin

## About this task

The available workspace displays in the Unified Navigation when you have access to at least one workspace. Multiple workspaces display in the Workspaces menu when you have access to more than one workspace.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  Select the application that you want to add to the Workspaces menu on the Unified Navigation.

3.  In related lists, select the **UX Application Category M2Ms** tab.

    ![UX Application Category M2Ms tab.](../image/ux-application-category-tab.png)

4.  Select **New** in the UX Application Category M2Ms list.

    **Note:** The **New** button only displays if you have access to the selected application.

5.  Select **Workspace** in the Experience Category column.

6.  On the form, fill in the fields.

<table id="table_th5_g5n_trb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Experience Category

</td><td>

Category of the experience added to the Unified Navigation. Select **Workspace**.

</td></tr><tr><td>

Application

</td><td>

Application that the experience applies to. Global is the default application and applies across the organization.

</td></tr><tr><td>

UX Application

</td><td>

UX application that you want to add to the **Workspaces** menu. Select the Workspace you want to display in the Workspaces menu.

</td></tr><tr><td>

Order

</td><td>

Order in which the Workspace you select is displayed in the Workspaces menu.**Note:** This option is enabled once the **glide.ui.next\_experience.workspace\_sorting** system property has been created. For more information, see [Set the order of your workspaces in the Unified Navigation Workspaces menu](set-order-workspace-unified-navigation.md).

</td></tr></tbody>
</table>7.  Select **Submit**.

8.  Refresh your browser to access the new workspace from the Workspaces menu.


**Parent Topic:**[Configuring the Next Experience UI](../concept/next-experience-ui-admin.md)

