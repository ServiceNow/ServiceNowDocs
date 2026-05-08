---
title: Turn off the Next Experience welcome screen after upgrading your instance
description: You can turn off the Next Experience welcome splash screen that appears in the Core UI after upgrading your instance by creating a user preference.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [User preferences, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Turn off the Next Experience welcome screen after upgrading your instance

You can turn off the Next Experience welcome splash screen that appears in the Core UI after upgrading your instance by creating a user preference.

## Before you begin

Role required: admin

## About this task

A Next Experience welcome splash screen appears in the Core UI when you upgrade your instance but haven't turned on the Next Experience UI on the instance.

This welcome splash screen appears for admins only. It informs you about the Next Experience UI so you can enable it. After the welcome splash screen has notified you about the Next Experience UI, you can use the following steps to turn off the splash screen.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User Preferences**.

2.  Click **New**.

3.  Enter the following values.

<table id="choicetable_h1c_4hh_jw"><tbody><tr><td id="d147215e114">

**Description**

</td><td>

A description of the user preference. For example, `Remove the welcome splash screen.`

</td></tr><tr><td id="d147215e126">

**User**

</td><td>

The user that the splash screen is turned off for.

 To turn off the splash screen for all users, leave this field empty.

 To turn off the splash screen for specific users, user the search icon \(![Search image.](../image/SearchIcon.png)\) to find the user and select them in the search results.

</td></tr><tr><td id="d147215e150">

**Name**

</td><td>

User preference name. To turn off the welcome splash screen, enter the following name:

 `overview_help.visited.NextExperience`

</td></tr><tr><td id="d147215e166">

**Value**

</td><td>

Enter `true` to enable this user preference, which turns off the welcome splash screen.

</td></tr><tr><td id="d147215e178">

**Type**

</td><td>

Select **string**.

</td></tr><tr><td id="d147215e191">

**System**

</td><td>

Select this check box to apply this user preference system wide.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The welcome splash screen is marked as **Visited**. When the welcome splash screen is marked as **Visited**, the screen is turned off on your instance for specified users or all users depending on how you configured the **User** option.

    **Note:** In the User Preferences table, verify that there is only one user preference record where the **System** field and **Value** field is set to `true`.


**Parent Topic:**[User preferences](../concept/c_UserPreferences.md)

**Related topics**  


[User preference settings](../reference/r_UserPreferenceSettings.md)

[Configure available keyboard shortcuts](configure-keyboard-shortcuts.md)

