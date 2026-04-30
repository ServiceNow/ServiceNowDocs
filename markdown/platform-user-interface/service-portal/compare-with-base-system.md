---
title: Compare a customized widget against the base system
description: Identify customizations to a base system widget so that you can revert your customized widgets and resolve issues on a portal page.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Widget diagnostics, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Compare a customized widget against the base system

Identify customizations to a base system widget so that you can revert your customized widgets and resolve issues on a portal page.

## Before you begin

Role required: admin or sp\_admin

## About this task

The option to compare a widget against the base system version is available only for customized widgets. There's no option to compare a cloned widget against the widget that you cloned it from.

## Procedure

1.  Navigate to a portal page.

2.  On the page, open the widget context menu by CTRL+right-clicking any widget.

3.  On the widget context menu, click **Show Widget Customizations**.

    Customized widgets are outlined in red.

4.  On any customized widget, click the information icon \(![Information icon](../image/info-icon.png)\).

5.  On the window, click **Compare with Base system widget**.

    The system displays the widget records of the base system and customized widgets side by side.

    **Note:** Although both widget records are labeled **Version**, the left-side record represents the base system widget and the right-side record represents the customized widget.

    ![Comparison between customized and base system widgets](../image/compare-with-base.png)

6.  For each field in which it appears, click the window icon \(![Window icon](../image/pop-out-icon.png)\) to open the code comparator.

    Differences between the code of current and previous widget versions are highlighted.

    ![Code comparator](../image/code-comparator.png)


**Parent Topic:**[Widget diagnostics](../concept/sp-diagnostic-tool.md)

