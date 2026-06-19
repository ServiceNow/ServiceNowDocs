---
title: Edit components
description: Edit Theme Builder individual components to better suit your brand and to meet accessibility conformance standards. The theme hooks that you can edit are specific to each type of component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/tb-edit-components.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [edit individual components, theme hooks, accessibility compliance standards, change components]
breadcrumb: [Component styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Edit components

Edit Theme Builder individual components to better suit your brand and to meet accessibility conformance standards. The theme hooks that you can edit are specific to each type of component.

## Before you begin

Role required: admin

## About this task

The components that you can edit in Theme Builder were created in the ServiceNow AI Platform Design System. For more information, see [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?releases[]=vancouver&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades) on the ServiceNow Developer Site.

For instructions on editing the Unified Navigation component, see [Align with your brand by using the Unified Navigation component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/edit-unified-navigation-component.md).

The total number of accessibility violations is indicated on the red numbered badge icon \[Omitted image "tb-a11y-inspector-badge.png"\] Alt text: Accessibility inspector badge. alongside the Accessibility inspector panel.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page displays in the Home page view.

2.  Use the Page drop-down list to select the Editor page view.

    \[Omitted image "tb-editor-page-list.png"\] Alt text: Page drop-down list with Editor selected.

3.  From the Theme drop-down list, select the theme that you want to edit components for.

4.  From the Editor page view, select the **Component styles** tab.

    The component styles are graphically listed.

    \[Omitted image "tb-component-styles-list.png"\] Alt text: Component styles.

5.  Select the **Editing** tab.

    \[Omitted image "tb-editing-tab.png"\] Alt text: Component styles Editing tab.

    **Note:** The components that can be edited are displayed. For information on how to filter the list of components to locate the component you want to edit, see [Preview components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/tb-preview-components.md).

6.  Select the component that you want to edit to access the Configurable Style panel.

    When you’re looking at the components listed in the Editing page, notice that some components may display the following symbol.

    \[Omitted image "tb-accessibility.png"\] Alt text: Accessibility error.

    **Note:** The accessibility warning symbol indicates that the color contrast of the selected component doesn’t adhere to Web Content Accessibility Guidelines \(WCAG\) 2.1 accessibility standards for color contrast. For information on editing components with accessibility violations, see [Adjust a component to meet accessibility standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/tb-adjust-component-wcag.md).

7.  From the Configurable style panel, edit the theme hooks that are available for the selected component, as needed.

    \[Omitted image "tb-configurable-styles-panel.png"\] Alt text: Configurable style panel.

    The editable theme hooks that are available depend on the type of component you selected. For example, if you select a Badge component, you can edit the colors and accessibility hooks for the badge. If you select a Text link component, you can edit the base color and accessibility hooks.

    **Note:** After you update the component-specific hooks, any changes that you make from global styles won't affect your component edits. Component-specific styles take precedence over globally defined styles.

8.  If you select a color to be edited, the color picker opens.

    \[Omitted image "tb-color-picker.png"\] Alt text: Color picker.

    **Note:** By default, the color picker shows all the available colors for the component. Use the **My Colors** tab to select from a predefined list of colors or choose the **Custom** tab to select the specific color model that you prefer: HEX, RGB, or HSL.

9.  When you have completed your color changes, select **Save changes**.

10. If you select a shape to be edited, use the selector modals to choose border width and corner radius.

11. When you have completed your shape changes, select **Save changes**.

12. If you select a font family or font face to be edited, the selector modal opens.

    \[Omitted image "tb-component-font-modal.png"\] Alt text: Edit font family selector modal.

    **Note:** If you have uploaded a custom font, it will appear in the modal for selection. You can also upload a custom font directly from the selector modal making it available for use throughout your theme. For more information, see [Upload a custom font to your theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/upload-custom-font.md).

13. When you have completed your font changes, select **Save changes**.

14. Select the undo icon \[Omitted image "undo-top-outline-24.svg"\] to revert your font to Source Sans Pro, if needed.

15. Access the Component Editor where you can style various aspects of a component by using one of the two ways listed:

    -   Double-click the component tile.
    -   Select either the **Style interactions**, **Style subcomponents**, or **Style variants** button within the configurable styles panel, depending on what is available for that specific component.

        **Note:** Not all components contain editable parts.

        \[Omitted image "tb-component-editor-page.png"\] Alt text: Component editor page.

16. From the Component Editor, choose the interaction, variant, or subcomponent of the selected component, then edit the available theme hooks.

    **Note:** After you save the changes to any of the color hooks, a Remove override symbol appears. The Remove override symbol enables you to revert your color changes back to the original auto-generated colors.

    \[Omitted image "tb-color-undo.png"\] Alt text: Remove override symbol.

17. Return to the Component Overview screen using the links within the navigational path.

    \[Omitted image "tb-component-breadcrumb.png"\] Alt text: Component editing breadcrumb navigation.


## Result

If your theme is published, your component edits are visible to users who have your theme applied on refresh. For information on publishing your theme, see [Publish your themes with Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/tb-apply-theme.md).

