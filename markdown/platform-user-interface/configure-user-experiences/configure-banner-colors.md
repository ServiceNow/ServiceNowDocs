---
title: Configure colors for banner illustrations
description: Configure and control the colors automatically applied to banner illustrations to keep your visual experience engaging while maintaining brand recognition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/configure-banner-colors.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Banner illustrations, Image styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure colors for banner illustrations

Configure and control the colors automatically applied to banner illustrations to keep your visual experience engaging while maintaining brand recognition.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see .

## About this task

As a category, all banner illustrations share color hook mappings. As a result, the colors that you apply to one banner illustration type are also applied to the entire banner illustration category.

**Important:** Configuring banner illustration colors applies to Workspaces and isn’t supported in the Core UI.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page opens in a new tab and is displayed in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    \[Omitted image "tb-editor-page-view.png"\] Alt text: Example view of the Editor page.

3.  From the Theme drop-down list, select the theme that you want to edit.

4.  Select the **Image styles** tab from the general styles panel and expand **Banners**.

    The banner illustrations available for editing are listed on the main stage.

5.  Select any banner illustration type from the main stage.

    **Note:** Customizing the colors of any banner illustration type applies the color change to the entire banner category, regardless of which type you select.

    The property panel opens automatically.

    \[Omitted image "tb-banner-property-panel.png"\] Alt text: Image styles tab selected with banner illustrations listed on main stage and property panel opened.

6.  From the property panel, select the **Colors** tab.

    **Note:** The number of leading or supporting colors differs depending on the illustration category. For example, banner illustrations have one leading color, while card illustrations have three leading colors. Leading colors are the main colors in the illustration and supporting colors are accents. They’re listed from most prominent to least.

    \[Omitted image "tb-property-panel-colors.png"\] Alt text: Property panel with Colors tab selected.

7.  Select an image color to edit the color using the Color picker.

    \[Omitted image "tb-color-picker.png"\] Alt text: Color picker.

    **Note:** By default, the My Colors tab shows all available colors for the illustration. You can also use the Custom tab to select a new color.

8.  When you have completed your changes, select **Save changes**.

    **Note:** After you have saved changes to any of the color hooks, a Remove override symbol appears. The Remove override symbol enables you to revert your color changes back to the original auto-generated colors.

    \[Omitted image "tb-color-undo.png"\] Alt text: Remove override symbol.


## Result

The new colors are applied to all banner illustration types.

If your theme is published, your banner illustration edits are visible to users who have your theme applied on refresh. For information about publishing themes, see [Publish your themes with Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/tb-apply-theme.md).

**Parent Topic:**[Banner illustrations in Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/banners-in-tb.md)

