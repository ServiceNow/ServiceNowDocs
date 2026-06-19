---
title: Enable the Next Experience dark theme for limited classic environment and configurable workspaces
description: Enable the Next Experience dark theme for limited classic environment and configurable workspaces by using system properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/tb-enable-dark-theme-using-sysprops.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dark theme, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Enable the Next Experience dark theme for limited classic environment and configurable workspaces

Enable the Next Experience dark theme for limited classic environment and configurable workspaces by using system properties.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and then in the filter navigator, search for `sys_properties.list`.

2.  In the list search bar, search for `glide.ui.polaris.dark_themes_enabled`.

    \[Omitted image "next-exp-enable-dark-theme.png"\] Alt text: System properties list search bar.

3.  Enable the dark theme for use in your Next Experience limited classic environment and configurable workspace instances by setting `glide.ui.polaris.dark_themes_enabled` to **True**.

    \[Omitted image "next-exp-enable-dark-theme-property.png"\] Alt text: Set system property value to true.


**Parent Topic:**[Working with the dark theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/tb-working-in-dark-theme.md)

