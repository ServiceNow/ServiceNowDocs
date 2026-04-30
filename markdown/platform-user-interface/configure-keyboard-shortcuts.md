---
title: Configure available keyboard shortcuts
description: Administrators can configure which keyboard shortcuts are available to users.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [User preferences, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure available keyboard shortcuts

Administrators can configure which keyboard shortcuts are available to users.

## Before you begin

Role required: admin

## About this task

For a list of available keyboard shortcuts, see [Core UI keyboard shortcuts](../../../use/navigation/reference/r_KeyboardShortcuts.md). You can enable or disable keyboard shortcuts universally by searching for the *glide.ui.keyboard.shorcuts.enabled* user preference. Then select the System checkbox and set the value to False.

You can also use the user preferences to determine which keyboard shortcuts are available to users and what the key combinations are.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User Preferences**.

2.  From the search bar, select **Name**.

3.  Type `*keyboard` to do a contains search for all user preferences containing keyboard in the name.

4.  To allow users to use keyboard shortcuts while typing in a field, set the value for the *glide.ui.keyboard.shortcuts.allow\_in\_input\_fields* user preference to true.

5.  Disable any of the following keyboard shortcuts by changing the value to False.

    |User preference|Description|Keyboard shortcut|
    |---------------|-----------|-----------------|
    |glide.ui.keyboard.shortcuts.main\_frame|Move keyboard focus to the main content on the page.|ctrl+alt+p|
    |glide.ui.keyboard.shortcuts.global\_search|Move keyboard focus to the global search bar in the banner frame.| |
    |glide.ui.keyboard.shortcuts.impersonator|Open the impersonator window.| |
    |glide.ui.keyboard.shortcuts.navigator\_filter|Move keyboard focus to the filter in the application navigator.| |
    |glide.ui.keyboard.shortcuts.navigator\_toggle|Toggle the application navigator open or closed.| |

6.  Use the value for any user preference that ends with key\_combo to change the key combination for that particular keyboard shortcut.


**Parent Topic:**[User preferences](../concept/c_UserPreferences.md)

**Related topics**  


[User preference settings](../reference/r_UserPreferenceSettings.md)

[Turn off the Next Experience welcome screen after upgrading your instance](remove-welcome-splash-screen.md)

