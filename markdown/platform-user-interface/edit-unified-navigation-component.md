---
title: Align with your brand by using the Unified Navigation component
description: Align your experience more closely with your brand by editing the Unified Navigation component and its subcomponents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Edit components, Component styles, Manage or edit a theme, Configuring Next Experience with Theme Builder, Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Align with your brand by using the Unified Navigation component

Align your experience more closely with your brand by editing the Unified Navigation component and its subcomponents.

## Before you begin

Role required: ui\_builder\_admin

For information on granular roles, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## About this task

The Unified Navigation component is made up of several subcomponents that you must style individually. In the Theme Builder 5.0 release, editing of the Unified Navigation is limited to the header and menus, although some styling may apply to all aspects of the Unified Navigation component and subcomponents.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Theme Builder**.

2.  From the Page drop-down list, select the Editor page view.

    ![View of the Editor page.](../image/tb-editor-page-view.png "Editor page view")

3.  From the Theme drop-down list, select the theme that you want to edit the Unified Navigation component for.

4.  Select the **Component styles** tab.

5.  Select the **Editing** tab.

    ![Component styles Editing tab.](../image/tb-editing-tab.png)

6.  Filter the list to view the Unified Navigation component.

    1.  Select the Filter icon \(![](../image/tb-filter-icon.png)\).

    2.  Expand the Navigation category and select the Unified Navigation component.

        ![Unified Navigation component selected from filter list.](../image/tb-filter-list-unified-nav.png "Unified Navigation component")

7.  Access the Component Editor where you can style various aspects of the Unified Navigation component by using one of the two ways listed:

    -   Double-click the Unified Navigation component tile.
    -   From the Unified Navigation editing panel, select **Style subcomponents**.
    ![Unified Navigation component editing panel including the Style subcomponents button.](../image/tb-unified-nav-editing-panel.png "Unified Navigation editing panel")

8.  Select the **Header** or **Menu** tile to open the configurable styles panel where you can edit the available theme hooks.

    The editable theme hooks that are available depend on the type of subcomponent that you have selected. For example, if you select a Header subcomponent, you can edit the background colors for the Header. If you select a Menu subcomponent, you can edit the background, text, and icon colors.

    **Note:** After you save the changes to any of the color hooks, a Remove override symbol appears. Select the Remove override symbol to revert your changes to the original auto-generated colors.

    ![Remove override symbol.](../image/tb-color-undo.png)

9.  Double-click the **Header** or **Menu** tile or select **Style subcomponents** to edit the available subcomponents.

    A Subcomponent is a smaller piece of a larger component. For example, the Unified Navigation Header or Menu subcomponent is a smaller piece of the Unified Navigation component. An interaction describes the different ways the component or subcomponent behaves. For example, the Default or Hover interactions are interactions of the Menu Trigger subcomponent.

    ![Unified Navigation Header subcomponent editing option.](../image/tb-unified-nav-header.png "Unified Navigation Header subcomponent editing options")

10. Continue editing each subcomponent and interaction until you complete styling the Unified Navigation component.

    For example, after you double-click the Header Menu Trigger subcomponent, the interactions of the Menu Trigger are available for styling. Likewise, if you double-click the Menu subcomponent, the subcomponents and interactions for each menu are available.

    **Note:** The canvas color feature automatically applies the background color from the parent subcomponent.

11. When editing certain subcomponents, such as the Menu, choose which configuration you want to preview.

    For example, when editing the Menu subcomponent, after you select **Component config**, you can select the specific menu that you want to edit from the Type drop-down list. After you select the desired menu, all available subcomponents for that particular menu are listed.

    ![Component config menu with the History menu selected.](../image/tb-component-config.png "Component config menu")

12. To return to a previous component editing screen, select one of the breadcrumb links.

    ![Component editing breadcrumb navigation.](../image/tb-un-component-breadcrumb.png "Component editing breadcrumb navigation")


## Result

If your theme is published, your Unified Navigation edits will be visible to users who have your theme applied upon refresh. For information on publishing your theme, see [Publish your themes with Theme Builder](tb-apply-theme.md).

