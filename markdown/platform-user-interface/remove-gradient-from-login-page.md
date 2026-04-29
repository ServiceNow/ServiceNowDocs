---
title: Remove the gradient from the Next Experience login page
description: Remove the gradient from the Next Experience login page and restore the solid color of your default theme.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Remove the gradient from the Next Experience login page

Remove the gradient from the Next Experience login page and restore the solid color of your default theme.

## Before you begin

Role required: admin

Before starting, delete any system properties you've created for background illustrations or custom background colors. These settings override the gradient color and must be removed to apply changes successfully.

-   Background illustration system property: **glide.ui.login.style.background.image**
-   Custom background color system property:**glide.ui.polaris.login.style.background**

## About this task

The gradient feature inherits the colors of the default theme, which is the theme that appears first in the user's Theme preference menu when multiple themes are published, or it is automatically applied across the instance when only one theme is available. When the gradient is removed, the login page displays a solid color based on the default theme. This color does not reflect the theme the user selects manually if it differs from the default. For information setting the default theme for your Theme Builder themes, see [Set the default theme](set-the-default-theme.md). For information setting the default theme for Theme Builder and themes created manually using Next Experience, see [Publish multiple themes in Next Experience](configure-presentation-order-of-themes.md).

## Procedure

1.  Navigate to the **All** menu and enter `sys_properties.list` in the filter navigator.

2.  In the **Name** field, enter `glide.ui.polaris.login.show_illustrations`.

3.  In the **Value** field, enter `false` and select the green check mark to save your selection.


## What to do next

Log out of your experience to view the new login page background color.

**Parent Topic:**[Working with themes in Next Experience](../concept/next-experience-theming.md)

