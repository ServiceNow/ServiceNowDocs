---
title: Configure an event handler manually
description: Add an event handler to a page, component, data resource, or declarative action within UI Builder so that your user can trigger an action.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Configure an event handler manually

Add an event handler to a page, component, data resource, or declarative action within UI Builder so that your user can trigger an action.

## Before you begin

Role required: ui\_builder\_admin

## About this task

An event handler lets you configure an action, components, data resource, or declarative action on your page. For example, you can map an event to your page to add an alert notification when the page successfully loads or you can add an event handler for a button component to perform an action when a user clicks it. The event handler could also be a modal on your page that asks a user to verify that the user wants to delete the record. For more information, see [Manage actions in UI Builder pages](../concept/work-events.md).

**Note:** You can also use Now Assist in UI Builder to configure event handlers. For more, information, see [Configure an event handler with Now Assist](../../ui-generation/task/configure-an-event-handler-with-now-assist.md)

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Open or create a page.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  Add a component to your page, such as a button.

    For more information about adding components to a page, see [Add and configure components](add-components.md#).

5.  To add an event handler to your component's event, go to the configuration panel and select **Events**.

    An event handler lets you assign an event to a component. For example, if you add a button component to your page, you want it to perform an action when a user clicks it.

6.  To start the process of assigning an event to a component select **Add event mapping**.

    Some components, such as the button component, only have one event mapping. Other components can have many events.

7.  Select an event mapping that you want to configure from the list.

8.  From the Event handler preview screen, select an action that you want assigned to the component.

9.  Select **Continue**.

10. Select the handler you want to trigger from the event selected in the earlier step.

    ![Link to destination selected from the handler list.](../image/event-handler-select-list-link-dest.png)

11. Select **Continue**.

12. Configure the payload for the event.

    ![Event handler configured to open the list page.](../image/event-handler-configured.png)

13. Select **Add**.

14. Select **Save**.

15. Test the event by selecting **Preview** in the header and trigger the action.


## Result

The configured event handler displays in the events tab of the configuration panel.

**Parent Topic:**[Manage actions in UI Builder pages](../concept/work-events.md)

