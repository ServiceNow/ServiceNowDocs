---
title: Developing custom widgets
description: Develop custom widgets for portals using AngularJS, Bootstrap, and the ServiceNow API.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Service Portal, Configure UIs and portals, Configure user experiences]
---

# Developing custom widgets

Develop custom widgets for portals using AngularJS, Bootstrap, and the ServiceNow API.

## Before you begin

To develop widgets, you need ServiceNow API experience to:

-   Run record queries on the server.
-   Create and update records.

You need AngularJS experience to:

-   Bind variables to client controllers.
-   Access server objects in a widget.
-   Gather user input.

Optionally, you can build on the Bootstrap template by accessing Bootstrap components.

## Parts of a widget

Like Angular directives, widgets execute a specified behavior within a Service Portal page. A widget includes mandatory and optional scripting components.

-   **HTML template**

    A mandatory widget component.

    The HTML template requires knowledge of AngularJS to display and gather data. Use the HTML template to:

    -   Render the dynamic view that a user sees in the browser using information from the model and controller.
    -   Bind client script variables to your markup.
    -   Gather data from the end user.
-   **Client script**

    A mandatory widget component.

    A client script requires knowledge of both the ServiceNow API and AngularJS to create a client controller. Use the client script to:

    -   Map server data from JavaScript and JSON objects to client objects.
    -   Process data before rendering it.
    -   Pass data to the HTML template.
    -   Pass user input and data back to the server for processing.
-   **Server script**

    A mandatory widget component.

    A server script requires knowledge of the ServiceNow API to work with record data. Use the server script to:

    -   Set the initial state of the widget.
    -   Send record data to the widget client script using the **data** variable.
    -   Run server-side queries.
-   **Link function**

    An optional widget component.

    The link function requires knowledge of AngularJS. Use a link function to directly manipulate the DOM.

-   **Option schema**

    An optional widget component.

    Allows a Service Portal admin to configure a widget. Use the option schema to:

    -   Specify the parameters for a widget.
    -   Allow admin users to define instance options for a widget instance.
    -   Develop flexible, reusable widgets.
-   **Angular Providers**

    An optional widget component.

    Angular Providers require knowledge of AngularJS. Use Angular Providers to:

    -   Keep widgets in sync when changing records or filters.
    -   Share context between widgets.
    -   Maintain and persist state.
    -   Create reusable behaviors and UI components and inject them into multiple widgets.
-   **Dependencies**

    An optional widget component.

    A widget dependency is an external resource used by your widget such as JavaScript or CSS files.


## Global objects in widgets

When a widget begins to render for the first time on a page, the server script executes first and accesses three global objects: **input**, **options**, and **data**. Because the **input** variable is a data object sent from the client script, this variable is undefined when first initialized.

![Available variables in server and client script global](../image/Server-ClientGlobalScripts.png)

When a widget is first instantiated, the server script:

1.  Initializes an empty **data** object.
2.  Initializes the **input** object with any data sent from the client controller, or the **options** object with any data used to initialize the widget.
3.  Sends the **data** object to the client controller as JSON.

The client script:

1.  Accesses the server **data** object using `c.data`.

    **Note:** By default, widgets use the **c** variable to represent the controller instance using `controller as` syntax. You can change this variable when creating or cloning widgets.

2.  Uses `server.update()` to post changes to the data model. This method updates the server script using the **input** object.

    **Note:** After calling `server.update()`, the client script **data** object is automatically overwritten by the server script **data** object.

3.  Uses `c.options` to access the values used to invoke the widget on the server. This object is read-only.

## Using the Widget Editor

When you create a widget, a record is created in the sp\_widget table. However, you can use the Widget Editor in Service Portal Configuration as your scripting environment. The Widget Editor is a full page application similar to an IDE. You can show the parts of the widget you want to edit and hide the rest, while previewing your changes in real time.

![Widget editor with the calculator widget showing script examples for the HTML template, CSS, Client script, and the server script](../image/WidgetEditorSample.png)

-   **[General guidelines for developing widgets](general-guidelines-developing-widgets.md)**  
When developing custom widgets, keep these general guidelines in mind for optimal performance, scalable development, and a good user experience.
-   **[Tutorial: Build a custom widget](adv-widget-tutorial.md#)**  
Follow this tutorial to build a custom widget that displays Service Catalog items. Use this tutorial as a model to help you understand the advanced scripting power of the Service Portal.
-   **[Clone a widget](../task/t_CloneAndEditAWidget.md)**  
Take advantage of existing code by cloning and editing an existing widget.
-   **[Create a new widget](../task/create-new-widget.md)**  
Create a new widget to build a custom widget from scratch.
-   **[Widget option schema](c_WidgetInstanceOptions.md#)**  
Widget instances allow users to uniquely configure each widget they add to a page. Use the option schema to define the parameters for your widget.
-   **[Widget API reference](../reference/widget-api-reference.md#)**  
Service Portal includes client and server side APIs to use in widget client and server scripts.
-   **[Reuse components with Angular Providers](../task/angular-providers.md)**  
Angular Providers are reusable components that can be injected into multiple widgets. To ensure quick loading widgets and a high performing portal, create Angular Providers instead of overloading your client controllers with persistent data and additional logic. With Angular Providers, you can maintain data for the lifetime of your Service Portal and reuse components and data objects across multiple widgets.
-   **[Embedded widgets](c_NestedWidgets.md#)**  
Embed a widget in the HTML template, server script, or client script.
-   **[Create a widget dependency](../task/widget-dependencies.md)**  
In Service Portal, you can link JavaScript and CSS files to widgets to create dependencies between widgets and third-party libraries, external style sheets, and angular modules.
-   **[Internationalize a widget](c_WidgetLocalization.md)**  
Use the `${}` or `gs.getMessage()` syntax in the **HTML Template**, **Client Script**, or **Server Script** fields of a widget to tag strings for translation so you can localize your Service Portal content.
-   **[Replace a Service Catalog form script with a widget](../task/ui-macro-widget.md)**  
You can use widgets in Service Portal to replace UI Macros. If your Service Catalog form includes a UI Macro that references other fields or variables on the form, you can create a widget to hold reusable code and embed it within the Service Catalog form. Use special syntax to access any variable fields on the form.
-   **[Widget troubleshooting guide](../reference/widget-troubleshooting-guide.md)**  
Use the following tools to investigate and resolve unexpected behavior in your custom Service Portal widgets.
-   **[Widget diagnostics](sp-diagnostic-tool.md)**  
Resolve Service Portal page issues by identifying widget customization levels and checking widget code directly from a portal page.

**Parent Topic:**[Service Portal](c_ServicePortal.md)

