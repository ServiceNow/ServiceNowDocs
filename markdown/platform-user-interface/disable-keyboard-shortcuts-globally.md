---
title: Disable keyboard shortcuts globally
description: Keyboard shortcuts are enabled by default. You can disable all keyboard shortcuts globally or disable certain shortcuts using different user preferences.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Core UI keyboard shortcuts, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Disable keyboard shortcuts globally

Keyboard shortcuts are enabled by default. You can disable all keyboard shortcuts globally or disable certain shortcuts using different user preferences.

## Before you begin

Role required: admin

For a list of available keyboard shortcuts, see [Core UI keyboard shortcuts](../reference/r_KeyboardShortcuts.md).

## Procedure

1.  To disable all keyboard shortcuts globally for all users, navigate to **All** &gt; **User Administration** &gt; **User preferences**.

    1.  Search for the `glide.ui.keyboard.shortcuts.enabled` user preference.

    2.  Make sure the System check box is selected.

    3.  Change the value to `false`.

    4.  Select **Update**.

2.  To disable a specific keyboard shortcut for all users, navigate to the list of user preferences and search for user preferences ending in `enabled`.

    For example, `glide.ui.keyboard.shortcuts.<shortcut_name>.enabled`.

    1.  Make sure the System check box is selected.

    2.  Change the value to `false`.

    3.  Select **Update**.


**Parent Topic:**[Core UI keyboard shortcuts](../reference/r_KeyboardShortcuts.md)

