---
title: Bind an event to a component
description: Bind data elements within UI Builder so that you can add event actions to your components.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Bind events to add actions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Bind an event to a component

Bind data elements within UI Builder so that you can add event actions to your components.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Each component has specific events that it binds to. For example, a button component has only a button-clicked event, while other components can have multiple events that are associated with them.

Some components do not have an event action that is applied to them. An example is the heading component. Many components require that you map an event to your component to make it perform an action, such as loading data.

To add actions to components, pages, and data resources on your page, you can add an event handler. A button component that you add to a page is static. By binding an event action to the button, you can link it to a web page.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Create or open a page.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  Add a component that has events to which it can bind to your page, such as a button.

    For more information about adding components to a page, see [Add and configure components](add-components.md#).

5.  To add an event handler to your component, select the **Events** tab.

    For more information on how to add event handlers to your component, see [Manage actions in UI Builder pages](../concept/work-events.md).

    1.  To start the process of setting up an event handler for your component, click **Add event mapping**.

        ![Arrow pointing to add event mapping option.](../image/event-handler-mapping-button.png)

    2.  Select the event mapping that you want to configure from the list.

        ![List of available event mappings.](../image/event-handler-list.png)

    3.  Select **Continue**.

    4.  From the Event handler preview section, select an event handler to bind to your component.

        ![Clear alert notifications when a row is clicked in a list.](../image/event-handler-add-page-level.png)

    5.  Select **Continue**.

    6.  Configure the payload for the event.

        You configure each event handler differently, depending on the action of the event. For example, if you add an event handler for a button component, you can choose what that button action performs.

    7.  Select **Add**.

6.  If you want a modal to pop up for your event, add the modal to the page before you bind your event to the component.

    A modal is a confirmation pop-up that appears when you click the component. For example, if you add a button component that deletes a record, you add a modal to ask the user to confirm that the user wants to delete the record. For more information, see [Add modal to component](modals-uib.md).

    1.  Select the **+** icon in the content tree next to **Modals**.

        ![Arrow pointing to the add new modal option.](../image/add-modal-selection.png)

    2.  Choose a modal type such as **Confirm**.

        ![Modal options with the confirm modal highlighted.](../image/add-modal-options.png)

    3.  Configure the modal.

        You can change the text in the modal, the names of the buttons in the modal, and the size of the modal screen. You can also set actions for the modal. When you finish configuring the modal, close it. Notice that the modal you created sits above the body of your page structure in the content tree.

7.  Bind an event to a button component.

    You bind an event to the button to trigger an action. Select the button component to highlight it again, either in the content tree, or on the page.

    1.  Select **+ Add content** in the content tree.

    2.  Select the **Button** component in the toolbox.

    3.  Select **None** when asked to choose a preset.

    4.  In the Configuration pane, click **Events**.

    5.  Select **Add handler**.

        ![Arrow pointing to the add event handler link for the button component.](../image/modal-button-event.png)

        The button component only has the button-clicked event associated with it. Other components can have more than one event.

    6.  Select an handler that you want assigned to the button.

        For example, to add an event handler for the button component, you could link it to another destination and add alert notifications. In this example, you can choose **Open or close modal dialog** to make the button open the modal that you created earlier. In this button scenario, select the Confirm and destroy modal dialog event handler that you created earlier.

        ![Event handler configuration screen showing the open or close modal dialog settings.](../image/modal-open-button-event.png)

    7.  Select **Continue**.

    8.  Select a modal from the drop-down.

    9.  Select **Add** to add the modal event handler to your button component.

8.  Click **Save**.

9.  Test the modal by selecting **Preview**.

10. To trigger the modal that you created, click the button on the page.


**Parent Topic:**[Bind events to add actions](../concept/bind-events.md)

