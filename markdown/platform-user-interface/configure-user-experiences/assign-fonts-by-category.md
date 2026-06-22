---
title: Assign fonts by component category
description: Assign fonts to specific component categories to create a clearer visual hierarchy and ensure consistent typography across related UI elements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/assign-fonts-by-category.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Global styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Assign fonts by component category

Assign fonts to specific component categories to create a clearer visual hierarchy and ensure consistent typography across related UI elements.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/granular-admin-roles.md).

## About this task

Font assignments at the category level override broader defaults. Font size is managed separately in the **Sizes** tab and isn’t changed when assigning fonts by category. For information on editing font size, see [Edit font size](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/edit-font-size.md).

**Note:** Changing the font at the category level does not affect individual components that have their own font settings.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page appears in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    \[Omitted image "tb-editor-page-list.png"\] Alt text: Page drop-down list with Editor selected.

3.  From the Theme drop-down list, select the theme that you want to edit.

    The **Global styles** tab opens automatically with the Overview panel displayed.

    \[Omitted image "tb-editor-page-view.png"\] Alt text: Example view of the Editor page.

4.  From the Global styles Overview panel, navigate to Typography and select the **Fonts** tab.

    Typography is split into Fonts and Sizes, with font assignments managed in the **Fonts** tab.

    \[Omitted image "tb-typography-panel-fonts.png"\] Alt text: Typography with Fonts selected.

5.  Expand a component category.

    Each category displays its current font family, font face, and text transform settings.

6.  For the selected category, choose a font family.

    Select from available platform fonts or previously uploaded custom fonts. You can also [Upload a custom font to your theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/upload-custom-font.md) directly from the font selector.

7.  Select **Save**.

    **Note:** After you save changes to a typography option, a Remove override icon \[Omitted image "undo-top-outline-24.svg"\] appears. Use Remove override to revert the option to its original default value.

8.  Adjust the font face or text transform for the category.

9.  Select **Save**.

10. Use the available views to validate typography at different levels of detail.

    Switch between Abstract UI, Experiences, and Categories views to confirm that the category-wide font assignment is applied as expected across related components.


## Result

Theme Builder automatically saves your theme record.

If your theme is published, your font edits are visible to users who have your theme applied on refresh. For information on publishing your theme, see [Publish your themes with Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/tb-apply-theme.md).

**Parent Topic:**[Working with Global styles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/working-with-global-styles.md)

