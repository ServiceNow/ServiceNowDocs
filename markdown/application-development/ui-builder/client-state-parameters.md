---
title: Client state parameters
description: Use client state parameters to bind values to component configurations. When the client state parameter's value changes, the component updates to use the new value.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Client state parameters

Use client state parameters to bind values to component configurations. When the client state parameter's value changes, the component updates to use the new value.

## What is a client-side interaction

In web-based applications, anything that happens in the browser is client-side. Client-side interactions occur when users interact with experience components by clicking. Examples of client-side interactions include:

-   Clicking a button
-   Applying a filter
-   Sorting a list
-   Refreshing a list
-   Providing inline search results
-   Alerting a user to incomplete or incorrect data

![Examples of client-side interactions.](../image/client-side-interactions.png)

Users sometimes interact with pages in order to navigate to other pages. In other cases, users want to make updates to a page's content, appearance, or data. Rather than refreshing the entire page, client-side interactions update only the affected parts of a page.

![Pointer changing page content by selecting a filter.](../image/client-side-interaction-example.png)

For example, a user can sort a list by clicking a column header. Sorting redraws only the list and not the entire page.

Creating client-side interactions in UI Builder involves:

-   Client state parameters
-   [Events](event-mapping.md)
-   [Client scripts](../task/define-client-scripts.md)

## What are client state parameters

Client state parameters are page variables. Define and configure a client state parameter and use the value to configure components. Client state parameters centralize management of configuration values for page components. UI Builder uses client state parameters to enhance user experience and provide personalized content and services.

## Example of client state parameters

In the example, a page has a client state parameter called color. Two of the three components are configured to use the color client state parameter. If color is set to orange, the components are orange. If color is set to purple, the components are purple. If color is set to green, the components are green. The client state parameter is a single place to manage a common value for the page. Without the client state parameter, each component that uses a value would need to be updated individually if that value changed.

![Pages with different client state parameter color options.](../image/client-state-parameter-color.png)

For example, a web experience stores the primary color used by components in the color client state parameter. When the components are configured to use the client state parameter, changing the value of the client state parameter updates the components to the new value.

![Client state parameters setting the color for multiple components.](../image/client-state-parameter-button-color.png)

Buttons can be added to the experience to allow users to select a color for the page components. With a single click, a user can simultaneously change the color of all components on a page. Store the user’s color choice in a client state parameter, then use the client state parameter to configure the page’s components. When a user interaction causes the client state parameter value to change, the page’s components are updated in real time.

## The client state panel

The client state panel is collapsed by default. Click the client state icon in the left navigation bar to open the client state panel.

The client state panel contains two sections:

-   Client state parameters: The client state parameters for the page
-   Client state preview: The JSON for the page's client state parameters

![Arrows pointing to the two sections of the client state parameter panel.](../image/client-state-panel.png)

## Creating client state parameters

To add a client state parameter to a page, click the **+ Add** button in the client state parameters section.

![Client state panel with the +Add button highlighted.](../image/client-state-panel-add.png)

Client state parameters have three configuration fields.

-   Name: The name of the parameter. Names should not include spaces
-   Type: The parameter's type
    -   String
    -   Number
    -   Boolean
    -   JSON
-   Initial value: The default value for the parameter

In the example, the client state panel has two client state parameters.

-   `occasionTypeQuery` is a string with no default value
-   `occasionListTitle` is a string with a default value of `All Special Occasions`

![Client state parameters for special occasions.](../image/client-state-panel-example.png)

## Working with client state parameters

Once you have a client state parameter, what can you do with it? To work with client state parameters, first bind the value of the client state parameter to component configurations. When the client state parameter's value changes, the component updates to use the new value. One way to change a client state parameter's value is with event handlers.

In the creating client state parameters page example, two client state parameters were added to the special occasions application: `occasionTypeQuery` and `occasionListTitle`. The `occasionTypeQuery` parameter has no value by default and `occasionListTitle` has the default value `All Special Occasions`. These client state parameters will be applied to the Occasion List component to set the list's title and filter. A button will be used to update the values of these client state parameters to dynamically update the list.

![Client state parameters for special occasions.](../image/client-state-panel-example.png)

## Binding client state parameters

Client state parameter values can be bound to component configuration fields the same way page context, payload, and data resources are. When configuring components, hover over a field, then select the **Dynamic data binding** button \(![Dynamic data binding icon.](../image/uib-dynamic-data-binding-button.png)\) to bind a client state parameter to the field value. In the example, the **Dynamic data binding** button is highlighted for the Occasion List component's filter field.

![Bind data icon highlighted in the configuration panel.](../image/client-state-binding-button.png)

The character @ indicates data binding and the state object contains the client state parameters. Select a client state parameter from the choice list. The example shows selecting the `occasionTypeQuery` client state parameter. The default value for the `occasionTypeQuery` client state parameter is empty, so no filter will be applied by default.

![The occasionTypeQuery client state parameter is highlighted in the Filter configuration option.](../image/client-state-select-parm.png)

The Title for the component is set in a similar manner: select the **Dynamic data binding** button for the Title field or type @, then select the **state.occasionListTitle** client state parameter from the choice list. The default value for the `occasionListTitle` client state parameter is `All Special Occansions`. The example shows both Title and Filter configured to use client state parameters.

![Configuration panel showing that client state parameters are now bound to the Title and Filter fields.](../image/client-state-parm-selected.png)

With both client state parameters applied, no filter is applied to the list and the title is `All Special Occasions`.

![Arrows showing where client state parameters affect the configured list component.](../image/client-state-parm-applied.png)

The `occasionTypeQuery` and `occasionListTitle` client state parameter values remain unchanged until a user interacts with a component that changes the value of the client state parameter.

## Change client state parameter values

User the **Update client state parameter** event handler to change the value of a client state parameter in runtime. The **Update client state parameter** event handler has two properties: client state parameter to update and the new value to use for the client state parameter.

As an example, a `Birthdays` button is added above the `Occasion List` component in the `Special Occasions` application. The objective of this button is to change the `Title` of the list to `All Birthdays` and to adjust the filter of the list to only show birthdays. To achieve this objective, two event handlers are mapped to the **Button clicked** event for the button, one to change the `occasionTypeQuery` client state parameter and another to change the `occasionListTitle` client state parameter. The image shows the **Update client state parameter** event handler configured to set the `occasionTypeQuery` client state parameter to `special_occasion=birthday`, which will filter the list to only show birthdays.

![Update client state parameter highlighted in the event handler selection screen.](../image/client-state-update-event.png)

When the **Button clicked** event is mapped to event handlers to update both the `occasionTypeQuery` and `occasionListTitle` client state parameters, clicking the button updates the client state parameters, which automatically updates the `Occasion List` component with the new values.

![Button that updates the components filter to show specific occasions.](../image/client-state-button-event.png)

-   **[Using client state parameters in UI Builder](../task/create-simple-counter-component.md)**  
Create a simple counter by adding the stylized text component and two buttons to an experience page. Use a client state parameter to implement the functionality so that when the buttons are selected the count increases or decreases.
-   **[Update a component’s state using client state parameters](../task/state-parameters.md)**  
Create and bind a client state parameter value to a component in UI Builder. By adding custom values to your components, these components can then be automatically updated through a script.

**Parent Topic:**[Dynamically expose data in UI Builder pages \(advanced feature\)](data-resources.md)

