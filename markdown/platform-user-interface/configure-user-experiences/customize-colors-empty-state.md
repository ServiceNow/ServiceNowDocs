---
title: Customize the colors for empty state illustrations and custom images
description: Customize and control the colors automatically applied to empty state illustrations and your custom images to keep your visual experience engaging while maintaining brand recognition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-user-interface/configure-user-experiences/customize-colors-empty-state.html
release: yokohama
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-03-19"
reading_time_minutes: 2
keywords: [theme builder, customize colors, empty state illustrations]
breadcrumb: [Working with Image styles, Manage or edit a theme with Theme Builder, Configuring Next Experience with Theme Builder, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Customize the colors for empty state illustrations and custom images

Customize and control the colors automatically applied to empty state illustrations and your custom images to keep your visual experience engaging while maintaining brand recognition.

## Before you begin

Before you can edit the colors of your custom image, you must append two design tokens to your image code before uploading the image to Theme Builder. For information, see [Override empty state illustrations with custom images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-user-interface/configure-user-experiences/override-empty-state-illustrations.md).

Role required: admin

## About this task

As a category, all empty state illustrations share color hook mappings. As a result, the colors that you apply to one empty state illustration type are also applied to the entire empty state illustration category.

**Important:** Customization of empty state illustration colors applies to Workspaces and is not supported in the Core UI.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Themes** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    \[Omitted image "tb-editor-page-view.png"\] Alt text: Example view of the Editor page.

3.  From the Theme drop-down list, select the theme that you want to edit.

4.  Select the **Image styles** tab from the general styles panel.

    The empty state illustrations available for editing are displayed on the main stage and grouped by type.

    \[Omitted image "tb-image-styles-opened.png"\] Alt text: Image styles tab selected with empty state illustrations listed on main stage and property panel opened.

5.  Select any empty state illustration type from the main stage.

    **Note:** Customizing the colors of any empty state illustration type will apply the color change to the entire empty state category, regardless of which type you select.

    The property panel opens automatically.

6.  From the property panel, select the **Colors** tab.

    \[Omitted image "tb-property-panel-colors.png"\] Alt text: Property panel with Colors tab selected.

7.  Select an image color to edit the color using the Color picker.

    \[Omitted image "tb-color-picker.png"\] Alt text: Color picker.

    **Note:** By default, the My Colors tab shows all of the available colors for the illustration. You can also use the Custom tab to select a new color.

8.  When you have completed your changes, select **Save changes**.

    **Note:** After you have saved changes to any of the color hooks, a Remove override symbol appears. The Remove override symbol enables you to revert your color changes back to the original auto-generated colors.

    \[Omitted image "tb-color-undo.png"\] Alt text: Remove override symbol.


## Result

The new colors are applied to all empty state illustration types including any custom images you've previously uploaded with design tokens applied.

If your theme is published, your empty state illustration edits are visible to users who have your theme applied upon refresh. For information about publishing themes, see [Publish your themes with Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-user-interface/configure-user-experiences/tb-apply-theme.md).

**Parent Topic:**[Working with Image styles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-user-interface/configure-user-experiences/working-with-image-styles.md)

