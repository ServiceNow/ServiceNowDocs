---
title: Update a component’s state using client state parameters
description: Create and bind a client state parameter value to a component in UI Builder. By adding custom values to your components, these components can then be automatically updated through a script.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Client state parameters, Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Update a component’s state using client state parameters

Create and bind a client state parameter value to a component in UI Builder. By adding custom values to your components, these components can then be automatically updated through a script.

## Before you begin

Role required: ui\_builder\_admin

## About this task

You can add two components to a page and then connect them by using [client state parameters](../concept/ui-builder-glossary.md#) and [scripts](../concept/ui-builder-glossary.md#). Start by creating a client state parameter and then binding the client state parameter to one of the components, such as a label. Next, you create a client script and bind it to a second component, such as a button, using an event handler. When you create the event handler, bind the client state parameter value to it to connect the two components. If you click one component, it changes the state of the other component. Client states are useful because you can add custom values to your components that can be automatically updated through a script. Think of a client state as a bucket for storing information that is specific to the page.

For example, you can add a button and label component to your page. The button changes the value of the label, such as changing the text color.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create or open a page.

    For more information, see [Manage UI Builder pages and page variants](../concept/work-pages.md).

4.  Add two components to your page.

    For more information, see [Add and configure components](add-components.md#).

5.  To define a client state parameter with an associated value, select Client state parameters in the lower-left panel.

6.  Select **+ Add**.

7.  Enter a name for the client state name, type, and initial value.

    The client state supports Strings, Numbers, Boolean, and JSON. For example, you could enter the name as `dynamic_label_value`, the type as `String`, and the initial value as `Initial Value`.

8.  Bind the value of the client state parameter to your component.

    1.  Select the component that you want to bind the client state parameter to.

    2.  Open the configuration panel and select the **Configure** tab.

    3.  Point to the field that you want to bind data to and select the dynamic data binding icon \(![Dynamic data binding icon.](../image/uib-dynamic-data-binding-button.png)\).

        ![Hovering over the bind data icon.](../image/data-bind-icon-hover.png)

        The data binding modal appears.

    4.  Select **Client states** in the **Data types** tab.

    5.  Double-click the client script that you want to bind to the component.

    6.  Select **Apply**.

9.  Select **Save**.

10. Bind the client state value to one component and create a script to connect the second component to the first.

    1.  In the left pane, select the **+** icon next to **Client scripts**.

    2.  Enter a script name that describes the task.

        For example, you could enter `Update Label Value` because that is what you want the script to do.

    3.  In the Now Code Editor, add your script.

        Let's say that you choose an API to call, and the parameters for the API, such as a state and a value. For example, you could call the `api.setState`, and include the`dynamic_label_value` as the first parameter, and a `NEW VALUE` as the second parameter.

11. Add an event handler to your second component to call the new client script that you created.

    1.  Select the component on your page that you want to bind the script to.

    2.  Select the **Events** tab.

    3.  Select **+ Add a new event handler**.

    4.  Under the Scripts section of event handlers, select the script that you created, and select **+** to add it as an event handler for the component.

        ![Adding the script as an event handler.](../image/client-script-add-to-event.png)

12. Select **Save**.

13. To preview your page and test the components to ensure they’re connected, select **Preview**.

    When you select one component, it should change the state of the second component. For example, select the **Button** component to change the **Label value** component text from **Initial Value** to **NEW VALUE**.


## Result

What you did in this procedure:

-   Added two components to your page.
-   Defined a client state parameter that had an initial value.
-   Bound the client state parameter to the first component.
-   Created a client script that updates a value that is defined by the client state parameter.
-   Created an event handler for the second component to call the new client script that you just created
-   Selected the second component so that it changed the state of the first component.

**Parent Topic:**[Client state parameters](../concept/client-state-parameters.md)

