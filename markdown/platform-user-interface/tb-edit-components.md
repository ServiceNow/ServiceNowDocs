---
title: Edit components
description: Edit Theme Builder individual components to better suit your brand and to support accessibility requirements. Each component type supports specific customization options called theme hooks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/tb-edit-components.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [edit individual components, theme hooks, accessibility compliance standards, change components]
breadcrumb: [Component styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Edit components

Edit Theme Builder individual components to better suit your brand and to support accessibility requirements. Each component type supports specific customization options called theme hooks.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

## About this task

The components available in Theme Builder were created in the ServiceNow AI Platform Design System. When you edit component-specific theme hooks, those changes take precedence over globally defined styles.

For more information, see [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?releases[]=vancouver&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades) on the ServiceNow Developer Site.

For instructions on editing the Unified Navigation component, see [Align with your brand by using the Unified Navigation component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/edit-unified-navigation-component.md).

The total number of accessibility violations is indicated on the red numbered badge icon \[Omitted image "tb-a11y-inspector-badge.png"\] Alt text: Accessibility inspector badge. alongside the Accessibility inspector panel. You can review and fix these violations as part of this task. See [Adjust a component to meet accessibility standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/tb-adjust-component-wcag.md) for guidance.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

    The Theme Builder landing page displays in the Home page view.

2.  From the Page drop-down list, select **Editor**.

    \[Omitted image "tb-editor-page-list.png"\] Alt text: Page drop-down list with Editor selected.

3.  From the Theme drop-down list, select the theme to edit.

4.  From the Editor page, select **Component styles**.

    The component styles are graphically listed.

    \[Omitted image "tb-component-styles-list.png"\] Alt text: Component styles.

5.  Select **Editing** to switch from the Preview view to the editable view.

    \[Omitted image "tb-editing-tab.png"\] Alt text: Component styles Editing tab.

    The component list displays, organized by category.

6.  Locate the component to edit by scrolling through the categories or using the filter icon \[Omitted image "tb-icon-filter.png"\] Alt text:.

    Some components display an accessibility warning symbol.

    \[Omitted image "tb-accessibility.png"\] Alt text: Accessibility error.

    **Note:** The accessibility warning symbol indicates that the color contrast of the selected component may not meet color contrast requirements. For information on resolving color contrast issues, see [Adjust a component to meet accessibility standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/tb-adjust-component-wcag.md).

7.  Select the component to open the Configurable Style panel.

    \[Omitted image "tb-configurable-styles-panel.png"\] Alt text: Configurable style panel.

    The Configurable Style panel displays all available theme hooks for that component. The type and number of theme hooks vary by component. For example, if you select a Badge component, you can edit the colors and accessibility hooks for the badge. If you select a Text link component, you can edit the base color and accessibility hooks.

8.  If the component has editable color hooks, select the color to change.

    The color picker opens.

    \[Omitted image "tb-color-picker.png"\] Alt text: Color picker.

    **Note:** By default, the color picker shows all the available colors for the component. Use the **My Colors** tab to select from a predefined list of colors or choose the **Custom** tab to select the specific color model that you prefer: HEX, RGB, or HSL.

9.  When you have completed your color changes, select **Save changes**.

10. If the component has shape properties, use the selector modals to adjust border width and corner radius.

11. When you have completed your shape changes, select **Save changes**.

12. If the component has editable font properties, select the font family or font face to edit.

    \[Omitted image "tb-component-font-modal.png"\] Alt text: Edit font family selector modal.

    **Note:** If you have uploaded a custom font, it appears in the modal for selection. You can also upload a custom font directly from the selector modal making it available throughout your theme. For more information, see [Upload a custom font to your theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/upload-custom-font.md).

13. When you have completed your font changes, select **Save changes**.

14. Select the undo icon \[Omitted image "undo-top-outline-24.svg"\] to revert your font to Source Sans Pro, if needed.

15. Access the Component Editor for deeper styling where you can style various aspects of a component by using one of the two ways listed:

    -   Select the component tile twice.
    -   Select either the **Style interactions**, **Style subcomponents**, or **Style variants** button within the configurable styles panel, depending on what is available for that specific component.

        **Note:** Not all components contain editable parts. These buttons only appear if they're available for your selected component.

        \[Omitted image "tb-component-editor-page.png"\] Alt text: Component editor page.

16. From the Component Editor, choose the interaction, variant, or subcomponent of the selected component.

17. Edit the available theme hooks.

    **Note:** After saving changes to a color hook, a Remove override symbol appears. The Remove override symbol reverts color changes to the original auto-generated colors.

    \[Omitted image "tb-color-undo.png"\] Alt text: Remove override symbol.

18. Use the navigational breadcrumb path to return to the Component Styles section or the component overview.

    \[Omitted image "tb-component-breadcrumb.png"\] Alt text: Component editing breadcrumb navigation.


## Result

Component edits are saved to the selected theme.

If your theme is published, your component edits are visible to users who have your theme applied on refresh. For information on publishing your theme, see [Publish your themes with Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/tb-apply-theme.md).

