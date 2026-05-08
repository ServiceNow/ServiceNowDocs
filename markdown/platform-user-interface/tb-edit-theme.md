---
title: Manage or edit a theme with Theme Builder
description: Customize and manage your theme and styling in a time and cost efficient way. After customizing, publish your new theme to either a web or mobile implementation of your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [customize theme, edit theme, manage theme, change theme]
breadcrumb: [Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Manage or edit a theme with Theme Builder

Customize and manage your theme and styling in a time and cost efficient way. After customizing, publish your new theme to either a web or mobile implementation of your instance.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see Granular admin roles.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

    ![Page menu.](../image/tb-home.png "Page menu")

2.  From the Home page view, select Manager page view to see all available themes.

    From the Manager page view, you have the choice of viewing existing themes in two ways. You can choose the Grid view or the List view.

    **Note:** In both the Grid and List views, your published and unpublished themes are grouped separately. The published themes are themes that appear in the user's theme preference. View your web and mobile themes by selecting either the **Web** or **Mobile** button.

    ![Grid view.](../image/tb-grid-view.png "Grid view")

    ![List view.](../image/tb-list-view.png "List view")

    Use the More actions icon ![](../image/tb-more-actions.png)on a published theme to access these options:

    -   Duplicate: creates a copy of the theme for reuse or modification.
    -   Delete: permanently removes the theme from your list.
    -   Add alternate color palette: applies a different color scheme to the theme for variation.
    -   Unpublish: removes the theme from active use without deleting it, so you can edit or republish later.
    -   Mark as default: sets the theme as the first option shown in the Next Experience Theme user preference. This option appears if the theme is not the current default theme.
    Use the More actions icon ![](../image/tb-more-actions.png)on a published theme with an alternate color palette defined to access these options:

    -   Edit group name: renames the theme group, which includes the base theme and all its alternate color palettes.
    -   Duplicate: creates a copy of the theme for reuse or modification.
    -   Delete: permanently removes the theme from your list.
    -   Unpublish: removes the theme from active use without deleting it, so you can edit or republish later.
    -   Mark as default: sets the theme as the first option shown in the Next Experience Theme user preference. This option appears if the theme is not the current default theme.
    Use the More actions icon ![](../image/tb-more-actions.png)on an unpublished theme to access these options:

    -   Duplicate: creates a copy of the theme for reuse or modification.
    -   Delete: permanently removes the theme from your list.
    -   Add alternate color palette: applies a different color scheme to the theme for variation.
    -   Publish: makes the theme available for use.
3.  Choose the theme you want to edit using one of the following ways.

<table id="choicetable_v1x_lnb_qfc"><thead><tr><th align="left" id="d51270e241">

Page

</th><th align="left" id="d51270e244">

Option

</th></tr></thead><tbody><tr><td id="d51270e250">

**Manager \(Grid view\)**

</td><td>

From the Published or Unpublished section, choose the theme you want to edit and select **Edit**.

</td></tr><tr><td id="d51270e262">

**Manager \(List view\)**

</td><td>

From the Published or Unpublished section, choose the theme you want to edit and select the pencil icon ![](../../workspace/image/pencil-icon.png).

</td></tr><tr><td id="d51270e276">

**Editor**

</td><td>

Choose the theme you want to edit from the Theme drop-down list.![Select a theme from the Theme drop-down list.](../image/tb-select-theme-editor-view.png "Select a theme from the Theme drop-down list")

</td></tr></tbody>
</table>    **Note:** When you select the theme you want to work on, verify that you selected the correct scope for the theme from the application scope picker.

    ![Application scope picker.](../image/tb-scope-picker.png "Application Scope Picker")

4.  Review and update the Global styles, as needed.

    ![Review global styles.](../image/tb-global-styles.png "Global styles overview")

    **Note:** The following style records are generated with your theme:

    -   **Your brand palette**: Update the interface colors for your brand. For more information, see [Edit your theme colors](edit-theme-colors.md).
    -   **Logo**: Update the logo. You can upload the logo during the theme application from the Overview page. For more information, see [Upload a new logo to your Theme Builder theme](tb-upload-logo.md).
    -   **Typography**: Update the fonts applied globally to your experience. The fonts are used in headlines, titles, subtitles, body text, and captions. For more information, see [Edit your default font](edit-font.md).
    -   **Shape**: Update the corner shapes of on-screen components. For more information, see [Edit corner shapes](edit-corner-shapes.md).
5.  Preview your theme before publishing.

    1.  Select the **Experiences** tab from the Global styles panel.

    2.  Select the experience that you want to preview from the Experience drop-down list.

    3.  Select the Open in new tab icon ![](../image/tb-icon-open-new-tab.png) to open the experience in a new tab.

        ![Global styles experience preview screen.](../image/tb-experience-preview-1.png "Experience preview")

        An actual live instance appears with all the theme selections applied. You can preview it before implementing the selected themes on the actual instance.

        **Note:** For published themes, data in the Experiences preview is live data. The changes that you make in the preview are reflected on your instance.

6.  Publish your theme.

    For more information, see [Publish your themes with Theme Builder](tb-apply-theme.md).


-   **[Core styles, colors, variants, and alternate color palettes](../reference/difference-themes-variants.md)**  
You can tailor the look and feel of the Next Experience UI for different users by configuring the core styles, variants, and alternate color palettes. Core styles define the base theme, variants support accessibility needs, and alternate color palettes provide cosmetic customization options for end users.
-   **[Add an alternate color palette](tb-edit-color-palette.md)**  
Customize a Theme Builder theme by creating an alternate color palette for the theme and publishing it to your instance.
-   **[Working with Global styles](../concept/working-with-global-styles.md)**  
Global styles enable you to edit and define core design elements like fonts, colors, and shapes that apply across your entire theme.
-   **[Working with Component styles](../concept/working-with-component-styles.md)**  
Component styles enable you to fine-tune the appearance of individual UI elements such as buttons, form controls, and navigation without affecting global theme settings. Use component styles when you need more granular control than what Global styles provide.
-   **[Working with Image styles](../concept/working-with-image-styles.md)**  
Image styles enable you to experiment with different color schemes for illustrations and replace default illustrations with your own custom images. The Image styles feature provides flexibility in customizing the visual elements of your theme.

**Parent Topic:**[Configuring Next Experience with Theme Builder](configuring-next-experience-with-theme-builder.md)

