---
title: Configure widget instances
description: Create unique instances of widgets by configuring the options for each instance.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure widget instances

Create unique instances of widgets by configuring the options for each instance.

## Before you begin

Create or edit a portal page and add widgets to it. You can also configure the existing widget instances on a base system page. For more information, see [Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#).

Role required: sp\_admin or admin

## About this task

You can have several instances of the same widget on a page, and each instance of the widget you configure remains unique. For example, each instance of the [Cool Clock widget](cool-clock-widget.md) on a page could use a different time zone.

Adding a widget to a page creates a record on the Widget Instances \[sp\_instance\] table with the following information:

-   A reference to the widget
-   A reference to the column of the page where the widget is located
-   The configuration for a widget in the form of pre-defined form fields and an **Additional Options** field in JSON format

**Note:** For widgets that do not contain any information by default, you must configure the options for their widget instances before they will appear on a portal page.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  Select the page with the widget instance\(s\) you want to configure.

4.  In the Service Portal Designer, move to a widget instance and select the Edit icon \(![Edit icon](../image/WidgetEditIcon.png)\).

5.  In the instance options window, complete the fields to configure the widget instance.

    Instance options vary depending on which widget you select.

6.  Select **Save**.


## Configure widget instance options

![Gif showing how to access widget instance options from the Service Portal Designer.](../image/WidgetInstanceOptions.gif)

## What to do next

Advanced users can define what options are available for a widget. For more information, see [Widget option schema](c_WidgetInstanceOptions.md#).

**Parent Topic:**[Using portal widgets](service-portal-widgets.md)

