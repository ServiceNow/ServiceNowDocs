---
title: Override the Next Experience theme
description: Override the Next Experience theme with your custom theme.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Next Experience themes and preferences, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Override the Next Experience theme

Override the Next Experience theme with your custom theme.

## Before you begin

The **glide.ui.polaris.theme.custom** was used to override the Next Experience theme prior to the Xanadu release. As of Xanadu, you are able to publish multiple themes and select a theme for the Next Experience. The **glide.ui.polaris.theme.custom** system property is only considered if the UX Parent App Themes table is empty. For more information, see [Publish multiple themes in Next Experience](configure-presentation-order-of-themes.md).

Role required: admin

## About this task

Override the default Next Experience theme while keeping the Next Experience UI.

## Procedure

1.  In the filter navigator field, type `sys_ux_theme.list` and press **Enter**.

2.  Select the theme you want to override the Next Experience theme with.

3.  Right-click the header and select **Copy sys\_id**.

    ![Copy sys id](../image/next-exp-override-copy-sys-id.png)

4.  In the application navigator field, type `sys_properties.list` and press **Enter**.

5.  Select **New**.

6.  Fill in the System Property form.

    ![System property form used to override the next experience theme.](../image/next-exp-override-form.png)

    -   Name the system property `glide.ui.polaris.theme.custom`.
    -   Set the type value to string.
    -   In the value field, paste the sys\_id you copied in step 3.
    -   A **Suffix** field will appear on the System Property form when you want to apply a custom theme to a specific application scope. This field is required.
7.  Select **Submit**.

    Your custom theme appears. If necessary, refresh your browser.

    **Note:** If, for any reason, you decide to revert back to the Polaris theme, repeat steps 4 through 7, replacing the sys\_id in the **Value** field with the sys\_id of the Polaris theme.


**Parent Topic:**[Configuring Next Experience themes and preferences](config-next-experience-themes-prefs.md)

