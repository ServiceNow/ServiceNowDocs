---
title: Configure offline mode properties for action functions
description: Determine which fields and functions are available to users when working in offline mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/config-offline-properties-action-funct.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Supported functions, Align apps, screens, and functions, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure offline mode properties for action functions

Determine which fields and functions are available to users when working in offline mode.

## Before you begin

Role required: mobile\_admin, admin

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

This configuration applies to the record screen.Details screen segment: Use this field to determine which fields are not available after the user performs an action in offline mode. For example, after a user assigns a task to themselves, you could hide the **Assigned to** field.

</td></tr><tr><td>

Show fields

</td><td>

This configuration applies to the record screen.Details screen segment: Use this field to determine which fields are available after the user performs an action in offline mode. For example, after a user assigns a task to themselves, you could show the **Work notes** field.

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

This setting controls which screens should visually reflect that a record was modified while the user was online and is no longer applicable once they go offline. When a user performs an action on a record while online, that record can be marked as “not available” for offline use. As soon as the user goes offline, the record appears with a strikethrough effect to indicate that it is no longer active or interactable.Use the **Select target record** field to select where the "not available" state should display.

 \[Omitted image "offline-changes-pre-sync.png"\] Alt text: Online behavior in "Disable after online edit" mode

</td></tr></tbody>
</table>7.  Select **Save**.


**Parent Topic:**[Supported functions for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/functions-offline.md)

