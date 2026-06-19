---
title: Create a UI interaction
description: Create a UI interaction and attach it to a component event in UI Builder. UI interactions are reusable flows that combine UI, logic, and scripts into a single unit, including custom UI built with Component Builder, and can be triggered from any component event on a page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/create-ui-interaction-show-alert.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
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

    \[Omitted image "uib-create-interaction.png"\] Alt text: Create drop-down menu with UI interaction selected.

3.  In the creation modal, enter a name for the interaction.

    \[Omitted image "uib-create-interaction-modal.png"\] Alt text: UI interaction creation modal

4.  Select an interaction Type.

    Generic interactions are used with no dependencies on form or list controller data. Form interactions use form-specific steps such as validating or saving a record. List interactions use list-specific steps such as refreshing or querying a list. If you're unsure, choose Generic.

5.  Enter a description that summarizes what the interaction does and when it runs.

    For example, `Displays a confirmation modal before deleting a record`.

6.  Select **Create**.

    \[Omitted image "uib-ui-interaction-editor.png"\] Alt text: UI interaction editor.

    The diagram editor opens with a start and end node connected by an add icon \[Omitted image "add-action-icon.png"\] Alt text:.

7.  Select the add icon \[Omitted image "add-action-icon.png"\] Alt text:between the start and end nodes to open the toolbox, then select a step to add it to the diagram.

    **Note:** The steps available in the toolbox depend on the interaction type that you selected.

    \[Omitted image "uib-ui-interaction-plus.png"\] Alt text: UI interaction editor with the step toolbox open.

8.  Select the step to open its properties in the configuration panel.

9.  Configure the step properties in the configuration panel.

    Properties vary depending on the step. For example, a modal step lets you set button labels and field content, while a script step lets you write server-side logic.

10. Repeat steps 7–9 to build out your interaction.

    Steps execute in sequence. To run steps in parallel, select the **And** step to create parallel branches. Each branch represents a separate path of steps and executes in order from top to bottom. To create conditional paths, add an **If/Else** step from the toolbox. This step creates branches that run when conditions are met. For more information, see [Edit an existing UI interaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/edit-ui-interaction.md).

11. Use the Inputs pill to add any data your interaction needs at runtime.

    Supported input types are: String, True/False, Choice, Reference, and JSON.

12. Select **Save**.


## Result

The UI interaction is created and ready to be attached to a component or page event. Once attached, it runs its configured steps whenever the specified event occurs. See [Trigger a UI interaction from a page event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/trigger-ui-interaction-from-page-event.md).

To trigger this UI interaction from a form or list button using a declarative action, see .

**Parent Topic:**[UI interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/uib-ui-interactions.md)

