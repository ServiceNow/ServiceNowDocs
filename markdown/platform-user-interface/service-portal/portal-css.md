---
title: Defining portal styles
description: Pages are made up of containers, columns, rows, widgets, and widget instances. You can configure the CSS of each component, or use the CSS defined in theme and branding as global definitions for the portal. If you do not define CSS in theme or branding, Bootstrap defaults are used.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Defining portal styles

Pages are made up of containers, columns, rows, widgets, and widget instances. You can configure the CSS of each component, or use the CSS defined in theme and branding as global definitions for the portal. If you do not define CSS in theme or branding, Bootstrap defaults are used.

You can define CSS in your portal at multiple levels.

-   **Bootstrap defaults**

    If no other CSS is defined, all elements use Bootstrap version 3.3.6 defaults. You can use [Bootstrap CSS Helper Classes](https://www.w3schools.com/bootstrap/bootstrap_ref_css_helpers.asp) with any Service Portal field that accepts CSS as a value. To show or hide Service Portal containers, use Bootstrap CSS Responsive Utilities Helper Classes such as `visible-lg` or `hidden-md`.

-   **Branding editor theme colors/Portal CSS**

    CSS defined in the Branding Editor Theme Colors tab. Changes made to the theme colors in the Branding Editor appear in the CSS variables field in the portal table \[sp\_portal\]. Customizing the theme colors overwrites the Bootstrap defaults.

    ![Branding editor UI, showing the Quick Setup tab and Theme Preview.](../image/branding-theme-colors.png)

-   **Theme CSS**

    CSS defined in the CSS variables field in the Themes table \[sp\_theme\]. Use the Theme CSS as much as possible to allow for more flexible evolution of your portal in the future.

    Using a theme overwrites the Portal CSS/Branding Editor theme colors.

-   **Page CSS**

    CSS defined in the Page Specific CSS field in the Pages table \[sp\_page\].

    Page-specific CSS overwrites the theme CSS.

-   **CSS classes**

    You can define CSS classes elements on the page within each respective record.

-   **Widget CSS**

    CSS defined in the CSS field in the Widgets table \[sp\_widget\].

    Widget CSS overwrites container, column, and row CSS.

-   **Widget instance CSS**

    CSS defined in the CSS field in the Instance table \[sp\_instance\].

    Widget instance CSS overwrites all other CSS definitions.


**Note:** In some cases, default styles for accessibility might overwrite the CSS defined for a portal.

![Diagram showing Service Portal CSS overrides](../image/CSSHierarchyDiagram.png "Hierarchy of style application in the Service Portal")

-   **[Configure portal branding](c_BrandingEditor.md)**  
Use Branding Editor to give your portal its own look and feel.
-   **[Activate La Jolla theme branding](../task/enable-la-jolla-brand-update.md)**  
Activate the Service Portal La Jolla Brand to apply ServiceNow branding, which includes WCAG-AA compliance for contrast. This plugin is active by default on new instances, but admins must activate the plugin on instances upgraded from earlier versions.
-   **[Create a portal theme](c_CustomCSS.md)**  
If you need more customizations than the Branding Editor can provide, you can create your own custom theme.
-   **[Enable text resize in your portal](../task/enable-text-resize.md#)**  
Enable text resize to increase the size of your text up to 200% through your browser settings.
-   **[Styling for right-to-left languages in portals](styling-right-to-left-languages.md)**  
Localizing a portal for right-to-left languages requires CSS that mirrors the direction of portal pages.

**Parent Topic:**[Configuring Service Portal](configuring-service-portal.md)

