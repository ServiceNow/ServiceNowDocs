---
title: Configure an event handler with Now Assist
description: Use Now Assist in UI Builder to configure event handlers. At present, you can configure link to destination, open or close modal, and view load requested event handlers using Now Assist in UI Builder.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Configure an event handler with Now Assist

Use Now Assist in UI Builder to configure event handlers. At present, you can configure link to destination, open or close modal, and view load requested event handlers using Now Assist in UI Builder.

## Before you begin

Role required: ui\_builder\_admin

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

6.  In the event handler, select **Link to destination** and select **Continue**.

7.  In the Configure section, select **Get Started**.

8.  In the **Generate configuration with Now Assist** field:

    -   Type the action you want to perform \(For example, open www.servicenow.com\) or select an option from the dynamic prompts.
    -   You can reference data from page context.
    ![Generate configuration with Now Assist](../image/event-handler-NowAssist.png)

9.  Select the right arrow icon.

    The configurations are set.

10. You can either reject, or accept and edit the configurations.

11. After you review the changes, select **Add**.

12. Test the event by selecting **Preview** in the header and trigger the action.


## Result

The event handler configurations are updated.

**Parent Topic:**[Manage actions in UI Builder pages](../concept/work-events.md)

