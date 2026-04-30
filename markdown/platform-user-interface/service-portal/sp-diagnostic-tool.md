---
title: Widget diagnostics
description: Resolve Service Portal page issues by identifying widget customization levels and checking widget code directly from a portal page.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Widget diagnostics

Resolve Service Portal page issues by identifying widget customization levels and checking widget code directly from a portal page.

If a portal page isn't working as expected, it may be because of a bug in widget code. To diagnose the page, try diagnosing the widgets on the page.

Diagnosing widgets involves:

-   Identifying widget customization levels
-   Checking the code that is used in each widget

## Identifying customization levels

Customization levels describe how widgets have been modified or developed. Identifying the customization level of a widget can help you know which part of the widget code is most important to check. There are four levels of widget customization.

<table id="table_wmr_pkl_cjb"><thead><tr><th>

Customization level

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base system

</td><td>

Base system widget with no modifications, including widgets for which you have set instance options.

</td></tr><tr><td>

Cloned

</td><td>

Widget that you cloned from a base system widget.

</td></tr><tr><td>

New

</td><td>

Widget that you created.

</td></tr><tr><td>

Customized

</td><td>

Base system widget that you configured in any of the following ways:-   Modified the widget code directly
-   Modified widget option schema
-   Modified widget dependencies, ng-templates, or Angular Providers

</td></tr></tbody>
</table>To identify the customization levels of widgets on a portal page, open the Widget Context Menu and select **Show Widget Customizations**. Widgets are color-coded as follows:

<table id="table_avs_mbb_gjb"><tbody><tr><td>

![Identifying customization levels](../image/diagnostic-tool.png)

</td><td>

-   Green – base system widget
-   Yellow – cloned widget
-   Blue – new widget
-   Red – customized widget

</td></tr></tbody>
</table>## Checking the widget code

After you've identified the customization levels of widgets on a portal page, check the code in each widget.

To view the widget code from the portal page, click the information icon \(![Information icon](../image/info-icon.png)\) on a widget.

![Widget diagnostics window](../image/widget-diagnostics-window.png)

From the widget diagnostics window, you can check the widget code in several ways:

-   [View a widget record from a portal page](../task/view-widget-record.md)

    View and identify potentially problematic code in the widget record without navigating away from the portal page.

-   [View related records](../task/view-related-records.md)

    View and identify potentially problematic code in the widget dependencies, Angular Providers, and ng-templates that are being used by the widget.

-   [Compare changes to related records](../task/compare-related-record-changes.md)

    Compare an Angular Provider or ng-template against its previous version so that you check if your most recent code changes are causing issues on a portal page.

-   [Compare changes to a customized widget](../task/compare-widget-versions.md)

    Compare your most recent update of a customized widget against the previous version to check if your recent changes are causing issues on a portal page.

-   [Compare a customized widget against the base system](../task/compare-with-base-system.md)

    Identify customizations to a base system widget so that you can revert your customized widgets and resolve issues on a portal page.


## Recommendations for diagnosing widgets

Of the four customization levels, the highest priority issue is customized widgets. These widgets aren't supported in system upgrades. If you're experiencing page issues during an upgrade, it may be because you have a customized widget on your portal page.

To resolve page issues that may be caused by customized widgets, identify which parts of the widget code have been customized. Then revert the code to the original configuration. For more information on identifying these code differences, see [Compare a customized widget against the base system](../task/compare-with-base-system.md).

**Tip:** Even if a customized widget is not causing page issues now, you may want to revert to the original widget to prevent issues during upgrades later.

If you're still experiencing page issues after reverting customized widgets, check your new and cloned widgets next.

With a new widget, it's likely that your most recent code changes are causing issues on your portal page. To identify your most recent changes so that you can debug your code, follow the steps in [Compare changes to related records](../task/compare-related-record-changes.md).

If you cloned a widget prior to a system upgrade, it's likely that the cloned widget didn't receive the same updated code as the base system widget. In this case, it's recommended that you clone the widget again and add your customizations to the clone.

A base system widget is least likely to cause page issues. If you've already checked other widgets and are still experiencing page issues, remove base system widgets from the page and add them again without any widget options set. You can also try adding base system widgets to another page instead.

## Limitations

There are several known limitations using widget diagnostics from a portal page:

-   Although you can view and compare widget code, you can't fix or revert code directly. Navigate away from the portal to change the code.
-   If you navigate to another portal page while using widget diagnostics, the system disables the tool.
-   Because the tool uses color to categorize widgets, it may not be accessible for visually impaired users.
-   The widget dependencies that are listed on the portal page reflect only the first-level dependencies. Any dependency that is nested deeper than the first level is not included. To further troubleshoot the widget, check the nested dependencies in the widget record.
-   There is no way for the system to track a Widget Dependency after you've deleted it.

-   **[View a widget record from a portal page](../task/view-widget-record.md)**  
View and identify potentially problematic code in the widget record without navigating away from the portal page.
-   **[View related records](../task/view-related-records.md)**  
View and identify potentially problematic code in the widget dependencies, Angular Providers, and ng-templates that are being used by the widget.
-   **[Compare changes to related records](../task/compare-related-record-changes.md)**  
Compare an Angular Provider or ng-template against its previous version so that you check if your most recent code changes are causing issues on a portal page.
-   **[Compare changes to a customized widget](../task/compare-widget-versions.md)**  
Compare your most recent update of a customized widget against the previous version to check if your recent changes are causing issues on a portal page.
-   **[Compare a customized widget against the base system](../task/compare-with-base-system.md)**  
Identify customizations to a base system widget so that you can revert your customized widgets and resolve issues on a portal page.

**Parent Topic:**[Developing custom widgets](widget-dev-guide.md)

