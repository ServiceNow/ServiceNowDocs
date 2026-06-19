---
title: Override the Next Experience default theme
description: Override the Next Experience theme with your custom theme.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/override-next-experience-theme.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Next Experience themes, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Override the Next Experience default theme

Override the Next Experience theme with your custom theme.

## Before you begin

Prior to the Xanadu release, overriding the Next Experience theme using the `glide.ui.polaris.theme.custom` system property was the primary way to apply a custom look globally. As of Xanadu, you are able to publish multiple themes and select a theme for the Next Experience. The `glide.ui.polaris.theme.custom` system property is only considered if the UX Parent App Themes table is empty. For more information, see [Publish multiple themes in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/configure-presentation-order-of-themes.md). Use override only if you need to enforce a single theme across your instance.

Starting in Zurich, Coral is the default theme for new instances. You can enable Coral or other themes using Theme Builder or by adding them to the UX Parent App Theme table following [Publish multiple themes in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/configure-presentation-order-of-themes.md).

Role required: admin

## About this task

Override the default Next Experience theme while keeping the Next Experience UI.

## Procedure

1.  In the filter navigator field, type `sys_ux_theme.list` and press **Enter**.

2.  Select the theme you want to override the Next Experience theme with.

3.  Right-click the header and select **Copy sys\_id**.

    \[Omitted image "next-exp-override-copy-sys-id.png"\] Alt text: Copy sys id

4.  In the application navigator field, type `sys_properties.list` and press **Enter**.

5.  Select **New**.

6.  Fill in the System Property form.

    \[Omitted image "next-exp-override-form.png"\] Alt text: System property form used to override the next experience theme.

    -   Name the system property `glide.ui.polaris.theme.custom`.
    -   Set the type value to string.
    -   In the value field, paste the sys\_id you copied in step 3.
    -   A **Suffix** field will appear on the System Property form when you want to apply a custom theme to a specific application scope. This field is required.
7.  Select **Submit**.

    Your custom theme appears. If necessary, refresh your browser.

    **Note:** If, for any reason, you decide to revert back to the Polaris theme, repeat steps 4 through 7, replacing the sys\_id in the **Value** field with the sys\_id of the Polaris theme.


**Parent Topic:**[Configuring Next Experience themes and preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/config-next-experience-themes-prefs.md)

