---
title: Adjust a component to meet accessibility standards
description: Adjust a component to meet the Web Content Accessibility Guidelines \(WCAG\) 2.1. When you're editing a component in Theme Builder and see a warning symbol, that indicates that the component doesn't conform with the guidelines for color contrast.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/tb-adjust-component-wcag.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Edit components, Component styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Adjust a component to meet accessibility standards

Adjust a component to meet the Web Content Accessibility Guidelines \(WCAG\) 2.1. When you're editing a component in Theme Builder and see a warning symbol, that indicates that the component doesn't conform with the guidelines for color contrast.

## Before you begin

Role required: admin

## About this task

When you're editing a component in Theme Builder, you may encounter a warning symbol \(\[Omitted image "tb-accessibility-icon.png"\] Alt text: Accessibility error\), which indicates that the component doesn't comply with the Web Content Accessibility Guidelines \(WCAG\) 2.1 for color contrast. The WCAG 2.1 contrast ratio that Theme Builder targets for content and UI variables is 3:1. This ratio determines the contrasts between brighter and darker screen colors and how they relate to the user interface. The first digit shows the level of bright colors, and the second digit shows the relative level of dark colors. The 3:1 threshold provides optimal visibility to visually challenged users. For more information, see the [W3C Recommendation site for WCAG 2.1](https://www.w3.org/TR/WCAG21/).

The total number of accessibility violations are indicated on the red numbered badge \(\[Omitted image "tb-a11y-inspector-badge.png"\] Alt text: Accessibility inspector badge.\) alongside the Accessibility inspector panel.

## Procedure

1.  From the Editor page, access the accessibility violations in one of the two ways listed in the following table.

<table id="choicetable_php_1vv_2dc"><thead><tr><th align="left" id="d112049e91">

Option

</th><th align="left" id="d112049e94">

Description

</th></tr></thead><tbody><tr><td id="d112049e100">

**From Accessibility inspector**

</td><td>

1.  Select the Accessibility inspector icon \[Omitted image "tb-accessibility-inspector-icon.png"\] Alt text: to display a list of components with accessibility errors. A red badge displays the number of accessibility issues within your theme.
2.  Select the Accessibility warning \[Omitted image "tb-accessibility-icon.png"\] Alt text: Accessibility warning. symbol to view a description of the warning for the component state you want to improve.
3.  Select the pencil icon \[Omitted image "pencil-icon.png"\] Alt text:next to the component state that you want to improve.

**Note:** The Component Editor page appears and the configurable style panel displays the editable hooks available for the selected component.

</td></tr><tr><td id="d112049e139">

**From the Component styles menu**

</td><td>

1.  Select the **Editing** tab.

\[Omitted image "tb-editing-tab.png"\] Alt text: Component styles Editing tab.

2.  Select a component that displays the accessibility warning symbol.

\[Omitted image "tb-accessibility.png"\] Alt text: Accessibility warning

3.  From the configurable style panel, select the accessibility warning symbol to view a description of the warning.

\[Omitted image "tb-accessibility-warning.png"\] Alt text: Description of accessibility warning.

4.  As indicated in the warning message, you can select the pencil icon \[Omitted image "pencil-icon.png"\] Alt text: to improve the contrast issue.

**Note:** The Component Editor page appears and the configurable style panel displays the editable hooks that are available for the selected component.

</td></tr></tbody>
</table>2.  Select the accessibility warning symbol in the Component Editor to obtain more information for fixing the issue.

    \[Omitted image "tb-accessibility-warning-text.png"\] Alt text: Accessibility warning

3.  Select from the link in the warning to fix the contrast issue.

    The color picker opens.

    **Note:** You can select the Hide inaccessible choices slider within the color picker to limit the color choices to those colors identified as accessible, based on Web Content Accessibility Guidelines \(WCAG\) guidelines.

4.  Select the undo symbol to revert your changes back to the original color, if needed.

    \[Omitted image "tb-color-undo.png"\] Alt text: Undo color changes

5.  When you complete your changes and the accessibility warning symbol is no longer visible, select **Save changes**.

    For example, after you select a color that passes the contrast ratio violation, the warning symbol turns green in the color picker.


