---
title: Event payloads in UI Builder
description: Use event payloads to link data to an action.Use event payloads in UI Builder to share information between components on a page.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Event payloads in UI Builder

Use event payloads to link data to an action.

Event payloads are pieces of data sent by a component when a selected event is triggered. The data sent by an event can include the type of event, timestamps, user actions, or resource data such as a SysID. You can use event payloads in UI Builder to share information between components on a page.

You can use this payload data when configuring an event handler so that the resulting interaction can be linked to the emitted data. For example, a SysID can be passed to other components on a page to display information related to a specified record.

![Red box containing the available event payloads for the selected component.](../image/event-payloads-avaliable.png)

Each component and event has a unique set of payload options. Event payloads may not be properly defined for each component. If that is the case, define a client script so that the console logs payloads such as `console.log(event.payload)`.

**Parent Topic:**[Manage actions in UI Builder pages](work-events.md)

## Create an event with payloads to share information between components

Use event payloads in UI Builder to share information between components on a page.

### Before you begin

Role required: ui\_builder\_admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](work-experiences.md).

3.  Create or open a page.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](../task/create-page.md).

4.  Add a component that has events, such as the data visualization component.

    For more information about adding components to a page, see [Add and configure components](../task/add-components.md#).

5.  To add an event handler to your component, select the **Events** tab.

    For more information on how to add event handlers to your component, see [Manage actions in UI Builder pages](work-events.md).

    1.  To start the process of setting up an event handler for your component, click **Add event mapping**.

        ![Arrow pointing to add event mapping option.](../image/event-payloads-event-mapping-button.png)

    2.  Select the event mapping that you want to configure from the list.

        ![List of available event mappings for the data visualization component.](../image/event-payloads-select-event.png)

    3.  Select **Continue**.

    4.  From the Event handler preview section, select an event handler to bind to your component.

        ![Clear alert notifications when a row is clicked in a list.](../image/event-handler-add-page-level.png) ![Update client state parameter handler selected from the list.](../image/event-payloads-add-handler.png)

    5.  Select **Continue**.

    6.  Select the **Create a new client state parameter** from the **Client State Parameter Name** drop-down.

    7.  Enter a name in the **Name** field.

    8.  Select the type of client state parameter from the **Type** drop-down.

    9.  Enter a value in the **Initial value** field.

    10. Select the bind data icon in the **Value to use after triggering event** field.

        ![Arrow pointing to the bind data icon in the Value to use after triggering event field.](../image/event-payloads-select-bind-icon.png)

    11. Select the value you would like to bind to the triggered event.

        ![Bind data modal](../image/event-payloads-value-select-modal.png)

    12. Select **Apply**.

    13. Select **Add**.

        The data handler will appear below the event mapping in the events tab.

        ![Arrow pointing to the configured event handler for the data visualization component.](../image/event-payloads-configured-handler.png)

6.  Select the component you want to bind the client state parameter to, in this example we will be using a heading component.

7.  Select bind data icon in the field you want to bind the client state parameter to.

    ![Arrow pointing to the bind data icon in the label field of the heading component.](../image/event-payloads-bind-data-field.png)

8.  Select **Client states**.

9.  Select the arrow next to the client state parameter you want to bind.

    ![Arrow pointing to the arrow that binds a client state parameter to the label field.](../image/event-payloads-bind-csp.png)

10. Select **Apply**.

11. Select **Save**.

12. Select **Preview** to test your the event you just configured.


