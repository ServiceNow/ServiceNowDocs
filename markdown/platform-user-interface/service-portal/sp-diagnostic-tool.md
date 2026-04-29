---
title: Widget diagnostics
description: Resolve Service Portal page issues by identifying widget customization levels and checking widget code directly from a portal page.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
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

Base

</td><td>

Base widget installed on a base system or with other ServiceNow plugins. Base widgets have no modifications but can have widget instances for which you have set instance options.

</td></tr><tr><td>

Cloned

</td><td>

Widget that you cloned from a base widget.

</td></tr><tr><td>

New

</td><td>

Widget that you created.

</td></tr><tr><td>

Customized

</td><td>

Base widget that you configured in any of the following ways:-   Modified the widget code directly
-   Modified widget option schema
-   Modified widget dependencies, ng-templates, or Angular Providers

</td></tr></tbody>
</table>To identify the customization levels of widgets on a portal page, open the Widget Context Menu and select **Show Widget Customizations**. Widgets are color-coded as follows:

-   Green: base widget
-   Yellow: cloned widget
-   Blue: new widget
-   Red: customized widget

![Identifying customization levels](../image/diagnostic-tool.png "Widget customizations highlighted on a portal page")

## Checking the widget code

After you've identified the customization levels of widgets on a portal page, check the code in each widget.

To view the widget code from the portal page, click the information icon \(![Information icon](../image/info-icon.png)\) on a widget.

![Widget diagnostics window](../image/widget-diagnostics-window.png)

From the widget diagnostics window, you can check the widget code in several ways:

-   [View a widget record from a portal page](../task/view-widget-record.md)

    View and identify potentially problematic code in the widget record without navigating away from the portal page.

-   [Identify customizations in widget related records](../task/view-related-records.md)

    View and identify potentially problematic code in the widget dependencies, Angular Providers, and ng-templates that are being used by the widget.

-   [Compare versions of a widget related record](../task/compare-related-record-changes.md)

    Compare an Angular Provider or ng-template against its previous version so that you check if your most recent code changes are causing issues on a portal page.

-   [Compare versions of a customized widget](../task/compare-widget-versions.md)

    Compare your most recent update of a customized widget against the previous version to check if your recent changes are causing issues on a portal page.

-   [Compare a cloned or customized widget against a base widget](../task/compare-with-base-system.md)

    Identify customizations to a widget so that you can revert your cloned or customized widgets and resolve issues on a portal page.


## Recommendations for diagnosing widgets

Of the four customization levels, the highest priority issue is customized widgets. These widgets aren't supported in system upgrades. If you're experiencing page issues during an upgrade, it may be because you have a customized widget on your portal page.

To resolve page issues that may be caused by customized widgets, identify which parts of the widget code have been customized. Then revert the code to the original configuration. For more information on identifying these code differences, see [Compare a cloned or customized widget against a base widget](../task/compare-with-base-system.md).

**Tip:** Even if a customized widget is not causing page issues now, you may want to revert to the original widget to prevent issues during upgrades later.

If you're still experiencing page issues after reverting customized widgets, check your new and cloned widgets next.

With a new widget, it's likely that your most recent code changes are causing issues on your portal page. To identify your most recent changes so that you can debug your code, follow the steps in [Compare versions of a widget related record](../task/compare-related-record-changes.md).

If you cloned a widget prior to a system upgrade, it's likely that the cloned widget didn't receive the same updated code as the base widget. In this case, it's recommended that you clone the widget again and add your customizations to the clone.

A base widget is least likely to cause page issues. If you've already checked other widgets and are still experiencing page issues, remove base widgets from the page and add them again without any widget options set. You can also try adding base widgets to another page instead.

## Limitations

There are several known limitations using widget diagnostics from a portal page:

-   Although you can view and compare widget code, you can't fix or revert code directly. Navigate away from the portal to change the code.
-   If you navigate to another portal page while using widget diagnostics, the system disables the tool.
-   Because the tool uses color to categorize widgets, it may not be accessible for visually impaired users.
-   The widget dependencies that are listed on the portal page reflect only the first-level dependencies. Any dependency that is nested deeper than the first level is not included. To further troubleshoot the widget, check the nested dependencies in the widget record.
-   There is no way for the system to track a Widget Dependency after you've deleted it.

