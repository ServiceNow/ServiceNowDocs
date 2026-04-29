---
title: Working with themes in Next Experience
description: Themes enable you to tailor the visual experience for your users, helping to update the look and feel to be more like your brand.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Working with themes in Next Experience

Themes enable you to tailor the visual experience for your users, helping to update the look and feel to be more like your brand.

Quickly create, edit, preview, and publish themes to your experiences using Theme Builder. See [Configure Next Experience with Theme Builder](../task/configuring-next-experience-with-theme-builder.md) for more information.

**Important:** Theming applies to the classic environment in Lists, Forms, and Dashboards. Custom components don't reflect theming.

## Theming at a glance

-   Theming is the ability to customize the Next Experience Design System to reflect your product or brand.
-   Theming means styling various aspects of the ServiceNow® platform while maintaining the overall look and feel.
-   Theming typically involves changing the colors to your company brand colors but can also include typography, imagery, shape and form.

## Next Experience default themes

New customers launching on Zurich will have the Next Experience Coral theme enabled by default on their instance.

Existing customers upgrading from a previous release will continue to see the theme they've applied to their instance prior to upgrade, for example the Next Experience Polaris theme or a theme created in Theme Builder. Use [Theme Builder to publish Coral theme to your instance](../task/tb-apply-theme.md) or [add Coral theme to the Next Experience UX Parent App Theme table.](../task/configure-presentation-order-of-themes.md)

![Theme preference with Polaris and Coral themes displayed.](../image/next-exp-coral-polaris.png "Next Experience default themes in Preferences modal")

![Record page with Coral theme light variant applied.](../image/next-exp-coral-record-light.png "Coral theme light variant")

![Record page with Coral theme dark variant applied.](../image/next-exp-coral-record-dark.png "Coral theme dark variant")

## Theme record

This image shows the default Polaris theme, which is read-only. You create your own themes and styles to be used by experiences in your instance by either cloning the Polaris or Coral theme or [by cloning a Theme Builder theme record](../task/create-custom-theme-using-theme-builder-record.md). If you clone either the Polaris or Coral theme, you also must clone the styles under UX Theme Styles and make changes to those styles, as desired. At least one Core type style must be defined.

![Next Experience Polaris UX theme main record with Applicability, Order, Style and Type columns highlighted](../image/comp-theme-overview.png)

## Theme styles

You can configure a theme to match your company brand look and feel in ServiceNow. When you configure a theme, you adjust the color schemes, fonts, and images of your applications. On the Theme Builder Theme form, you configure Order, Style, and Type settings.

-   **Order**

    Style records with higher-order values override styles with lower values. The base system styles all have the order 0. If you meet the Applicability constraint, styles with higher values override the base system styles. If not, the lower-value style is used.

-   **Style**

    Style records define reusable styles that together comprise a theme. Core styles include color, shape and form, typography, and imagery. Variants are a different version of the theme, commonly different colors, that users can select in preferences. The most common use of variants is for accessibility purposes, particularly to account for color blindness. If you decide to use a dark theme, consider selecting the Polaris or Coral theme or [create a dark alternate color palette in Theme Builder](../task/tb-edit-color-palette.md).

-   **Type**

    Styles can be of either the Core type or the Variant type. Core styles are active by default. Users can choose from available variants from their Theme user preference, and those variant styles override the core style. Theme Builder doesn’t automatically generate dark theme variants; however, you can create a dark alternate color palette with limited customization. For more information, see [Add an alternate color palette](../task/tb-edit-color-palette.md). The Polaris and Coral themes include a Dark Theme variant that is available on instances with Next Experience enabled.


-   **[Guided tours in Theme Builder](guided-tours-theme-builder.md)**  
Learn about Theme Builder guided tours, including how to access and take them to build your knowledge of Theme Builder.
-   **[Dark mode in Theme Builder](dark-mode-theme-builder.md)**  
Learn how to switch to dark mode in Theme Builder.
-   **[Get help with Theme Builder](theme-builder-get-help-now.md)**  
To get help with Theme Builder, your ServiceNow instance, plugins, permissions, and more, watch a short video to contact the ServiceNow admin who works in your company.
-   **[Configuring Next Experience with Theme Builder](../task/configuring-next-experience-with-theme-builder.md)**  
Reflect your company's brand on your ServiceNow instance by managing, editing, and implementing Next Experience themes in an easy, efficient, and upgrade-safe way using Theme Builder. Theme Builder is included as a core plugin with the Next Experience and is available by default.
-   **[Working with the dark theme](tb-working-in-dark-theme.md)**  
The dark theme emits less blue light, making the display easier for your eyes and less disturbing in low-light settings. The dark theme is supported for configurable workspaces, lists, forms, dashboards, and reports.
-   **[Working with theme-able empty state images](themeable-empty-state-images.md)**  
Add theme-able empty state images to customize empty states and improve the user experience. Empty states include guidance or actions for users to add or create content.
-   **[Configuring Next Experience themes and preferences](../task/config-next-experience-themes-prefs.md)**  
Theming in Next Experience applies to individual experiences. As an admin user, you can configure the variables for colors, shapes, fonts, and other aspects of the user experience.
-   **[Configure login theming in Next Experience](../task/edit-login-features-u-n.md)**  
Customize Next Experience login illustrations and welcome text to provide a login experience that reflects your branding.
-   **[Customize the Next Experience login background illustration](../task/customize-login-background.md)**  
Customize and change the background illustration applied to your Next Experience login page.
-   **[Customize the Next Experience login background color](../task/customize-ne-login-background-color.md)**  
Customize and change the background color applied to your Next Experience login page.
-   **[Remove the gradient from the Next Experience login page](../task/remove-gradient-from-login-page.md)**  
Remove the gradient from the Next Experience login page and restore the solid color of your default theme.

**Parent Topic:**[Configuring the Next Experience UI](next-experience-ui-admin.md)

