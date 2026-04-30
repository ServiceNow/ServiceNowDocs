---
title: Manage or edit a theme with Theme Builder
description: Customize and manage your theme and styling in a time and cost efficient way. After customizing, publish your new theme to either a web or mobile implementation of your instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
keywords: [customize theme, edit theme, manage theme, change theme]
breadcrumb: [Configuring Next Experience with Theme Builder, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Manage or edit a theme with Theme Builder

Customize and manage your theme and styling in a time and cost efficient way. After customizing, publish your new theme to either a web or mobile implementation of your instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Themes** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

2.  From the Home page view, select Manager page view to see all available themes.

    ![Page menu.](../image/tb-home.png "Page menu")

    From the Manager page view, you have the choice of viewing existing themes in two ways. You can choose the Grid view or the List view.

    **Note:** In both the Grid and List views, your published and unpublished themes are grouped separately. The published themes are themes that appear in the user's theme preference. View your web and mobile themes by selecting either the **Web** or **Mobile** button.

    ![Grid view.](../image/tb-grid-view.png "Grid view")

    ![List view.](../image/tb-list-view.png "List view")

    The More actions \(![More actions icon.](../image/tb-more-actions.png)\) icon for published themes contains the following options:

    -   Duplicate
    -   Delete
    -   Add alternate color palette
    -   Unpublish
    -   Mark as default

        **Note:** This option appears if the theme isn’t the current default theme.

    The More actions \(![More actions icon.](../image/tb-more-actions.png)\) icon for published themes with the alternate color palettes defined contains the following options:

    -   Edit group name
    -   Duplicate
    -   Delete
    -   Unpublish
    -   Mark as default

        **Note:** This option appears if the theme isn’t the current default theme.

    The More actions \(![More actions icon.](../image/tb-more-actions.png)\) icon for the unpublished themes contains the following options:

    -   Duplicate
    -   Delete
    -   Add alternate color palette
    -   Publish
3.  Select Editor page view and choose the theme you want to edit from the Theme drop-down list. In the Editor page view, you can see only the theme that you select.

    ![Select a theme from the Theme drop-down list.](../image/tb-select-theme-editor-view.png "Select a theme from the Theme drop-down list")

    **Note:** When you select the theme you want to work on, verify that you selected the correct scope for the theme from the application scope picker.

    ![Application scope picker.](../image/tb-scope-picker.png "Application Scope Picker")

4.  Review and update the Global styles, as needed.

    ![Review global styles.](../image/tb-global-styles.png "Review global styles")

    **Note:** The following style records are generated with your theme:

    -   **Your brand palette**: Update the interface colors for your brand.
    -   **Logo**: Update the logo. You can upload the logo during the theme application either from imagery or the overview page. For more information, see [Upload a logo while publishing a theme with Theme Builder](tb-upload-logo.md).
    -   **Font Family**: Update the fonts applied globally to your experience. The fonts are used in headlines, titles, subtitles, body text, and captions.

        **Note:** If you prefer to customize your font, see [Create a Next Experience style](create-next-experience-style.md). After you save your customized font type and refresh the page, the new font appears as `Custom Font`. If you delete the custom font from your theme record, the font reverts to `Source Sans Pro` as the default.

    -   **Shape**: Update the corner shapes of on-screen components.

        **Note:** If you prefer to customize your shape, see [Create a Next Experience style](create-next-experience-style.md). After you save your customized shape and refresh the page, the new shape appears as `Mixed`. This custom value is also displayed in the **Component Styles** tab, where you can edit the custom value.

    1.  To change the auto-generated UI colors for more in-depth editing, select the Color palette icon ![](../image/tb-color-palette-icon.png) from the Global styles color panel. Use the drop-down list next to each UI element to access the color options.

        **Note:** After you have saved changes to any of the color hooks, a Remove override symbol appears. Select the Remove override symbol to revert your changes back to the original auto-generated colors.

        ![Remove override symbol.](../image/tb-color-undo.png)

5.  To preview your theme before publishing it to your instance, select the **Experience preview** tab.

    ![Experience preview tab.](../image/tb-exp-preview-tab.png)

    Select the experience that you want to preview from the Experience drop-down list.

    ![Experience drop-down.](../image/tb-experience-preview-dropdown.png)

    An actual live instance appears with all the theme selections applied. You can preview it before implementing the selected themes on the actual instance.

    **Note:** Select the Open in new tab icon ![](../image/tb-icon-open-new-tab.png) to open the experience in a new tab. You can see how your unpublished theme interacts with your selected experience.

    ![Preview of your experience with theme applied.](../image/tb-preview-before-applying-theme.png "Preview of your experience with theme applied")

    **Note:** For published themes, data in the Experience preview is live data. The changes that you make in the preview are reflected on your instance.

6.  Publish your theme.

    For more information, see [Publish your themes with Theme Builder](tb-apply-theme.md).


-   **[Core styles, colors, variants, and alternate color palettes](../reference/difference-themes-variants.md)**  
You can tailor the look and feel of the Next Experience UI for different users by configuring the core styles, variants, and alternate color palettes.
-   **[Add an alternate color palette](tb-edit-color-palette.md)**  
Customize a Theme Builder theme by creating an alternate color palette for the theme and publishing it to your instance.
-   **[Preview components](tb-preview-components.md)**  
As you’re creating or managing your theme, you can preview the components available for inclusion on your instance.
-   **[Edit components](tb-edit-components.md)**  
Edit Theme Builder individual components to better suit your brand and to meet accessibility compliance standards. The theme hooks that you can edit are specific to each type of component.
-   **[Working with Image styles](../concept/working-with-image-styles.md)**  
Image styles enable you to experiment with different color schemes for illustrations and replace default illustrations with your own custom images. The Image styles feature provides flexibility in customizing the visual elements of your theme.

**Parent Topic:**[Configuring Next Experience with Theme Builder](configuring-next-experience-with-theme-builder.md)

