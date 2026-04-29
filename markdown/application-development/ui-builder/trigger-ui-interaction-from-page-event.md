---
title: Trigger a UI interaction from a page event
description: Attach a UI interaction to a UI Builder page event so the interaction runs when a user performs an action on a component.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [UI interactions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Trigger a UI interaction from a page event

Attach a UI interaction to a UI Builder page event so the interaction runs when a user performs an action on a component.

## Before you begin

You have already created a UI interaction that you want to trigger.

Role required: ui\_builder\_admin

## About this task

UI interactions don’t run on their own. To execute an interaction, you must attach it to an event that occurs on a page or component. UI interactions are triggered by page events, including events mapped from component actions.

In this task, you configure a component event on a page to trigger an existing UI interaction.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    For more information, see [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md).

3.  Create or open a page within the experience.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  Select the component that should trigger the interaction.

    If the page doesn’t already include the component you want to use, add it to the page first. For more information about adding components to a page, see [Add and configure components](add-components.md#).

5.  In the component configuration panel, select the **Events** tab.

    ![Button selected on a page, with Events tab displayed.](../image/uib-uii-event-tab.png "Events tab")

6.  Select **Add handler**.

7.  Search for your UI interaction by name, or select the **UI interactions** pill to filter results.

8.  Select the UI interaction that you want to trigger.

    **Note:** If your interaction type is Form or List and the applicable controller isn’t already on the page, it is added automatically. If multiple controllers exist on the page, you’re prompted to choose which one feeds data to the interaction.

    ![Add handler modal with UI interaction selected.](../image/uib-uii-select-a-response.png "Add handler modal")

9.  Select **Add**.

10. Select **Save**.

11. Select **Preview**, then perform the action that fires the configured event to verify the interaction runs.


## Result

When the specified page event occurs, the UI interaction runs and executes its configured actions.

**Parent Topic:**[UI interactions](../concept/uib-ui-interactions.md)

