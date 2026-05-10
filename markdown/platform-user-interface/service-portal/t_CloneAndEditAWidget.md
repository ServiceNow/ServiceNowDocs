---
title: Clone a widget
description: Take advantage of existing code by cloning and editing an existing widget.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Clone a widget

Take advantage of existing code by cloning and editing an existing widget.

## Before you begin

Role required: admin or sp\_admin

## About this task

**Note:** Base system widgets are read-only so you can benefit from future updates. To make changes, you can clone base system widgets. However, cloned widgets are considered custom and don't benefit from future updates to the widgets they were cloned from.

## Procedure

1.  Open the Widget Editor in the Service Portal Configuration page, then select an existing widget from the **Select a widget** list.

    For example, select **Hello World 2**.

2.  From the list menu in the widget header, click **Clone "Hello World 2"**.

    ![Clone a Widget form](../image/CloneAWidget.png "Clone a widget")

3.  Enter a name for the cloned widget.

    The widget ID is created automatically based on the widget name.

4.  Select **Create test page** to automatically create a page containing the widget.

5.  Use the check boxes to show or hide the different components of the widget editor as needed.

    Make changes to the HTML Template, CSS, client script, server script, or the link function.

    **Note:** For server-side scripts, you can turn on using the ECMAScript 2021 \(ES12\) JavaScript mode if your application uses ES5 Standards mode or Compatibility mode. Scripts in applications with the JavaScript mode set to ECMAScript 2021 \(ES12\) use ECMAScript 2021 \(ES12\) by default. For more information, see [Turn on ECMAScript 2021 \(ES12\) mode for a script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/set-es12-mode-scripts.md).

    ![Hello World 2 widget cloned and edited to say "Hola, mundo"](../image/CalculatorCodeExample.png "Hello World 2 clone")

6.  In order to enable a preview of your widget, use **Enable Preview** from the menu.

    Use the eye icon that appears to show or hide a preview of your widget.


## What to do next

If you clone a widget that uses the Angular ng-template, you must manually clone the template and change the name of the template reference in the widget.

For example, the header menu widget uses the Angular ng-template `menuTemplate`. If you clone the header menu widget, you must also clone the `menuTemplate` and give the clone a unique name. When you open the clone of the header menu widget, you can see a reference to the menuTemplate in the HTML.

![ng-template called menuTemplate highlighted and changed to menuTemplateCopy in header menu widget HTML](../image/NgTemplateCopy.png "menuTemplate in header widget HTML")

**Parent Topic:**[Developing custom widgets](../concept/widget-dev-guide.md)

