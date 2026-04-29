---
title: Compare versions of a customized widget
description: Compare your most recent update of a customized widget against the previous version to check if your recent changes are causing issues on a portal page.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Widget diagnostics, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Compare versions of a customized widget

Compare your most recent update of a customized widget against the previous version to check if your recent changes are causing issues on a portal page.

## Before you begin

Role required: admin or sp\_admin

## About this task

The option to compare versions is available only for customized widgets that you modified directly. There's no option to compare versions of a customized widget for which you modified only the widget dependencies, Angular Providers, or ng-templates.

There's no option to compare versions for new, cloned, or base system widgets.

## Procedure

1.  Navigate to a portal page.

2.  On the page, open the widget context menu by CTRL+right-clicking any widget.

3.  On the widget context menu, click **Show Widget Customizations**.

    Customized widgets are outlined in red.

4.  On a customized widget, click the information icon \(![Information icon](../image/info-icon.png)\).

5.  On the window, click **Compare with previous version**.

    The system displays the widget records of the current and previous widget versions side by side.

    ![Comparison between current and previous versions of widget](../image/compare-versions.png)

    Although both widget records are labeled **Version**, the left-side record represents the previous version and the right-side record represents the current version.

6.  For each field in which it appears, click the window icon \(![Window icon](../image/pop-out-icon.png)\) to open the code comparator.

    Your most recent changes to the widget code are highlighted in the code comparator.

    ![Code comparator](../image/code-comparator.png)


