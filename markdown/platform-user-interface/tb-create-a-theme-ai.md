---
title: Create a theme with AI in Theme Builder
description: Use an AI-powered theme creation from within Theme Builder to generate themes from brand images, preview, and refine results all within the updated Create a theme wizard.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-01-22"
reading_time_minutes: 3
breadcrumb: [Theme creation with AI, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Create a theme with AI in Theme Builder

Use an AI-powered theme creation from within Theme Builder to generate themes from brand images, preview, and refine results all within the updated Create a theme wizard.

## Before you begin

This feature requires:

-   Now Assist for Creator installed. See [Install Now Assist for Creator](https://www.servicenow.com/docs/access?context=install-now-assist-for-creator&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

    ![Theme Builder Home screen.](../image/tb-ai-home.png "Theme Builder Home screen")

2.  Select **Create a theme**.

    The Create a theme wizard appears to guide you through your brand configurations, as described in the next steps.Your selections are saved automatically as you progress through the wizard.

3.  Enter the name and a description of your new theme, and select **Next**.

4.  Choose how to define your theme colors.

    |Option|Action|
    |------|------|
    |**Upload brand image**|AI automatically extracts a color palette from your image.|
    |**Select __Handpick my colors__**|Manually choose your theme colors|

    ![Theme Creation wizard showing the option to upload a brand image or handpick colors to generate a color palette.](../image/tb-nap-wizard-flow-2.png "Generate theme colors using AI or manual selection")

5.  If you chose to upload a brand image, generate your theme colors using AI.

    1.  Upload your brand image.

        Supported formats are JPEG, JPG, PNG, and SVG with a maximum size of 1 MB.![Theme Creation wizard showing a brand image uploaded to generate a color palette using AI.](../image/tb-nap-wizard-upload-image.png)

    2.  Select **Generate Palette**.

    3.  Review the AI‑generated primary and secondary colors, then use the simplified preview to see where the colors appear in your instance.

    4.  Modify the palette by selecting either the Primary or Secondary tile and select the **add \(+\)** button or choose from the AI-generated supporting colors.

        **Note:** The AI detects up to eight colors from your image, with the two most dominant pre-selected as the primary and secondary. Any additional detected colors are suggested as available options that you can swap in as needed.

        ![Theme Creation wizard showing primary and secondary colors with a color selector for adjusting the primary palette.](../image/tb-nap-wizard-flow-manage-colors.png)

    5.  Choose a new color from the color selector and select **Apply**.

    6.  Select **back** to return and choose a different image or to handpick your colors.

    7.  Select **Next**.

6.  If you selected **Handpick my colors**, define your theme colors manually.

    1.  Select the Primary tile and choose your brand’s primary color from the color selector or enter a value using HEX, RGB, or HSL.

        ![Your brand's primary color](../image/tb-select-primary-color.png "Your brand's primary color")

    2.  After you identify the primary color of your brand, select **Apply**.

    3.  Select the Secondary tile and choose your brand’s secondary color from the color selector.

    4.  Select **Apply**.

    5.  Select **Generate with AI instead** to return to the AI-generated palette step.

    6.  Select **Next**.

7.  Upload your brand logo, confirm it appears correctly in the preview, and select **Next**.

    If you don’t add a logo, the ServiceNow logo is used.

8.  Select the preferred font for your text and select **Next**.

9.  Select the corner shape of your components in the interface, such as the buttons, modals, and drop-down menus, and select **Next**.

10. Review your selections and select **Create theme**.

    **Note:** From this screen, you can edit any part of the theme before selecting **Create theme**. After the theme is created, any changes you make are automatically saved.

    ![Final review screen showing theme information, brand colors, and a preview before creating the theme.](../image/tb-nap-wizard-flow-summary.png "Theme details and final preview before creation")


## Result

Your theme is saved as a draft in Theme Builder and appears in the Unpublished section of the Manager page.

## What to do next

After creating your theme in the wizard, you are directed to the Editor view of the theme where you can continue [modifying](tb-edit-theme.md) or [publish your theme](tb-apply-theme.md).

**Parent Topic:**[Theme creation with AI](../concept/theme-creation-with-ai.md)

