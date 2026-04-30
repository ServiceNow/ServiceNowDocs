---
title: Create a theme using Now Assist
description: Use Now Assist to generate themes from your brand image. This AI-powered workflow extracts color palettes automatically, creating visually consistent themes without requiring brand color codes.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-02-02"
reading_time_minutes: 3
breadcrumb: [Theme creation with AI, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Create a theme using Now Assist

Use Now Assist to generate themes from your brand image. This AI-powered workflow extracts color palettes automatically, creating visually consistent themes without requiring brand color codes.

## Before you begin

This feature requires:

-   Now Assist for Creator installed. See [Install Now Assist for Creator](https://www.servicenow.com/docs/access?context=install-now-assist-for-creator&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   A theme creation workflow enabled in AI Agent Studio. See [Turn on theme creation workflow for use in the Now Assist panel](turn-on-theme-creation-workflow.md).
-   Now Assist panel turned on. See [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Roles required:

-   admin
-   now\_assist\_panel\_user

## Procedure

1.  Select the Now Assist sparkle icon ![](../../../get-started/servicenow-overview/image/icon-now-assist.png) to display the Now Assist panel.

2.  In the chat window, enter `Create a theme`.

    This triggers the AI-enabled Theme Builder workflow.

    ![Now Assist panel with Create a theme entered into the chat window.](../image/tb-nap-chat-window.png "Now Assist panel")

3.  Select **Yes** when prompted to proceed.

4.  Select **Show** to open the theme creation wizard.

    ![Theme Builder Show button highlighted.](../image/tb-nap-show-button.png "Launch theme creation wizard")

5.  Enter your theme name and a description, then select **Next**.

6.  Choose how to define your theme colors.

    |Option|Action|
    |------|------|
    |**Upload brand image**|AI automatically extracts a color palette from your image.|
    |**Select __Handpick my colors__**|Manually choose your theme colors|

    ![Theme Creation wizard showing the option to upload a brand image or handpick colors to generate a color palette.](../image/tb-nap-wizard-flow-2.png "Generate theme colors using AI or manual selection")

7.  If you chose to upload a brand image, generate your theme colors using AI.

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

8.  If you selected **Handpick my colors**, define your theme colors manually.

    1.  Select the Primary tile and choose your brand’s primary color from the color selector or enter a value using HEX, RGB, or HSL.

        ![Your brand's primary color](../image/tb-select-primary-color.png "Your brand's primary color")

    2.  After you identify the primary color of your brand, select **Apply**.

    3.  Select the Secondary tile and choose your brand’s secondary color from the color selector.

    4.  Select **Apply**.

    5.  Select **Generate with AI instead** to return to the AI-generated palette step.

    6.  Select **Next**.

9.  Upload your brand logo, confirm it appears correctly in the preview, and select **Next**.

    If you don’t add a logo, the ServiceNow logo is used.

10. Select the preferred font for your text and select **Next**.

11. Select the corner shape of your components in the interface, such as the buttons, modals, and drop-down menus, and select **Next**.

12. Review your selections and make any changes, if needed.

    ![Final review screen showing theme information, brand colors, and a preview before creating the theme.](../image/tb-nap-wizard-flow-summary.png "Theme details and final preview before creation")

13. Select **Create theme**.

    **Note:** Themes aren't saved until **Create theme** is selected. Leaving the chat or restarting the workflow discards the theme.

14. Select **Personalize your theme** to customize or publish your theme from Theme Builder.


## Result

Your theme is saved as a draft in Theme Builder and appears in the Unpublished section of the Manager page.

## What to do next

Customize and publish your theme in Theme Builder. See [Manage or edit a theme with Theme Builder](tb-edit-theme.md)\[Publish a theme\] and [Publish your themes with Theme Builder](tb-apply-theme.md).

**Parent Topic:**[Theme creation with AI](../concept/theme-creation-with-ai.md)

