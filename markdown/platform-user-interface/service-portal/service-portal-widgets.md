---
title: Using portal widgets
description: Widgets are what define the content of your portal pages. You can use the base system widgets provided with Service Portal, clone and modify widgets, or develop custom widgets to fit your own needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-04-21"
reading_time_minutes: 5
breadcrumb: [Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Using portal widgets

Widgets are what define the content of your portal pages. You can use the base system widgets provided with Service Portal, clone and modify widgets, or develop custom widgets to fit your own needs.

Using widgets with Service Portal 

When you create or update a page in the Service Portal Designer, add widgets by searching in the widget filter and dragging a widget onto the page. You can also access all widget records from the platform at **All** &gt; **Service Portal** &gt; **Widgets**.

## Base system widgets

You can use the base system widgets included with Service Portal to get started configuring portal pages. Base system widgets are read-only so you can benefit from future updates. However, for each instance of a base system widget that you add to a page, you can configure the instance options available for that widget.

For a list of base system widgets and information about their instance options, see the [Widget library](widget-showcase.md).

## Widget instances

When you add a widget to a page using the Service Portal Designer, it creates a widget instance. A widget instance is a reference to a widget that contains a location, properties, and CSS specific to that instance. Adding the same widget multiple times to the same page creates multiple instances.

All widget instances point to a widget. If you edit that widget, all of its widget instances receive that change as well. You can also make changes specific to a widget instance, and only that widget instance is affected.

For example, the following image includes four instances of the base system [Icon Link widget](icon-link-widget.md) with different configurations specific to each instance.

![Icon link widgets from the Service Portal homepage with different icons and titles for each instance](../image/IconLinkInstances.png "Icon link widgets")

**Note:** For widgets that do not include any information by default, you must configure the options for their widget instances before they will display on a portal page.

## Widget context menu

From any rendered Service Portal page, you can CTRL+right-click a widget to see more configuration options in a context menu.

For example, navigate to **Service Portal** &gt; **Service Portal Home** to open a sample portal page. CTRL+right-click Knowledge Base on that page.

![Icon Link widget context menu](../image/WidgetContextMenu.png "Widget context menu")

**Note:** You must have the admin or sp\_admin role to see the widget context menu. When you impersonate a user without one of those roles, you can see the menu. However, a regular user signed in without those roles can’t see the menu.

|Option|Description|
|------|-----------|
|Widget performance|How long it takes for a widget to load|
|Instance options|Specify an [instance of a widget](c_ConfigureWidgetInstances.md). Widget instance options vary depending on the widget that you select. For example, the instance options for the cool clock widget include different time zones for each instance, so you can have the same clock four times on a page, but with all different time zones.|
|Instance in Page Editor|Opens that instance of the widget in the Page Editor|
|Page Designer|Opens the widget in the [Service Portal Designer](../task/t_ConfigureAPage.md#), which enables you to add containers, columns, and widgets. You can add styling from the Service Portal Designer to the widget or to the page the widget lives on.|
|Show Widget Customizations|Shows customization levels of widgets on the page so that you can diagnose page issues. For more information, see [Widget diagnostics](sp-diagnostic-tool.md).|
|Edit Container Background|Edit the layout in which the widget is located.|
|Widget Options Schema|Define the options that you can select for an instance of a widget. For more information on configuring your own instance options, see [Widget option schema](c_WidgetInstanceOptions.md#).|
|Widget in Form Modal|Opens the widget form in a pop-up window so you can make quick changes to the widget.|
|Widget in Editor|Opens the widget in the Widget Editor. You can use the Widget Editor to configure HTML templates, CSS, client scripts, service scripts, and demo data for the widget.|
|Log to console: $scope.data|The $scope.data object passes data from the server to the client-side controller. Instead of adding console.log messages or alerts into the controller code, you can log the $scope.data object to the browser console and view the data there.|
|Log to console: $scope|Similar to the $scope.data object, except it logs everything in $scope to the console.|

## Custom widgets

Base system widgets are read-only so you can benefit from future updates. To make changes, you can copy base system widgets. However, copied widgets are considered custom and don't benefit from future updates to the widgets they were copied from. You can also create widgets from scratch. To learn more about copying or creating widgets, see [Developing custom widgets](widget-dev-guide.md).

-   **[Configure widget instances](c_ConfigureWidgetInstances.md)**  
Create unique instances of widgets by configuring the options for each instance.
-   **[Widget library](widget-showcase.md)**  
You can use base system widgets as-is in your Service Portal or duplicate them to suit your own business needs.
-   **[Configure widget loading order in Service Portal](../task/configure-widget-loading-order.md)**  
Configure service portal pages to defer load the widgets on a page. The delay in loading of non-essential widgets helps to improve page loading speed and optimizes the use of resources.

**Parent Topic:**[Configuring Service Portal](configuring-service-portal.md)

