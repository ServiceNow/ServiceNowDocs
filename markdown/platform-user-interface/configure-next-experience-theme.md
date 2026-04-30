---
title: Configure a Next Experience theme
description: Add the styles that you have created to your Next Experience theme to modify the look and feel of the user experience.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring Next Experience themes and preferences, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure a Next Experience theme

Add the styles that you have created to your Next Experience theme to modify the look and feel of the user experience.

## Before you begin

Ensure that the following system properties that are located in `sys_properties.list` are set to **True**:

-   **glide.ui.polaris.experience**
-   **glide.ui.polaris.dark\_themes\_enabled**: To reuse the Next Experience dark variant in this theme.

Role required: admin

## About this task

The default Next Experience theme is called Polaris. You can reuse or customize the theme as a starting point when you create or modify your own themes.

## About this task

**Note:** If you're customizing a theme that you created with Theme Builder and enter invalid JSON code, you can't save your theme record. While working in the UX theme record, you can navigate to the Editor page by using the **Open in Theme Builder** button. For more information, see [Manage or edit a theme with Theme Builder](tb-edit-theme.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Management** &gt; **Themes**.

2.  Create a theme record by selecting **New**.

3.  Enter a name and a description for your theme.![UX Theme form.](../image/next-exp-theming-form.png)

4.  Select the Additional actions icon \(![Additional actions icon](../image/icon-context-p.png)\) and select **Save**.

5.  On the **Compositional: App Theme** tab, insert rows to add styles that are associated with your theme.

    You assign values in four columns:

    -   **Applicability**

        Overrides the base theme. Users who meet the applicability constraints see those overrides in their theme rather than the base style. For example, a style with different fonts can be applied to managers. Users who meet the manager applicability see the different fonts in the Next Experience UI, which overrides the base system theme values. Administrators do not have to copy or create an entire theme with changes for the applicable audience.

        **Note:** Leaving the Applicability constraint to empty will apply the style to all users.

    -   **Order**

        Specifies when the style is applied. The higher the order means that the greater its priority is.

        **Note:** If you want to use a custom style, make sure that your style order number is higher than the standard Polaris style.

    -   **Style**

        Configures four main styles. You can't edit the style names that are used in the Polaris theme, but you can copy the JSON code that is associated with each style from this theme and paste and edit it in your custom style's form.

        -   **Colors:** Specifies the color properties of the theme and any base variants that you want to add. In the base section of the color style, a subset of the colors that the theme uses are defined with Red, Green, Blue \(RGB\) values. The theme generates more than 20 gradients of those colors in the application.
        -   **Shape and Form:** Specifies the look and feel of the borders as well as the buttons and other UI controls.
        -   **Imagery:** Adds images that are used in your application's theme.
        -   **Typography:** Specifies the fonts that are used throughout the application.
    -   **Type**

        Specifies two types: Core and Variant. The Core styles include the color, shape and form, typography, and imagery. Variants specify a different version of the theme, such as the different colors that users can select. The most common variant is a dark version of the theme. The Dark theme is the only variant that is shipped with Next Experience. For more information, see [Working with themes in Next Experience](../concept/next-experience-theming.md).

6.  Select the **Style** field and select the search icon \( ![UX style search icon.](../image/ux-style-search.png)\).

7.  Select **New**.

8.  Select Primary, Secondary, and Neutral colors.

    **Note:** A theme is made up of multiple variables, so you may notice the default Polaris theme coloring coming through in different places.

9.  When you have your organization's branding colors, navigate to the color generator at [https://theme.deoprototypes.com/color-generator-algo-v1](https://theme.deoprototypes.com/color-generator-algo-v1).

10. Select the **Auto Generate** button.

    A modal pops up and asks you to enter in the three colors from your organization.

11. Enter your hex code values for your organization's colors.

12. Select **Generate**.

13. Gather your CSS variables by selecting **Copy JSON**.

14. Fill in the UX style form.![UX Style form.](../image/ux-style-theme-form.png)

<table id="table_hh5_w11_45b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your UX style.

</td></tr><tr><td>

Type

</td><td>

-   Core
-   Variant
 For more information on types, see [Difference between core styles and variants](../reference/difference-themes-variants.md).

</td></tr><tr><td>

Style

</td><td>

Values for the colors, shapes, and forms. Some of the values are colors and some, like borders, are pixel values.**Important:** JSON code must be wrapped as shown in the following example.![Property value string.](../image/property-values.png)

</td></tr><tr><td>

Application

</td><td>

Scope of the UX style.

</td></tr></tbody>
</table>15. Select **Submit**.

16. Select **Update**.


## What to do next

To publish your custom theme, see [Publish multiple themes in Next Experience](configure-presentation-order-of-themes.md).

**Parent Topic:**[Configuring Next Experience themes and preferences](config-next-experience-themes-prefs.md)

