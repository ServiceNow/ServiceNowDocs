---
title: Configure keys for keyboard shortcuts
description: Determine which shortcut key pairings users can use to access elements in an instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Core UI keyboard shortcuts, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure keys for keyboard shortcuts

Determine which shortcut key pairings users can use to access elements in an instance.

## Before you begin

Role required: admin

For a list of available keyboard shortcuts, see [Core UI keyboard shortcuts](../reference/r_KeyboardShortcuts.md).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User Preferences**.

2.  Search for the user preference you want to change the key combination for.

    You can change any of the following options:

    |Shortcut property|Description|
    |-----------------|-----------|
    |glide.ui.keyboard.shortcuts.global\_search.key\_combo|Enables keyboard shortcut to activate global search|
    |glide.ui.keyboard.shortcuts.impersonator.key\_combo|Sets keyboard shortcut for impersonating a user|
    |glide.ui.keyboard.shortcuts.main\_frame.key\_combo|Enables keyboard shortcut to jump to start of main content|
    |glide.ui.keyboard.shortcuts.navigator\_filter.key\_combo|Enables keyboard shortcut to activate navigation filter|
    |glide.ui.keyboard.shortcuts.navigator\_toggle.key\_combo|Enables keyboard shortcut to expand or collapse navigator|

3.  In the Value field, change the value to one of the following combinations:

    Include two access keys such as Control, Command, Alt, or Option as the start keys to any of the following keys. For example, ctrl+alt+p.

    ```
    0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e,
    f, g, h, i, j, k, l, m, n, o, p, q, r, s, t,
    u, v, w, x, y, z, num0, num1, num2, num3, num4, num5, num6, num7,
    num8, num9, f1, f2, f3, f4, f5, f6, f7, f8, f9, f10, f11, f12, num,
     semicolon, equal, equalsign, comma, dash, period, slash, forwardslash,
    graveaccent, openbracket, backslash, closebracket, singlequote, space, spacebar
    ```

4.  Select **Update**.


**Parent Topic:**[Core UI keyboard shortcuts](../reference/r_KeyboardShortcuts.md)

