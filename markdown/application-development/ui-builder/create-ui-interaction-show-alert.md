---
title: Create a UI interaction
description: Create a UI interaction and attach it to a component event in UI Builder. UI interactions are reusable flows that combine UI, logic, and scripts into a single unit, including custom UI built with Component Builder, and can be triggered from any component event on a page.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [UI interactions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a UI interaction

Create a UI interaction and attach it to a component event in UI Builder. UI interactions are reusable flows that combine UI, logic, and scripts into a single unit, including custom UI built with Component Builder, and can be triggered from any component event on a page.

## Before you begin

Role required: ui\_builder\_admin

## About this task

In this task, you create a UI interaction and define its behavior using the diagram editor. You select an interaction type, add and configure steps, define logic and branching, and specify inputs that the interaction requires at runtime.

**Important:** UI interactions don’t run on their own. After creating an interaction, you must attach it to a component or page event so it can run when that event occurs.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the UI Builder home page, select **Create** &gt; **UI interaction**.

    ![Create drop-down menu with UI interaction selected.](../image/uib-create-interaction.png "Create UI interaction")

3.  In the creation modal, enter a name for the interaction.

    For example, for a UI interaction to report a knowledge gap, you may enter `Report Knowledge Gap`. You can change the name in the UI interaction settings later.

    ![UI interaction creation modal](../image/uib-create-interaction-modal.png "UI interaction creation modal")

4.  Select an interaction Type.

    Generic interactions are used with no dependencies on form or list controller data. Form interactions use form-specific steps such as validating or saving a record. List interactions use list-specific steps such as refreshing or querying a list.

5.  Enter a description that summarizes what the interaction does and when it runs.

    For example, `Displays a confirmation modal before deleting a record`.

6.  Select **Create**.

    ![UI interaction editor.](../image/uib-ui-interaction-editor.png "UI interaction editor")

    The diagram editor opens with a start and end node connected by an add icon ![](../../flow-designer/images/add-action-icon.png). The steps available in the toolbox depend on the interaction type that you selected.

7.  Build your interaction by selecting the add icon ![](../../flow-designer/images/add-action-icon.png) between the start and end nodes to add steps from the toolbox.

    1.  Select **+** to open the toolbox.

        ![UI interaction editor with the step toolbox open.](../image/uib-ui-interaction-plus.png "UI interaction toolbox")

    2.  Browse the available steps by category, or search by name.

        When you add a first step between the Start and End nodes, the **And** branch appears in an Unavailable section within the toolbox. The **And** branch cannot be added until at least one step has been added to the main branch. When you insert a step between two existing steps, steps with no outgoing events, such as navigation steps, appear in an Unavailable section within the toolbox. These steps cannot be inserted before an existing step and must be added through an **And** branch, where they connect directly to the End node.

    3.  Select a step to add it to the canvas.

        Add a step between the start and end nodes, or insert one before any existing step. By default, when inserting a new step before an existing one, the flow continues with the topmost outgoing event. To change it, select the event node and choose a different event.

        **Note:** Each event supports a single outgoing branch. If you swap an event, any downstream bindings that depend on it reset to their default values, and a visual indicator shows the reset.

    4.  Configure the step properties in the configuration panel.

    5.  Repeat to add additional steps in sequence.

        To run steps in parallel, select the select the **And** step from the toolbox. Branches execute in order from top to bottom. To define conditional paths, add an **If/Else** step from the Logic section of the toolbox. When you insert an **If/Else** step before an existing step, the system preserves the downstream flow in the Else branch.Conditions can be defined using formula building or a script. Branches are evaluated top to bottom and the first branch that evaluates to true executes.

    6.  If your interaction requires data at runtime, define inputs by selecting the Inputs pill and adding the data your interaction needs.

        Supported input types are: String, True/False, Choice, Reference, and JSON.

    7.  Select **Save**.

    8.  Delete a step from the interaction at any time by selecting the delete icon ![](../image/uib-delete-event-mapping-icon.png).

    9.  To delete an event on the diagram, select the delete icon ![](../image/uib-delete-event-mapping-icon.png) on the event.

        Deleting an event removes the connection and any downstream steps.


## Result

The UI interaction is created and ready to be attached to a component or page event. Once attached, it runs its configured steps whenever the specified event occurs. See [Trigger a UI interaction from a page event](trigger-ui-interaction-from-page-event.md).

To trigger this UI interaction from a form or list button using a declarative action, see [Trigger a UI interaction from a declarative action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-da-ui-interactions.md).

**Parent Topic:**[UI interactions](../concept/uib-ui-interactions.md)

