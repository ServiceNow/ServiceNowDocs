---
title: Adjust a component to meet accessibility standards
description: Adjust a component to meet the Web Content Accessibility Guidelines \(WCAG\) 2.1. When you're editing a component in Theme Builder and see a warning symbol, that indicates that the component doesn't conform with the guidelines for color contrast.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Edit components, Component styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Adjust a component to meet accessibility standards

Adjust a component to meet the Web Content Accessibility Guidelines \(WCAG\) 2.1. When you're editing a component in Theme Builder and see a warning symbol, that indicates that the component doesn't conform with the guidelines for color contrast.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see Granular admin roles.

## About this task

When you're editing a component in Theme Builder, you may encounter a warning symbol \(![Accessibility error](../image/tb-accessibility-icon.png)\), which indicates that the component doesn't comply with the Web Content Accessibility Guidelines \(WCAG\) 2.1 for color contrast. The WCAG 2.1 contrast ratio that Theme Builder targets for content and UI variables is 3:1. This ratio determines the contrasts between brighter and darker screen colors and how they relate to the user interface. The first digit shows the level of bright colors, and the second digit shows the relative level of dark colors. The 3:1 threshold provides optimal visibility to visually challenged users. For more information, see the [W3C Recommendation site for WCAG 2.1](https://www.w3.org/TR/WCAG21/).

The total number of accessibility violations are indicated on the red numbered badge \(![Accessibility inspector numbered badge.](../image/tb-a11y-inspector-badge.png)\) alongside the Accessibility inspector panel.

## Procedure

1.  From the Editor page, access the accessibility violations in one of the two ways listed in the following table.

<table id="choicetable_php_1vv_2dc"><thead><tr><th align="left" id="d115137e98">

Option

</th><th align="left" id="d115137e101">

Description

</th></tr></thead><tbody><tr><td id="d115137e107">

**From Accessibility inspector**

</td><td>

1.  Select the Accessibility inspector icon ![](../image/tb-accessibility-inspector-icon.png) to display a list of components with accessibility errors. A red badge displays the number of accessibility issues within your theme.
2.  Select the Accessibility warning ![Accessibility warning.](../image/tb-accessibility-icon.png) symbol to view a description of the warning for the component state you want to improve.
3.  Select the pencil icon ![](../../workspace/image/pencil-icon.png)next to the component state that you want to improve.

**Note:** The Component Editor page appears and the configurable style panel displays the editable hooks available for the selected component.

</td></tr><tr><td id="d115137e146">

**From the Component styles menu**

</td><td>

1.  Select the **Editing** tab.

![Component styles Editing tab.](../image/tb-editing-tab.png)

2.  Select a component that displays the accessibility warning symbol.

![Accessibility warning](../image/tb-accessibility.png)

3.  From the configurable style panel, select the accessibility warning symbol to view a description of the warning.

![Description of accessibility warning.](../image/tb-accessibility-warning.png)

4.  As indicated in the warning message, you can select the pencil icon ![](../../workspace/image/pencil-icon.png) to improve the contrast issue.

**Note:** The Component Editor page appears and the configurable style panel displays the editable hooks that are available for the selected component.

</td></tr></tbody>
</table>2.  Select the accessibility warning symbol in the Component Editor to obtain more information for fixing the issue.

    ![Accessibility warning](../image/tb-accessibility-warning-text.png)

3.  Select from the link in the warning to fix the contrast issue.

    The color picker opens.

    **Note:** You can select the Hide inaccessible choices slider within the color picker to limit the color choices to those colors identified as accessible, based on Web Content Accessibility Guidelines \(WCAG\) guidelines.

4.  Select the undo symbol to revert your changes back to the original color, if needed.

    ![Undo color changes](../image/tb-color-undo.png)

5.  When you complete your changes and the accessibility warning symbol is no longer visible, select **Save changes**.

    For example, after you select a color that passes the contrast ratio violation, the warning symbol turns green in the color picker.


