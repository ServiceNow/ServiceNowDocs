---
title: Edit font size
description: Adjust font sizes at the theme or component category level to refine default or custom fonts and keep your brand consistent across all experiences.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/edit-font-size.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Global styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Edit font size

Adjust font sizes at the theme or component category level to refine default or custom fonts and keep your brand consistent across all experiences.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/granular-admin-roles.md).

## About this task

The global base font size acts as the foundation for all other typography sizes. Increasing or decreasing the base value scales every size category proportionally, preserving the relative differences between sizes.

When you edit font sizes by category, you change which size tier the category uses, not the size values themselves. This approach enables you to adjust the relative emphasis of different types of text while keeping size values consistent and reusable across the theme.

Font sizing changes in Theme Builder also apply to web embeddables using your theme. This approach ensures consistent typography across ServiceNow and any embedded components on external sites. If you use embeddables, preview your theme to confirm sizes render as expected.

**Important:** Changing the font size may cause components to appear distorted or lead to unexpected issues with how text is displayed.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page appears in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    \[Omitted image "tb-editor-page-list.png"\] Alt text: Page drop-down list with Editor selected.

3.  From the Theme drop-down list, select the theme that you want to edit.

    The **Global styles** tab opens automatically with the Overview panel displayed.

    \[Omitted image "tb-editor-page-view.png"\] Alt text: Example view of the Editor page.

4.  From the Global styles Overview panel, navigate to Typography and select the **Sizes** tab.

    Typography is split into Fonts and Sizes, with size assignments managed in the **Sizes** tab.

    \[Omitted image "tb-typography-sizes.png"\] Alt text: Typography with Sizes selected.

5.  Edit global font sizes.

<table id="choicetable_o4q_hfq_g3c"><tbody><tr><td id="d45066e179">

**Edit global base font**

</td><td>

Under Global sizes, locate Base font size and enter a new size value.

</td></tr><tr><td id="d45066e188">

**Edit individual global font sizes**

</td><td>

Under Global sizes, expand Base font size. Locate the individual size that you want to change and enter a new pixel value.

</td></tr></tbody>
</table>6.  To revert the font sizes to their original default size, select the Remove override icon \[Omitted image "undo-top-outline-24.svg"\].

7.  Edit fonts by component category.

    1.  Navigate to the Categories by size section.

    2.  Locate and expand the category you want to edit.

    3.  Drag the category to a different size tier.

        The category adopts the size of the tier it is dropped into. Dragging a category changes which size it uses, not the size value itself.

    4.  To revert the category back to its original default size, select the Remove override icon \[Omitted image "undo-top-outline-24.svg"\].

8.  Use the available views to validate typography at different levels of detail.

    Switch between Abstract UI, Experiences, and Categories views to confirm that the category-wide font assignment is applied as expected.


## Result

Theme Builder automatically saves your theme record.

If your theme is published, your font sizing edits are visible to users who have your theme applied on refresh. For information on publishing your theme, see [Publish your themes with Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/tb-apply-theme.md).

**Parent Topic:**[Working with Global styles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/working-with-global-styles.md)

