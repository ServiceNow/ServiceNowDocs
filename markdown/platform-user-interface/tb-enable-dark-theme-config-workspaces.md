---
title: Enable the dark theme only in configurable workspaces
description: Enable the Next Experience dark theme in configurable workspaces only, and not for the classic environment. The dark theme emits less blue light, making the display easier for your eyes and less disturbing in low-light settings.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dark theme, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Enable the dark theme only in configurable workspaces

Enable the Next Experience dark theme in configurable workspaces only, and not for the classic environment. The dark theme emits less blue light, making the display easier for your eyes and less disturbing in low-light settings.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and in the filter navigator, search for `sys_properties.list`.

2.  In the list search bar, search for `glide.ui.polaris.dark_themes_enabled`.

3.  Enable the dark theme in all of your Next Experience configurable workspaces by setting `glide.ui.polaris.dark_themes_enabled` to **True**.

4.  In the list search bar, search for `glide.ui.polaris.core_ui_exclude_dark_mode`.

5.  Exclude the dark theme in the classic environment by setting `glide.ui.polaris.core_ui_exclude_dark_mode` to **True**.

    **Note:** If you select the dark theme, the dark theme only applies to the configurable workspaces. The classic environment remains in the default theme.


**Parent Topic:**[Working with the dark theme](../concept/tb-working-in-dark-theme.md)

