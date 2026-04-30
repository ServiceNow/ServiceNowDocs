---
title: Manage actions in UI Builder pages
description: Learn how to work with events so that you can add actions to components, pages, data resources, and declarative actions in UI Builder.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Manage actions in UI Builder pages

Learn how to work with events so that you can add actions to components, pages, data resources, and declarative actions in UI Builder.

## Actions in UI Builder

UI actions tell UI Builder what to do when an [event](ui-builder-glossary.md#) is triggered. An event is an action a user takes or occurrence that happens on a [page](ui-builder-glossary.md#). Use UI actions to create interactive, user-friendly interfaces that help your users complete tasks. Each [component](ui-builder-glossary.md#) has its own events associated with it. Events include:

-   User clicks a data visualization
-   Page successfully fetches data
-   User selects a radio button
-   Page loads

![Types of events that can trigger actions.](../image/events-example-graphic.png)

## Events in UI Builder

Use an event to add actions to your components, pages, and data resources.

-   A component event is an action that you set up for a component. You set up an event handler to configure that component action. For example, you can add a button component to your UI Builder page. Then, you can add an event handler to apply an action for that button, such as going to a web page.
-   Page events perform actions for the entire page. You can configure the following page events:
    -   Page event mappings. Add, remove, or clear alert notifications on your page.
    -   Variant event mappings. Add, remove, or clear alert notifications on your page variant.
    -   Dispatched events. Create dispatched events for your page to create relayed event mappings that model events after a parent event handler. Select a target parent event handler to model the payload fields after it.
    -   Handled events. A handled event is an event that is exposed and available for use by other users. After you create a handled event, it is available under **Page event mappings** for other users to use. You can also set up payload fields that you create manually or choose a template for your handled event, such as an open or close a modal dialog.
-   Data resources events map data resources to notify information about when data is fetched.
-   Events for a page or component do nothing until the event is mapped to one or more event handlers.

![Event progression for different types of events.](../image/events-progression-graphic.png)

## Event mapping in UI Builder

Map actions to events such as clicking a button or filling in a field. An event mapping is the process that enables you to map an event's payload or contextual values to the object or handler that acts on that event.

For more information about event mapping, see [Define map events](event-mapping.md).

## Event handlers in UI Builder

An event handler is an action performed when an event occurs. By mapping an event handler to an event, you are specifying which action or actions to take when the event occurs. Use an event handler to configure an action for your UI Builder page or the components on the page. For example:

-   Clicking a data visualization opens a list of records represented in the visualization
-   Fetching data successfully for a list opens an alert that indicates the data fetch was successful
-   Selecting a radio button adjusts the filter for a list on the page
-   Loading a page opens a modal to confirm acceptance of cookies before proceeding

When you add an event handler to a UI Builder page or component, you can choose different types of event handlers. For example, a Button component can have the following types of event handlers:

-   Inherited event handlers. An inherited event handler is exposed from the page that you are working in. If you are in the parent UI Builder page, an inherited event handler could be exposed from the app shell. The following table lists the different types of inherited event handlers that you can use and what you can do with them.

<table id="table_uwz_1py_24b"><thead><tr><th>

Event handler

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breadcrumb URL changed

</td><td>

 

</td></tr><tr><td>

Link to destination

</td><td>

Navigate to a destination.-   App routes: Link to another page within an app, like a home screen.
-   External URL: Link to a website or any external URL.
Sample script

```
    return {
        route: null, /* Page route, e.g. 'record' */
        fields: null, /* Required params, e.g. {"table":"incident","sysId":"X"} */
        params: null, /* Optional params, e.g. {"selectedIndex" : 1} */
        ☑️redirect: null, /* ??? True/false? */
        ☑️passiveNavigation: null, /* Load in background, e.g. 'false' */
        title: null, 
        multiInstField: null, 
        ☑️targetRoute: null, /* ??? */
        ☑️external: null /* ??? True/false? */
    };

```

</td></tr><tr><td>

Add parameters to URL

</td><td>

Add additional parameters to a URL.Sample script

```
{ “selectedTabIndex” : 0 }
```

</td></tr><tr><td>

Open or close modal dialog

</td><td>

After you create a modal, use **Open or close modal dialog** to trigger the modal.

</td></tr></tbody>
</table>-   Page-level event handlers. This type of event handler is common to all pages, and you would use this handler type when you want to add or clear page-level alert notifications. The following table lists the different types of page-level event handlers that you can use and what you can do with them.

<table id="table_xdx_dqy_24b"><thead><tr><th>

Event handler

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add alert notifications

</td><td>

Add a code snippet to send an alert notification. For example: ```
return {
    items: [{"type" : "info", "message" : "Info message", "id" : "optionalID"}] /* Types: info, warning, error */
};

```

</td></tr><tr><td>

Remove alert notification

</td><td>

Add code to call alert notification IDs that you want to dismiss. For example, click a button to remove a page load alert notification.

</td></tr><tr><td>

Clear alert notification

</td><td>

Add code to call all alert notification IDs that you want to dismiss. For example, click a button to remove all alert notifications.

</td></tr><tr><td>

Set loading state

</td><td>

Toggle loading on or off. For example, you can toggle loading on to load the page when you click a button or toggle loading off to not load the page when a button is clicked.

</td></tr><tr><td>

Update client state parameter

</td><td>

Declaratively set the client state parameter. Let's say that you have a client state parameter that you set up with a value. You can configure the **Update client state parameter** event handler to update the client state parameter with a new value. For example, you have a client state parameter that is called **Greeting** that is set up with `Hello` as the initial value. You can add an **Update client state parameter** event handler, select the **Greeting** client state parameter, and then enter a new value like `Goodbye`. When you click the button, **Goodbye** replaces **Hello** on the page.

</td></tr><tr><td>

UXF macroponent viewport load requested

</td><td>

Add to a component, such as a button component, to open a viewport. For more information, see [Add a viewport component to your page](work-with-viewport-components.md).

</td></tr></tbody>
</table>-   Data resource handlers. This type of event handler triggers the fetching or writing of data to the server.

    You can refresh the app shell data source data on your UI Builder page by clicking a button. For example, with a data resource handler, you can do the following actions:

    -   Bind data to the description of an incident record.
    -   Change the value of the incident description.
    -   Add a button component to your page.
    -   Label the button as `Refresh incident`.
    -   Add a **Look Up Record** event handler for the button.
    -   Save your page.
    -   If the description of the incident record changes, click **Refresh** to update the description on your page.
-   Client scripts. Scripts that execute when an event is triggered on a component. You create these scripts in the Client scripts section in UI Builder. For more information, see [Define and bind client scripts to components](../task/define-client-scripts.md).

## Binding events to components in UI Builder

Bind event handlers to the events on a component. When you add components to your UI Builder page, these components are not configured to perform any action on your page. For example, a button component is static and does not do anything until you bind an event action to it, such as deleting a record. Some components have several events where event handlers can be assigned. For example, on the list component, you can assign a navigation handler to the **Row clicked** event. You can also assign an open modal to the **Data fetch failed** event. For more information, see [Bind an event to a component](../task/bind-event-component.md).

## Binding events to UI Builder pages

Bind a page-level event to execute event handlers on the page. For example, use page-level events for page notifications, page load, or when a page property changes. The assignment of the event handler to the page-level event is similar to assigning handlers to events from components.

You can bind event mappings using the following methods:

-   Page event mappings. Add, remove, or clear alert notifications on your page.
-   Variant event mappings. Add, remove, or clear alert notifications on your page variant.
-   Dispatched events. Create dispatched events for your page to create relayed event mappings that model events after a parent event handler. Select a target parent event handler to model the payload fields after it.
-   Handled events. Add a handled event for an event that is exposed and available for use by other users.

For more information, see [Bind an event to a page](../task/bind-event-page.md).

## Binding events to data resources in UI Builder

Bind event handlers to individual data resources on your UI Builder page. For example, when a data resource successfully fetches new data, it executes an event handler, like navigation, to take a user to the next step in a flow. When a data resource successfully adds a record to a table, it shows a success modal that uses the show modal event handler. For more information, see [Bind an event to a data resource](../task/bind-event-data-resource.md).

## Binding events to declarative actions in UI Builder

Bind data elements to add event actions to a declarative action definition in **Actions &amp; Components** in the ServiceNow AI Platform®. For example, you could bind a data element to add an event action to complete work on a table.

If you add a component to your UI Builder page that has a declarative action, you must bind it to a handled event. The handled event creates an action that is performed when a user selects the component. By selecting **Configure declarative action event mapping**, you add a new event handler to define what the declarative action does on the page.

![Configure the declarative action event mappings option in the Configure panel.](../image/declarative-action-config.png)

For more information, see [Bind an event to a declarative action](../task/bind-event-declarative-action.md).

-   **[Define map events](event-mapping.md)**  
An event mapping in UI Builder is the process that enables you to map an event's payload or contextual values to the object or handler that acts on that event. The four event types are: component, page, data resource, and declarative action.
-   **[Event payloads in UI Builder](event-payloads.md#)**  
Use event payloads to link data to an action.
-   **[Configure an event handler manually](../task/event-handler.md)**  
Add an event handler to a page, component, data resource, or declarative action within UI Builder so that your user can trigger an action.
-   **[Configure an event handler with Now Assist](../task/configure-an-event-handler-with-now-assist.md)**  
Use Now Assist in UI Builder to simplify the configuration of event handlers. At present, you can configure the following event handlers using Now Assist in UI Builder: Open page or URL, open or close modals, and viewport load requested.
-   **[Bind events to add actions](bind-events.md)**  
After you have created events, you can bind them to actions on your components, pages, data resources, and declarative actions.
-   **[Disable component preset event mappings](../task/disable-preset-event-mappings.md)**  
You can disable event mappings that are automatically created by a component preset.
-   **[Delete an event handler](../task/delete-event-handler.md)**  
Delete an event handler that you no longer need in UI Builder.
-   **[Delete an event mapping](../task/delete-event-mapping.md)**  
Delete an event mapping that you no longer need in UI Builder.

**Parent Topic:**[Working in UI Builder](using-ui-builder.md)

