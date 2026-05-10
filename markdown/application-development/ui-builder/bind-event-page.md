---
title: Bind an event to a page
description: Use page event mappings to bind data elements within UI Builder so that you can add event actions to your page.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Bind events to add actions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Bind an event to a page

Use page event mappings to bind data elements within UI Builder so that you can add event actions to your page.

## Before you begin

Role required: ui\_builder\_admin

## About this task

You can bind an event to a page by using the following types of events:

-   Page event mappings. Add, remove, or clear alert notifications on your page.
-   Variant event mappings. Add, remove, or clear alert notifications on your page variant.
-   Dispatched events. Create dispatched events for your page to create relayed event mappings that model events after a parent event handler. Select a target parent event handler to model the payload fields after it.
-   Handled events. A handled event is an event that is exposed and available for use by other users. After you create a handled event, it is available under **Page event mappings** for other users to use. You can also set up payload fields that you create manually or choose a template for your handled event, such as an open or close a modal dialog.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information.

3.  Open or create a page.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  Highlight the page body in the content tree.

    The body is the top-level line of the content tree. When you highlight the whole page, you can add page-level events.

    ![Arrow pointing at the body option in the content tree.](../image/content-tree-body.png)

5.  In the configuration panel, select the **Events** tab.

6.  Add an event handler in one of the following ways.

<table id="choicetable_tqw_v1s_znb"><thead><tr><th align="left" id="d117113e178">

To add this event handler

</th><th align="left" id="d117113e181">

Do this

</th></tr></thead><tbody><tr><td id="d117113e187">

**Page event mappings**

</td><td>

**Page ready** source event: 1.  Select **Add event handler**.
2.  To add, remove, or clear alert notifications from the page, choose an event handler from **Page-level event handlers**. You can add, remove, or clear alert notifications on your page.
3.  To add the event handler to your page, select **Add**.
 **Page property changed** source event: 1.  Select **Add a new event handler**.
2.  Choose an event handler from **Page-level event handlers**. You can add, remove, or clear alert notifications on your page. You can also choose **Set loading state** to show the word **Loading** on your page so users can see that the page is loading. You can also select **Update client state parameter** to change the client state name.
3.  To add the event handler to your page, click **Add**.


</td></tr><tr><td id="d117113e257">

**Variant event mappings**

</td><td>

**Variant event mappings** You must have a variant page to perform a variant event mapping. The Variant event mappings that are available depend on the variant page. If the variant page has a list, you add event handlers for things like Row clicked, Nav item, and so on. When the variant has a Viewport, you may have different event handlers to set up.

 1.  Select **Add event mappings**. For example, you can add a new event handler for **Row clicked**.
2.  Select an event handler from the list of available Inherited event handlers or local event handlers like the UXR App Shell Data Source.
3.  To add the event handler to your variant, select **Add**.
 ![Variant event handler options.](../image/variant-event-mappings.png)

 -   These event mappings are in the variant record that are found in the `sys_ux_screen` table.
-   The source events for these event mappings are any dispatched events that are defined for your page.
-   The available handlers for these event mappings are canvas-level events, the UXR App Shell Data Source, and operations from inherited data resources.
-   These event mappings are used as relays so that events that are dispatched from components on your page are relayed up to the user session handlers.
-   These mappings are automatically created on a page save when you have mapped a component's dispatched event to another event. For example, when you map a **Button clicked** event to the **Link to destination** event, the event creates a dispatched relay event and a variant event mapping after you save the page.


</td></tr><tr><td id="d117113e330">

**Dispatched events**

</td><td>

1.  Select **Dispatched events**.
2.  Select ![+Add icon.](../image/add-icon.png).
3.  In the **Add an event** screen, do the following actions:
    -   Type a label for your event.
    -   Select a target parent event handler.
4.  To add the event handler to your dispatched events, select **Add**.

![Create an event dialog.](../image/dispatched-page-events.png)

5.  The new event handler that you created appears in **Dispatched events**. The following example shows how to add a **Link to destination** event handler.

![Event handler added to dispatched events.](../image/dispatched-page-events-result.png)

 -   These events are in the \[sys\_ux\_event\] table. The page definition record contains references to the \[sys\_ux\_event\] record.

-   These events serve as source events for variant event mappings.

-   To create new dispatched events for your page, select ![+Add icon.](../image/add-icon.png). Configure the event label to auto-populate the event name and payload fields for your new `sys_ux_event`.

-   These events are often used to create relay event mappings. You can select a **Target parent event handler** to model the payload fields after the selected event. You can also manually create payload fields for your dispatched event.

</td></tr><tr><td id="d117113e437">

**Handled events**

</td><td>

-   These events are saved in the \[sys\_ux\_event\] table. The page definition record contains references to the \[sys\_ux\_event\] record.

-   These events serve as source events for Page event mappings.

-   To create new dispatched events for your page, select ![+Add icon.](../image/add-icon.png). These events are not modeled after parent event handlers. Payload fields for handled events are created manually. To use an existing handler's payload fields as a template, select a template and edit the fields as necessary.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  To preview your page and test the data resource event that you set up, select ![Preview button.](../image/preview-button.png).


**Parent Topic:**[Bind events to add actions](../concept/bind-events.md)

