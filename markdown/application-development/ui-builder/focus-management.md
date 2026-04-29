---
title: Enhance accessibility with focus management
description: Set focus on specific elements, ensuring users can interact with them effectively using screen readers.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Enhance accessibility with focus management

Set focus on specific elements, ensuring users can interact with them effectively using screen readers.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Focus management can help users navigate experiences built with UI Builder by directing their attention to specific elements on a page. For example, you can point to a component when closing a modal that updated information on a parent page.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  Select a component from the content tree that you want to trigger the focus.

5.  Select the **Events** tab.

6.  Select **Add event mapping**.

7.  Choose an event from the list.

8.  Select **Continue**.

9.  Specify the type of focus you want to trigger with the event.

    Select **Set focus on** to direct users to a specific component on your page.

    Select **Focus parent page** to direct users to the parent page of a modal, pop-up, or similar overlay.

    ![List of event handlers showing Set focus on.](../image/set-focus-option.png)

10. Select **Continue**.

11. Select the component you want to focus on from the **Set focus on** list.

    ![Simple List component selected in the set focus on field.](../image/set-focus-list.png)

12. Select **Add**.

13. Select **Save**.


**Parent Topic:**[Customize UI Builder pages using components](../concept/work-components.md)

