---
title: Add events to track components with unsaved changes
description: Locate dirty state components through event configuration.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [UI Builder, dirty state, unsaved changes, search events, components]
breadcrumb: [Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add events to track components with unsaved changes

Locate dirty state components through event configuration.

## Before you begin

Role required: ui\_builder\_admin

## About this task

You can add the **Screen status changed to dirty** event to check which components have unsaved changes. This avoids having to manually inspect advanced properties on events for each individual component. Once added, the event remains available in the configuration panel for direct access.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create or open a page.

4.  In the content tree, select **+ Add content** to add a component.

5.  Select a component from the toolbox and select **Add**.

    For example, select a **Button**.

6.  Add an event to the component.

    1.  Select the **Events** tab in the configuration panel.

    2.  Under **Button clicked**, select **Add handler**.

    3.  Under **Choose a handler**, enter `isDirty` \(or `dirty`\) into the search bar.

    4.  Select the **Screen status changed to dirty** event and select **Continue**.

        ![Choose a handler dialog showing "isDirty" typed into the search bar, with the "Screen status changed to dirty" event selected.](../image/dirty-state-event-select.png)

    5.  Select the **Screen is dirty** check box to mark the property as `true`.

    6.  Select **Add**.

    The dirty state event now appears in the configuration panel, enabling you to quickly check the `isDirty` property and determine if the component has unsaved changes without adding additional events.


**Parent Topic:**[Manage actions in UI Builder pages](../concept/work-events.md)

