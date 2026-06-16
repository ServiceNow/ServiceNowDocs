---
title: Theme Builder release notes
description: Version history for the Theme Builder application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-ui-theme-builder.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Theme Builder release notes

Version history for the Theme Builder application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.1.0 - June 2026**

    Upload your brand guidelines to generate theme colors.

-   **Version 7.0.1 - March 2026**
    -   Generate AI‑powered color palettes from brand images using the Now Assist panel or within Theme Builder.
    -   Assign fonts and adjust font sizes by component category to create a clear, consistent visual hierarchy.
    -   Access the default icon library and replace icons with custom assets that support size variants and outline or fill styles, inheriting colors from their associated components.
-   **Version 6.1.1 - December 2025**
    -   Enable dark mode to improve the usability of Theme Builder in low-light conditions. This option is commonly used to alleviate eye strain and improve readability. Dark mode applies to the Theme Builder interface only and does not affect the appearance of individual themes.
    -   Configure the following new image categories to further enhance your theme:
        -   Edit the colors of banners, modals, tile icons, and cards from within Theme Builder.
        -   Override each of these default illustrations with your own custom images to uniquely align with your branding style.
    -   Create a theme wizard color selector updated: When you create a theme, the color selector now defaults to Coral theme colors instead of static gray tones. This means your initial color options feature a blue hue for a more vibrant look. Colors can still be customized at any time by selecting a preferred color in the color selector
    -   Learn about additional features and complete tasks through interactive steps by taking updated guided tours within Theme Builder.
-   **Version 6.0.3 - August 2025**
    -   Upload and manage custom fonts in your theme Use your organization's fonts to maintain a consistent look and feel for your brand throughout your experience.
        -   Upload, preview, and edit up to 10 custom font families from the Global styles or Component styles tabs.
        -   Add unlimited associated font faces to each font family and apply them individually to components.
        -   Delete your font family or font face from your theme.
    -   Publish the new Coral themePublish or unpublish the new Coral theme directly from Theme Builder. This theme provides a fresh look and feel and features brand-neutral illustrations to improve your user experience. A dark theme variant is available for web and mobile experiences.
-   **Version 5.2.4 - May 2025**
    -   New:
        -   As of Theme Builder version 5.1, customize the colors of empty state illustrations from within the application.
        -   As of Theme Builder version 5.1, override the empty state illustrations with your own custom images.
    -   Changed: As of Theme Builder version 5.1, the Accessibility Inspector now displays the total number of accessibility errors with contrast issues for the Unified Navigation component and subcomponents. See the Accessibility section for details.
-   **Version 5.0.3 - February 2025**
    -   Theme Builder highlights for the Yokohama release
        -   Edit and style the Unified Navigation component to better suit your brand
        -   Double-click any component to quickly access the Component Editor where you can make individual style edits
    -   New in the Yokohama release Edit the Unified Navigation component
        -   Edit the Unified Navigation header component and drill down to style its subcomponents.
        -   Use the component configuration menu to view any shared styling between subcomponents.
        -   View the background color of your subcomponent and see how it renders in relation to the Unified Navigation component using the updated canvas color feature.
    -   Use the double-click feature to quickly access the Component Editor Double-click on a component tile to access the component editor where you can continue to make style adjustments to subcomponents, variants or interactions.
    -   UI changes:
        -   Navigation updated
        -   The Return to component overview link within the Component Editor is replaced with breadcrumb-style navigation for a more contextual navigation experience.
        -   Component Editor button replaced
        -   The Go to Component Editor button is now labeled either Style variants, Style subcomponents, or Style interactions depending on the selected component.
        -   The Component Editor behaves in the same way despite this UI change.
        -   Component Editor Interaction States panel updated
        -   The Interaction States panel within the Component Editor now refers to either Interactions, or Subcomponents.
-   **Version 4.1.2 - November 2024**
    -   New:
        -   Use the drag-and-drop feature in List view to publish and unpublish your themes for your web instance.
        -   Define the presentation order of themes displayed in Next Experience user preferences by using the drag-and-drop feature in the List view.
        -   Remove overrides you've made to Global Styles and revert back to your initial values using the Remove Override button.
        -   Get notified when a new update is available from within Theme Builder.
    -   Changed:
        -   Use the updated accessibility inspector to identify and address all accessibility violations within your theme. This tool includes the total number of errors along with the component details where the a11y error has occurred.
        -   Reflow improvements for the Home, Manager, and Editor pages.
        -   Reflow improvements for the create theme and add an alternate color palette wizard.
        -   Updated modal for publishing a theme group on the web. Theme groups consist of themes and their alternate color palettes. A warning appears if there is an a11y error in the theme or it's alternate color palette.
-   **Version 4.0.1 - August 2024**
    -   Theme Builder highlights for the Xanadu release:
        -   Achieve your branding and styling needs by offering multiple themes and alternate color palettes to your users.
        -   Add a dark alternate color palette to your newly created themes and edit to refine your theme.
        -   Important: Theme Builder is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.
    -   New in the Xanadu release:
    -   -   Publish multiple themes along with their alternate color palettes to your web instance. Set a default theme for your users.
-   Add a dark alternate color palette to your Theme Builder theme. You can edit this alternate color palette to further enhance your brand style.
-   Define the presentation order of themes displayed in Next Experience user preferences.
-   View multiple themes and their alternate color palettes in Next Experience user preferences.
-   Manage your web and mobile theming experiences separately using the manager view.
    -   Removed in this release:
    -   -   Removed the Apply button used to apply your theme to web and mobile instances.
-   To Publish your theme, use the Publish option from the overflow menu. For more information about publishing themes, see Publish your themes with Theme Builder.
-   **Version 3.1.2 - May 2024**
    -   While customizing a UX theme record, an Open in Theme Builder button displays redirecting you to the editor page in a new tab.
    -   Theme Builder now validates JSON for the style and theme records. Theme Builder logs any errors and displays an alert for any invalid manual theming updates, preventing you from saving an incorrect theme record.
    -   Customize shape and typography values and view these customizations in the global and component styles tabs.
-   **Version 3.0.0 - February 2024**
    -   Component editing: Edit individual components to better suit your brand and to meet accessibility compliance standards. The theme hooks you can edit are specific to each type of component.
    -   Context-sensitive messaging: Learn about new features in Theme Builder as you upgrade versions.
-   **Version 2.0.2 - August 2023**

    Changed: Security fix.

-   **Version 2.0.1 - August 2023**
    -   New: Create, edit, and manage alternative color palettes
    -   Changed: Updated component preview page with filtering capability
-   **Version 1.1.2 - May 2023**
    -   New:
        -   Apply web themes to mobile experiences.
        -   Apply themes to web and mobile for consistent styles across the platform.
        -   Apply themes to all mobile apps for consistent styles across mobile experiences.
        -   Use Theme Builder workflows to create, refine and organize your themes for both web and mobile experiences.
    -   Changed:
        -   Updated look and feel.
        -   Minor functional and design bug fixes.
        -   Sys prop for logo override is no longer required.
-   **Version 1.0.1 - February 2023**
    -   Theme Builder is a guided, low-code tool for creating themes to reflect your company's brand in your experience. Theme Builder saves time and reduces complexity by automating color generation, coding styles and application of your theme in an easy and efficient workflow. Admins with any level of expertise can make and use a custom theme within minutes.
        -   Create your theme including your brand colors, logo, typography, corner shapes through an intuitive wizard workflow.
        -   Edit a theme further using a style panel to refine brand attributes at a global level.
        -   Preview changes made to styles in real time on an instance and as an abstracted image.
        -   Manage and apply themes to your instance in one location

