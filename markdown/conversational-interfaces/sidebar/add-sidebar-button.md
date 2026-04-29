---
title: Adding the Discuss button
description: To use Sidebar, you must add the Discuss button to assets that do not have it automatically installed and to custom workspaces where you must enable Sidebar on an asset. After you add the Discuss button, you can create Sidebar discussions.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Adding the Discuss button

To use Sidebar, you must add the **Discuss** button to assets that do not have it automatically installed and to custom workspaces where you must enable Sidebar on an asset. After you add the **Discuss** button, you can create Sidebar discussions.

## Before you begin

Role required: admin

## About this task

You don’t need to add the **Discuss** button to these workspaces because it’s automatically installed for the specified types:

|Workspace|Button shipped with base system|
|---------|-------------------------------|
|CSM Configurable Workspace|Case, interaction|
|CSM Manager Workspace|Case, interaction|
|FSM Dispatcher Workspace|Task or work order|
|HR Agent Workspace \(Configurable only\)|Case|
|HR Manager Workspace|Case, catalog task, change request, change task, incident, interaction, problem, request item|
|ITSM Manager Workspace|Catalog task, change request, incident, interaction, request, request item|
|Vendor Management Workspace|Change request, CMDB CI outage, core company, service credit|

## Procedure

1.  Identify the table that you want to configure the Discuss button for.

2.  Determine whether the table extends the task.

    If the table extends the task, then continue. If the table does not extend the task, then see the KB article.

3.  From the home screen, select the workspace you want to use.

    ![](../image/add-discuss-workspace-select.png)

4.  Change the application scope so it matches the workspace.

    ![](../image/add-discuss-scope-select.png)

5.  In the navigation filter, enter `sys_ux_form_action_layout_list.do` so the UX Form Actions Layouts screen appears.

    ![](../image/add-discuss-ux-forms-screen.png)

6.  On the UX Forms Action Layouts screen, select **New**.

    ![](../image/add-discuss-new-action-layouts.png)

7.  On the UX Forms Actions Layout New record screen, fill out the fields.

    -   Name
    -   Description
    -   Application - this defaults to the workspace you selected.
    -   Table - from the drop-down list, select **Task**.
    -   Action Config - select the workspace.
    -   Active - this checkbox should be selected.
    ![UX Forms Actions Layout New record screen.](../image/add-discuss-new-action-layouts-filled.png)

8.  Select **Submit**.

9.  On the UX Form Actions Layouts screen, select the record that you created.

    ![](../image/add-discuss-select-layout.png)

10. On the UX Forms Action Layout screen, from the UX Form Action Layout Items tab, select **Edit**.

    ![](../image/add-discuss-task-layout.png)

    If the Edit button does not appear, check that admin is the same scope as the UX Form Actions layout record.

11. On the Edit Members screen, select **Discuss** from the Collection column.

    ![](../image/add-discuss-edit-members.png)

12. Select the right-pointing arrow \(![](../image/add-discuss-right-arrow.png)\) to move **Discuss** to the Task layout column.

13. Select **Save**.


## What to do next

If you want to enable Sidebar for non-task tables and add the Discuss button to the layout, see [Adding the Discuss button for non-task tables](add-sidebar-button-advanced.md).

After you add the **Discuss** button, you must configure the activity stream. For more information, see [Activity stream in Sidebar](../concept/activity-stream-sidebar.md).

