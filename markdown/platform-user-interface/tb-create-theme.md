---
title: Create a theme with Theme Builder
description: Create a theme record for your web or mobile experiences by using the Home view in the Theme Builder application.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [theme, theme builder, add a theme]
breadcrumb: [Configuring Next Experience with Theme Builder, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Create a theme with Theme Builder

Create a theme record for your web or mobile experiences by using the Home view in the Theme Builder application.

## Before you begin

Once you've downloaded Theme Builder from the ServiceNow Store, you must activate the plugin \(sn\_theme\_builder\). To activate the Theme Builder plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Themes** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

    ![Theme Builder Home screen](../image/tb-home.png "Theme Builder Home screen")

2.  Select **Create a theme**.

    The Before we get started wizard appears to guide you through your brand configurations, as described in the next steps. The theme record is saved automatically as you work.

    ![Before we get started wizard.](../image/tb-wizard.png "Before we get started wizard")

3.  Start defining your new theme by selecting **Continue**.

4.  Insert the name and a description of your new theme, and select **Next**.

5.  Select the **Primary** tile, select your brand’s primary color, and review the simplified preview to see where the selected color displays in your instance.

    ![Your brand's primary color](../image/tb-select-primary-color.png "Your brand's primary color")

    -   In the Color Name dialog box, you can select the color model that you prefer: HEX, RGB, or HSL.
    -   When editing theme colors, you can view the contrast ratio in the color picker. The value updates when you change the color from the palette or My colors view.
6.  After you identify the primary color of your brand, select **Apply**, and then select **Next**.

7.  If your brand includes a secondary color, repeat the previous step on the secondary color screen.

8.  Repeat the previous step to define a neutral brand color for divider lines and surface containers.

9.  Choose additional colors for your brand and select **Next**.

10. Upload your brand logo and review the simplified preview to verify that it appears as expected with the primary color you chose, and then select **Next**.

11. Select the preferred font for your text and select **Next**.

    **Note:** If you prefer to customize your font, see [Create a Next Experience style](create-next-experience-style.md). After you save your customized font type and refresh the page, the new font appears as `Custom Font`. If you delete the custom font from your theme record, the font reverts to `Source Sans Pro` as the default.

12. Select the corner shape of your components in the interface, such as the buttons, modals, and drop-down menus, and select **Next**.

    **Note:** If you prefer to customize your shape, see [Create a Next Experience style](create-next-experience-style.md). After you save your customized shape and refresh the page, the new shape appears as `Mixed`. This custom value is also displayed in the **Component Styles** tab, where you can edit the custom value.

13. Review your selections and select **Create theme**.

    **Note:** You can select **Back** to make changes in the wizard before selecting **Create theme**.

    After creating your theme in the wizard, you’re directed to the Editor view of the theme where you can continue [modifying](tb-edit-theme.md) or [publish your theme](tb-apply-theme.md).


**Parent Topic:**[Configuring Next Experience with Theme Builder](configuring-next-experience-with-theme-builder.md)

