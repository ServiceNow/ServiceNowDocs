---
title: Compare a cloned or customized widget against a base widget
description: Identify customizations to a widget so that you can revert your cloned or customized widgets and resolve issues on a portal page.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Widget diagnostics, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Compare a cloned or customized widget against a base widget

Identify customizations to a widget so that you can revert your cloned or customized widgets and resolve issues on a portal page.

## Before you begin

Role required: sp\_admin or admin

## About this task

If a widget is cloned from another cloned widget, both clones are compared against the base widget.

## Procedure

1.  Navigate to a portal page.

2.  On the page, open the widget context menu by CTRL+right-clicking any widget.

3.  On the widget context menu, select **Show Widget Customizations**.

    Customized widgets are outlined in red. Cloned widgets are outlined in yellow.

4.  On any customized or cloned widget, select the information icon \(![Information icon](../image/info-icon.png)\).

5.  From the Widget Diagnostics dialog box, select **Compare with base widget**.

    The system displays the widget records of the base widget and cloned or customized widgets side by side.

    **Note:** The left-side record represents the base widget and the right-side record represents the cloned or customized widget.

    ![Comparison between customized and base widgets](../image/compare-with-base.png)

6.  For each field in which it appears, select the window icon \(![Window icon](../image/pop-out-icon.png)\) to open the code comparator.

    Differences between the code of the customized or cloned widget and base widget versions are highlighted.

    **Note:** The left-side record represents the base widget and the right-side record represents the cloned or customized widget.

    ![Code comparator](../image/code-comparator.png)


