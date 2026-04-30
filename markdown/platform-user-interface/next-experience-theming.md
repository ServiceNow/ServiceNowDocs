---
title: Working with themes in Next Experience
description: Themes enable you to tailor the visual experience for your users, helping to update the look and feel to be more like your brand.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Working with themes in Next Experience

Themes enable you to tailor the visual experience for your users, helping to update the look and feel to be more like your brand.

Quickly create, edit, preview, and publish themes to your experiences using Theme Builder. See [Configure Next Experience with Theme Builder](../task/configuring-next-experience-with-theme-builder.md) for more information.

**Important:** Theming applies to the classic environment in Lists, Forms, and Dashboards. Custom components don't reflect theming.

## Theming at a glance

-   Theming is the ability to customize the Next Experience Design System to reflect your product or brand.
-   Theming means styling various aspects of the ServiceNow® platform while maintaining the overall look and feel.
-   Theming typically involves changing the colors to your company brand colors but can also include typography, imagery, shape and form.

## Theme record

This image shows the default Polaris theme, which is read-only. You create your own themes and styles to be used by experiences in your instance by either cloning the Polaris theme or using Theme Builder. If you clone the Polaris theme, you also must clone the styles under UX Theme Styles and make changes to those styles, as desired. At least one Core type style must be defined.

![Next Experience Polaris UX theme main record with Applicability, Order, Style and Type columns highlighted](../image/comp-theme-overview.png)

## Theme styles

You can configure a theme to match your company brand look and feel in ServiceNow. When you configure a theme, you adjust the color schemes, fonts, and images of your applications. On the Theme Builder Theme form, you configure Order, Style, and Type settings.

-   **Order**

    Style records with higher-order values override styles with lower values. The base system styles all have the order 0. If you meet the Applicability constraint, styles with higher values override the base system styles. If not, the lower-value style is used.

-   **Style**

    Style records define reusable styles that together comprise a theme. Core styles include color, shape and form, typography, and imagery. Variants are a different version of the theme, commonly different colors, that users can select in preferences. The most common use of variants is for accessibility purposes, particularly to account for color blindness. If you decide to use a dark theme, consider selecting the Polaris theme or create a dark alternate color palette in Theme Builder. For more information, see [Add an alternate color palette](../task/tb-edit-color-palette.md).

-   **Type**

    Styles can be of either the Core type or the Variant type. Core styles are active by default. Users can choose from available variants for themselves from the User Preferences, and those variant styles override the core style. Theme Builder doesn’t automatically generate dark theme variants; however, you can create a dark alternate color palette with limited customization. For more information, see [Add an alternate color palette](../task/tb-edit-color-palette.md). The Polaris theme includes a Dark Theme variant that is available on instances with Next Experience enabled.


## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Get help with Theme Builder](theme-builder-get-help-now.md)**  
To get help with Theme Builder, your ServiceNow instance, plugins, permissions, and more, watch a short video to contact the ServiceNow admin who works in your company.
-   **[Configuring Next Experience with Theme Builder](../task/configuring-next-experience-with-theme-builder.md)**  
Reflect your company's brand on your ServiceNow instance by managing, editing, and implementing Next Experience themes in an easy, efficient, and upgrade-safe way using Theme Builder. Before you can use Theme Builder, you must first download it from the ServiceNow® Store. When you have completed the download, you may need to clear your local cache before it appears on your instance.
-   **[Working with the dark theme](tb-working-in-dark-theme.md)**  
The dark theme emits less blue light, making the display easier for your eyes and less disturbing in low-light settings. The dark theme is supported for configurable workspaces, lists, forms, dashboards, and reports.
-   **[Working with theme-able empty state images](themeable-empty-state-images.md)**  
Add theme-able empty state images to customize empty states and improve the user experience. Empty states include guidance or actions for users to add or create content.
-   **[Configuring Next Experience themes and preferences](../task/config-next-experience-themes-prefs.md)**  
Theming in Next Experience applies to individual experiences. As an admin user, you can configure the variables for colors, shapes, fonts, and other aspects of the user experience.
-   **[Edit login theming in Next Experience](../task/edit-login-features-u-n.md)**  
Customize Next Experience login illustrations and welcome text to provide a login experience that reflects your branding.

**Parent Topic:**[Configuring the Next Experience UI](next-experience-ui-admin.md)

