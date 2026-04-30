---
title: View a widget record from a portal page
description: View and identify potentially problematic code in the widget record without navigating away from the portal page.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Widget diagnostics, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# View a widget record from a portal page

View and identify potentially problematic code in the widget record without navigating away from the portal page.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Navigate to a portal page.

2.  On the page, open the widget context menu by CTRL+right-clicking any widget.

3.  On the widget context menu, click **Show Widget Customizations**.

    Widgets are color-coded as follows:

    |Color|Customization level|
    |-----|-------------------|
    |Green|Base system widget|
    |Yellow|Cloned widget|
    |Blue|New widget|
    |Red|Customized widget|

4.  On any widget, click the information icon \(![Information icon](../image/info-icon.png)\).

5.  On the window, click **Open widget in platform**.

    ![Open widget in platform](../image/open-widget.png)

    **Note:** The **Open widget in platform** button doesn't appear for all customized widgets. The button appears for customized widgets only if you modified one or more widget dependencies, Angular Providers, or ng-templates.


## Result

A new window opens with a read-only view of the widget record.

**Parent Topic:**[Widget diagnostics](../concept/sp-diagnostic-tool.md)

