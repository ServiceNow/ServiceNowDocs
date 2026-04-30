---
title: Bind an event to a data resource
description: Assign event handlers within UI Builder to individual data resources on your page. When a data resource successfully fetches new data, it executes an event handler to take a user to the next step in a flow.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Bind events to add actions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Bind an event to a data resource

Assign event handlers within UI Builder to individual data resources on your page. When a data resource successfully fetches new data, it executes an event handler to take a user to the next step in a flow.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Bind an event to a data resource, to perform data-related actions on your page. For example, you can add a button to reload data to a page if it doesn't load the first time. You can also set up a data resource event to reload data behind the scenes of your page.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Create or open a page.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  If you do not have any components on your page, add one to your page.

    For more information, see [Add and configure components](add-components.md#).

5.  Add a data resource to your page.

    For more information, see [Add and configure data resources to a page](add-data-resources.md).

6.  Select a data resource instance.

    ![Arrow pointing to the look up a single record data resource.](../image/data-resource-select-look-record.png)

7.  To add an event handler to your data resource, select the **Events** tab in the configuration panel of the data resource.

    You can add event handlers to your data resource to handle actions for Operation Initiated, Operation Succeeded, and Operation Failed.

    ![Events tab in data resources panel.](../image/data-resource-events.png)

8.  Select **Add event mapping**.

9.  Select an event from the list.

    ![List of events that can be bound to data resources.](../image/data-resource-events-list.png)

10. Select **Continue**.

11. Select an event handler from the list.

    ![List of event handlers that can be assigned to an event.](../image/data-resource-event-handler-list.png)

12. Select **Continue**.

13. Fill in the required information for the event handler.

    The configuration varies depending on which event handler is selected.

14. Select **Add**.

15. Select **Save**.

16. To preview your page and test the data resource event that you set up, select ![Preview button](../image/preview-button.png) in the UI Builder header.


-   **[Link an event to another page](link-component-destination.md)**  
Add a link to the destination event handler within UI Builder so that an event action can open another page. You can also configure the event handler to follow the App Route to the desired page.

**Parent Topic:**[Bind events to add actions](../concept/bind-events.md)

