---
title: Reuse components with Angular Providers
description: Angular Providers are reusable components that can be injected into multiple widgets. To ensure quick loading widgets and a high performing portal, create Angular Providers instead of overloading your client controllers with persistent data and additional logic. With Angular Providers, you can maintain data for the lifetime of your Service Portal and reuse components and data objects across multiple widgets.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Reuse components with Angular Providers

Angular Providers are reusable components that can be injected into multiple widgets. To ensure quick loading widgets and a high performing portal, create Angular Providers instead of overloading your client controllers with persistent data and additional logic. With Angular Providers, you can maintain data for the lifetime of your Service Portal and reuse components and data objects across multiple widgets.

## Before you begin

Role required: admin or sp\_admin

## About this task

By creating an Angular Provider, you can:

-   Keep widgets in sync when changing records or filters.
-   Share context between widgets.
-   Maintain and persist state.
-   Create behaviors and inject them into multiple widgets.

To learn more, visit [Angular Providers](https://docs.angularjs.org/guide/providers).

**Tip:** For easier maintenance and troubleshooting, remove any unused providers from the Angular Providers related list in the Widget \[sp\_widget\] table.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration** &gt; **Portal Tables** &gt; **Widget Angular Provider**.

    The Widget Angular Providers table opens.

2.  Click **New** to create a new record.

3.  Select the type of Angular Provider.

    -   Directive
    -   Factory
    -   Service
    To facilitate migration to ECMAScript 6 or later, consider using services over factories.

4.  Define a name.

    You will use the name to associate the Provider with your widget.

5.  Add a script in the **Client Script** field.

    A basic factory that formats a number in US currency.

    ```
    function formatterFactory(){
      var myVal = Number;
      return {
        format: function(myVal) {
          return '$' + myVal.toFixed(2);
        }
      }
    }
    ```

6.  Associate the Angular Provider with a widget.

    1.  Navigate to `<yourInstanceURL>/sp_config?id=widget_edit`.

    2.  Open the widget you would like to associate with the Angular Provider.

    3.  Under **Related Lists**, select **Angular Providers**.

    4.  In the **Angular Providers** list, click **New**.

    5.  In the **Angular Provider** field, select the appropriate Provider.

    6.  Check the **Widget** field to ensure that you are associating the Angular Provider with the correct widget.

    7.  Click **Save**.

7.  Update the appropriate scripts in your widget to inject the Angular Provider into the widget.

    Inject the factory into your widget client script by passing the name of the factory as an argument in your client controller function. You can then access the object defined in the factory function in your widget client script.

    ```
    function(formatterFactory) {
      /* widget controller */
      var c = this;
      console.log(formatterFactory.format(300));
    }
    ```

    If defining a directive, use the directive in the widget HTML template.

8.  To edit the Angular Provider after it is registered with your widget, open the Angular Provider client script in the widget editor.

    1.  Navigate to **Service Portal Configuration** &gt; **Widget Editor**.

    2.  Under **Edit an existing widget**, select the widget associated with your Angular Provider.

    3.  From the **Show** menu, open the **Dependencies** list and select the Angular Provider.

        **Note:** Only Angular Providers associated with the widget are displayed in the **Dependencies** list. This list includes any external resources your widget depends on.

        The Angular Provider client script displays in the widget editor. In the widget editor interface, you can edit and save your widget and Provider scripts at the same time.


## What to do next

To use an Angular Provider with multiple widgets, register your Provider with each widget and update the appropriate scripts.

**Parent Topic:**[Developing custom widgets](../concept/widget-dev-guide.md)

