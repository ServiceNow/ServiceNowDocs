---
title: Configure offline mode properties for action functions
description: Determine which fields and functions are available to users when working in offline mode.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure offline mode properties for action functions

Determine which fields and functions are available to users when working in offline mode.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** from the menu.

4.  Either select **New** or an existing record.

5.  In the **Properties** area, select **Available offline**.

    The Offline settings area displays further down the page.

6.  Select the **Choose** button on any of the following fields to determine which fields and functions are available to users when working in offline mode.

<table id="table_o1n_3jc_nvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide fields

</td><td>

Use this field to determine which fields are not available after the user performs an action in offline mode. For example, after a user assigns a task to themselves, you could hide the **Assigned to** field.

</td></tr><tr><td>

Show fields

</td><td>

Use this field to determine which fields are available after the user performs an action in offline mode. For example, after a user assigns a task to themselves, you could show the **Work notes** field.

</td></tr><tr><td>

Hide functions

</td><td>

Use this field to determine which functions are not available after the user performs an action in offline mode. For example, after a user taps the Start Work function in offline mode that action function is hidden.Use the **Select target record** field to select the functions you want to hide.

</td></tr><tr><td>

Show functions

</td><td>

Use this field to determine which functions are available after the user performs an action in offline mode. For example, after a user taps the Start Work function in offline mode, the Close Incomplete function displays instead.Use the **Select target record** field to select the functions you want to show.

</td></tr><tr><td>

Disable after online edit

</td><td>

Use this field to define sections to gray out when a user performs an action.In offline mode, an indicator appears next to a record after a user makes a change. Setting a screen marked as "Disable after online edit" mimics the online behavior, where a record is grayed out in the list after a user makes a change.

 Use the **Select target record** field to select the screens that you want to gray out.

 ![Mobile screen shot showing a record in a list that has been grayed out.](../image/OnlineZombieMode.png "Online behavior in "Disable after online edit" mode")

</td></tr></tbody>
</table>7.  Select **Save**.


-   **[Display and hide buttons in offline mode](buttons-offline.md)**  
Define whether to show or hide buttons while users are in offline mode on their Mobile Agent app.
-   **[Trigger offline cache download](trigger-offline-cache-download.md)**  
**Trigger offline cache download** is an optional button attribute \(**sys\_sg\_button\_atribute\_name**\) that will generate an offline cache after a successful completion of the assigned writeback action.

**Parent Topic:**[Offline mode](../concept/mobile-offline-mode.md)

