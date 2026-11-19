---
title: Add the Discuss button
description: To use Sidebar, you must add the Discuss button to assets that don't have it automatically installed. You must also add it to custom workspaces where you need to enable Sidebar on an asset. After you add the Discuss button, you can create Sidebar discussions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/sidebar/add-sidebar-button.html
release: zurich
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Add the Discuss button

To use Sidebar, you must add the **Discuss** button to assets that don't have it automatically installed. You must also add it to custom workspaces where you need to enable Sidebar on an asset. After you add the **Discuss** button, you can create Sidebar discussions.

## Before you begin

Role required: admin

## About this task

These workspaces automatically include the **Discuss** button for the specified types, so you don't need to add it:

|Workspace|Button shipped with base system|
|---------|-------------------------------|
|CSM Configurable Workspace|Case, interaction|
|CSM Manager Workspace|Case, interaction|
|FSM Dispatcher Workspace|Task, work order|
|HR Agent Workspace \(Configurable only\)|Case|
|HR Manager Workspace|Case, catalog task, change request, change task, incident, interaction, problem, request item|
|ITSM Manager Workspace|Catalog task, change request, incident, interaction, request, request item|
|Vendor Management Workspace|Change request, CMDB CI outage, core company, service credit|

**Note:** After you add the **Discuss** button, you need to configure the activity stream. For more information, see [Activity stream in Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/activity-stream-sidebar.md).

## Procedure

1.  Navigate to **All** &gt; **UX Form Actions Configs**.

2.  On the UX Actions Configurations screen, select the workspace where you want to add the **Discuss** button.

3.  On the UX Form Actions Layouts screen, select **Name** from the drop-down list and enter `incident` in the search field.\[Omitted image "add-sidebar-name-incident.png"\] Alt text: UX Forms Actions Layouts drop-down list selection

4.  Select the search result that has the name Incident and an Action Config of SOW Actions.

    The UX Form Actions Layout - Incident screen displays.

5.  Check that you’re in the correct application scope.

    For example, use workforce optimization configurable workspace core application for Manager Workspace Actions.

6.  Select the **UX Form Action Layout Items** tab.

7.  Create a new record or edit an existing one:

    -   Create a new record: Create a UX Form Actions Layout record to add a Sidebar discussion button to assets that extend from task and interaction tables.
        1.  Define the name and select the table from the drop-down menu.

            **Note:** The remaining fields are filled in automatically. Sidebar discussions support only tables that extend from the task and interaction tables.

        2.  On the UX Form Actions Layout Item screen, enter this information:

            |Field|Value|
            |-----|-----|
            |Name|Open Collab Chat|
            |Label|Discuss|
            |Action|Open collab chat for Task or Open collab chat for Interaction, depending on the table. For example, the Incident table uses Open collab chat for Task.|
            |Application|Incident Management – Service Operations Workspace|
            |Table|Global|

        3.  If your organization has multiple UX Form Actions Layout items for Sidebar discussions, ensure that you relate the proper items to actions based on the label value.
        4.  Select `Save`.
    -   Edit an existing record.
        1.  Select `Edit`.
        2.  Search for the Discuss label value in the **Collection** field.
        3.  Add it to the UX Form Actions Layout Item list.
        4.  Select `Save`.
        5.  If your organization has multiple UX Form Actions Layout items for Sidebar discussions, ensure that you relate the proper items to actions based on the label value.
8.  In the navigation filter, enter `sys_us_form_action_layout.list`.

9.  Filter for name = Incident and Action Config = SOW.

10. Select the **UX Form - Action Layout Items** tab.

11. Select **New** and fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|Open Collab Chat|
    |Label|Discuss|
    |Action|Open collab chat \(make sure the right action is selected as per your need Either Open collab chat for task or for interaction.\)|
    |Application|Incident Management - Service Operations Workspace|
    |Table|global|

12. Save the UX Form Action Layout item.


## What to do next

To enable Sidebar for non-task tables and add the **Discuss** button to the layout, see [Adding the Discuss button for non-task tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/sidebar/add-sidebar-button-advanced.md).

