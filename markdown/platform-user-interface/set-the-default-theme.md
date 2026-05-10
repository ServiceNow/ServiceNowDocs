---
title: Set the default theme
description: Set a preferred Theme Builder theme as the default for your web experiences when multiple themes are published.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Publish themes, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Set the default theme

Set a preferred Theme Builder theme as the default for your web experiences when multiple themes are published.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

## About this task

If you have published only one theme to your web instance, that theme is automatically set as the default theme.

The default theme is treated as the first theme that is displayed in the Next Experience Theme user preference. If a user has not made a selection from the Theme user preference, the default theme is displayed.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page appears in the Home page view.

2.  From the Home page view, select the Manager page view to see the themes that you have created.

3.  From the Published section, choose the theme that you want to set as the default.

    **Note:** When you have selected the theme that you want to set as the default, verify that you have selected the correct scope for the theme from the application scope picker.

4.  Select the More actions icon ![](../image/tb-more-actions.png)from the theme that you have selected, and select **Mark as default**.

    ![Mark as default option.](../image/tb-mark-as-default.png)

    The theme is listed as the Default within the Published section. The default theme is treated as the first theme and each theme listed after the default theme follows a sequential order.

    ![Default theme displayed in Published section.](../image/tb-theme-default.png)

5.  Refresh your browser to view the new theme.

    The default theme appears first in the user's Theme preference.


**Parent Topic:**[Publish your themes with Theme Builder](tb-apply-theme.md)

