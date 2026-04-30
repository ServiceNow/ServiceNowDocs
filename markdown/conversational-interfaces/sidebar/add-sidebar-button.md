---
title: Adding the Discuss button
description: To use Sidebar, you must add the Discuss button to assets that do not have it automatically installed and to custom workspaces where you need to enable Sidebar on an asset. After you add the Discuss button, you can create Sidebar discussions.
locale: en-US
release: yokohama
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Adding the Discuss button

To use Sidebar, you must add the **Discuss** button to assets that do not have it automatically installed and to custom workspaces where you need to enable Sidebar on an asset. After you add the **Discuss** button, you can create Sidebar discussions.

## Before you begin

Role required: admin

## About this task

You do not need to add the **Discuss** button to these workspaces because it is automatically installed for the specified types:

|Workspace|Button shipped with base system|
|---------|-------------------------------|
|CSM Configurable Workspace|Case, interaction|
|CSM Manager Workspace|Case, interaction|
|FSM Dispatcher Workspace|Task, work order|
|HR Agent Workspace \(Configurable only\)|Case|
|HR Manager Workspace|Case, catalog task, change request, change task, incident, interaction, problem, request item|
|ITSM Manager Workspace|Catalog task, change request, incident, interaction, request, request item|
|Vendor Management Workspace|Change request, CMDB CI outage, core company, service credit|

**Note:** After you add the **Discuss** button, you must configure the activity stream. For more information, see [Activity stream in Sidebar](../concept/activity-stream-sidebar.md).

## Procedure

1.  Navigate to **All** &gt; **UX Form Actions Configs**.

2.  On the UX Actions Configurations screen, select the workspace where you want to add the **Discuss** button.

3.  On the UX Form Actions Layouts screen, select **Name** from the drop-down list and enter `incident` in the search field.![UX Forms Actions Layouts drop-down list selection](../image/add-sidebar-name-incident.png)

4.  Select the search result that has the name Incident and an Action Config of SOW Actions.

    The UX Form Actions Layout - Incident screen displays.

5.  Check that you’re in the correct application scope.

    For example, use workforce optimization configurable workspace core application for Manager Workspace Actions.

6.  Select the UX Form Action Layout Items tab.

7.  Create a new record or edit an existing one:

    -   Create a new record - create a new UX Form actions layout record to add a Sidebar discussion button to assets that extend from task and interaction tables.
        1.  Define the name and select the table from the drop-down menu.

            **Note:** The remaining fields should be filled in automatically. Note that Sidebar discussions only support tables that extend from the task and interaction tables.

        2.  On the UX Form Actions Layout Item screen, enter this information:

            |Field|Value|
            |-----|-----|
            |Name|Open Collab Chat|
            |Label|Discuss|
            |Action|Open collab chat \(Make sure the right action is selected as per your need. Either Open collab chat for Task or for Interaction. In this example we are configuring Discuss button on Incident, so we have used Open collab chat action for Task\)|
            |Application|Incident Management – Service Operations Workspace|
            |Table|Global|

        3.  If your organization has multiple UX Form Actions Layout items for Sidebar discussions, ensure that you relate the proper items to actions based on the label value.
        4.  Select `Save`.
    -   Edit an existing record.
        1.  Select `Edit`.
        2.  Search for label value "Discuss" in the Collection field.
        3.  Add it to the UX Form Actions Layout Item list.
        4.  Select `Save`.
        5.  If your organization has multiple UX Form Actions layout Items for Sidebar discussions, ensure that you relate the proper items to actions based on the label value.
8.  In the filter navigation field, enter `sys_us_form_action_layout.list`.

9.  Filter for name = Incident and Action Config = SOW.

10. Select the **UX Form - Action Layout Items** tab.

11. Select **New** to create a new entry and enter the following fields:

    |Field|Value|
    |-----|-----|
    |Name|Open Collab Chat|
    |Label|Discuss|
    |Action|Open collab chat \(make sure the right action is selected as per your need Either Open collab chat for task or for interaction.\)|
    |Application|Incident Management - Service Operations Workspace|
    |Table|global|

12. Save the UX form Action Layout item..


## What to do next

If you want to enable Sidebar for non-task tables and add the Discuss button to the layout, see [Adding the Discuss button for non-task tables](add-sidebar-button-advanced.md).

