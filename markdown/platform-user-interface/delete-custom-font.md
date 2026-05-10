---
title: Delete a custom font from your theme
description: Delete and remove a custom font family or font face you no longer need from your Theme Builder theme.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [theme builder, delete custom font, delete font face]
breadcrumb: [Upload custom font, Global styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Delete a custom font from your theme

Delete and remove a custom font family or font face you no longer need from your Theme Builder theme.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page appears in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    ![Page drop-down list with Editor selected.](../image/tb-editor-page-list.png "Page drop-down list")

3.  From the Theme drop-down list, select the theme that you want to edit.

    The **Global styles** tab opens automatically with the Overview panel displayed.

    ![Example view of the Editor page with custom font listed.](../image/tb-editor-page-view-custom-font.png "Editor page view with custom font listed")

4.  Select the custom font family or font face that you want to delete listed beneath the **Manage custom fonts** header.

    The **View custom font family** or **View font face** modal appears.

5.  Select **Delete**.

    Your font family or font face is no longer displayed.

    **Note:** Deleting the last remaining font face removes the entire font family. If your custom font is your default font, then the default font automatically reverts to Source Sans Pro. If you delete a custom font family that is used for theming your components, Source Sans Pro is applied. If you delete a font face that is used for theming your components, the first font face of that font family is used. If none remain, Source Sans Pro Regular is applied.


**Parent Topic:**[Upload a custom font to your theme](upload-custom-font.md)

