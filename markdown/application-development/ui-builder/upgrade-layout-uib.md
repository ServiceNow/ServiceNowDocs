---
title: Upgrading layouts in UI Builder
description: Upgrade layouts created in Quebec and Rome to the new layout system.Upgrade your UI Builder pages to the new layout system.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Organize components in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Upgrading layouts in UI Builder

Upgrade layouts created in Quebec and Rome to the new layout system.

The UI Builder layout system was enhanced and updated in the San Diego release. This new layout system features a simplified content tree and a new styling panel for layout configuration and component styling. All newly created page variants use the new layout system. You have the option to upgrade to the new layout system for existing and custom pages.

The new layout system includes the following:

-   A simplified content tree
-   Improved styling panel for layout configuration and component styling
-   Low-code UI for configuring CSS [Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) and [Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout) layouts.
-   Enhanced UI for component styling
-   Updated layouts do not require slots

## Things to look for after upgrading layouts

Variants and pages are upgraded individually.

A page/variant is made up of a layout, components, and subcomponents, that are wrapped in a container within a layout with data resources, event bindings, and composition. Only the layout of your page is upgraded when upgrading to the new layout system, so there is no impact to your data, components, or component styling.

All slots in the old layout system are migrated during the upgrade process to the new layout. The upgrade process changes how the component containers are structured on your page.

While component styling is not impacted, there may not be a one-to-one style migration of how components were positioned. Complex pages can have visual misalignments that occur through the upgrade process as styles are merged from slots to containers. Some issues must be resolved manually.

**Parent Topic:**[Organize components in UI Builder pages](work-layouts.md)

## Upgrade your layout to the new layout system

Upgrade your UI Builder pages to the new layout system.

### Before you begin

Role required: ui\_builder\_admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience with the page you want to upgrade.

    See [Configure how users interact with your applications in UI Builder](work-experiences.md) for more information on creating experiences.

3.  Select the page that you want to upgrade.

    ![Page variants that can be upgraded to the new layout system.](../image/uib-update-layout-icon.png)

    You can find page variants that can be upgraded to the new layout system tagged with a red dot.

    **Note:** Legacy pages created using the pre-Quebec row/column layout system are not upgradable and must be rebuilt with the new layout system.

4.  Select the **Update layout** button.

    ![UI Builder updating a page layout to the new layout system.](../image/uib-update-layout.gif)

    UI Builder begins updating your page layout to the new layout system. A notification appears when the process is complete.

5.  You can compare your old layout to the upgraded layout by selecting **compare the two layout versions** in the **Layout needs review before you can edit** notification.

    ![Compare layouts before rejecting or accepting the changes.](../image/uib-layout-review.png)

    Two browser tabs open, one displaying your current layout and one displaying the upgraded layout.

6.  Select **Keep new** if you would like to update the page to the new layout system, or select **Use old** if you would like to keep the page layout as it was.

    A modal appears asking you to confirm your selection.

7.  Select **Keep new** to complete the upgrade to the new layout system, or select **Use old** to reverse the upgrade process and return the page to the old layout system.

    ![Confirm that you want to keep the updated layout for your experience.](../image/uib-layout-keep-new.png)

8.  The page reloads with the changes applied.

9.  View and test your page by selecting the **Preview** button \(![Preview button that opens the page variant.](../image/preview-button.png)\).


