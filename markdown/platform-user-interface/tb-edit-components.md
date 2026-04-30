---
title: Edit components
description: Edit Theme Builder individual components to better suit your brand and to meet accessibility compliance standards. The theme hooks that you can edit are specific to each type of component.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [edit individual components, theme hooks, accessibility compliance standards, change components]
breadcrumb: [Manage or edit a theme with Theme Builder, Configuring Next Experience with Theme Builder, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Edit components

Edit Theme Builder individual components to better suit your brand and to meet accessibility compliance standards. The theme hooks that you can edit are specific to each type of component.

## Before you begin

Role required: admin

## About this task

The components that you can edit in Theme Builder were created in the ServiceNow AI Platform Design System. For more information, see [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?releases[]=vancouver&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades) on the ServiceNow Developer Site.

The total number of accessibility violations are indicated on the red numbered badge ![Accessibility inspector numbered badge](../image/tb-a11y-inspector-badge.png) alongside the Accessibility inspector panel.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Themes** &gt; **Theme Builder**.

    The Theme Builder landing page displays in the Home page view.

2.  From the page view drop-down menu, select the Editor page view.

    ![Example view of the Editor page.](../image/tb-editor-page-view.png "Editor page view")

3.  From the Theme drop-down menu, select the theme that you want to edit components for.

4.  From the Editor page view, select the **Component styles** tab.

    The component styles are graphically listed.

    ![Component styles.](../image/tb-component-styles-list.png)

5.  Select the **Editing** tab.

    ![Component styles Editing tab.](../image/tb-editing-tab.png)

    **Note:** The components that can be edited are displayed. For information on how to filter the list of components to locate the component you want to edit, see [Preview components](tb-preview-components.md).

6.  Select the component that you want to edit.

    When you’re looking at the components listed in the Editing page, notice that some components may display the following symbol.

    ![Accessibility error.](../image/tb-accessibility.png)

    **Note:** The accessibility warning symbol indicates that the color contrast of the selected component doesn’t adhere to WCAG 2.1 accessibility standards for color contrast. For more information, see [Adjust a component to meet accessibility standards](tb-adjust-component-wcag.md).

7.  In the configurable style panel, edit the theme hooks that are available for the selected component as needed.



    ![Configurable styles panel.](../image/tb-configurable-styles-panel.png)

    The editable theme hooks that are available depend on the type of component you selected. For example, if you select a Badge component, you can edit the colors and accessibility hooks for the badge. If you select a Text link component, you can edit the base color and accessibility hooks.

    **Note:** After you update the component-specific hooks, any changes that you make to the global style won't update the component styles because component-specific styles take precedence over globally defined styles.

8.  If you select a color to be edited, the color picker opens.

    ![Color picker.](../image/tb-color-picker.png "Color picker")

    **Note:** By default, the color picker shows all the available colors for the component. You can select the Hide inaccessible choices slider to limit the color choices to those colors identified as accessible, based on the current Web Content Accessibility Guidelines \(WCAG\) guidelines.

9.  When you have completed your changes, select **Save changes**.


