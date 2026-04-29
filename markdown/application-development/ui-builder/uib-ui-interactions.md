---
title: UI interactions
description: Trigger UI interactions directly from events in UI Builder, allowing you to link event-driven behavior to reusable interaction logic.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# UI interactions

Trigger UI interactions directly from events in UI Builder, allowing you to link event-driven behavior to reusable interaction logic.

UI interactions are reusable flows that combine UI elements and logic into a single unit you can trigger from component events in UI Builder. They help you avoid repeating the same wiring across multiple pages and make your designs easier to maintain.

## Why use UI interactions

-   **Reduced duplication**: Instead of creating separate actions for every component, you define the flow once and reuse it.
-   **Improve consistency**: Interactions ensure the same behavior across multiple pages or experiences.
-   **Simplify maintenance**: Changes to an interaction automatically apply wherever it’s used.

**Note:** If you want record-based, sequential UI and desire a long-running process, consider using Playbook.

## Practical uses for UI interactions

-   Trigger a confirmation dialog when a user selects a button
-   Show an alert message after a record is saved
-   Show a form view inside a modal when validation fails
-   Chain multiple steps together such as updating data followed by displaying a success message

## UI interaction workflow

A UI interaction defines a reusable flow of user and system actions. At a high level, every interaction works this way:

1.  Inputs: a configurable piece of data that a UI interaction needs to run. Supported types include string, true/false, choice, reference, and JSON. Inputs can be defined upfront or promoted from a step property.
2.  Trigger: a component, declarative action, or event starts the interaction and passes inputs.
3.  Start: one or more start nodes determine where execution begins.
4.  Steps: the interaction runs its steps in sequence, optionally branching with events or parallel And paths.
5.  End: execution reaches an End node, completing the flow.

![UI interaction workflow.](../image/uib-uii-workflow.png "UI interaction workflow example")

## How UI interactions differ from declarative actions

Declarative actions determine where and when an action appears, most commonly on a form or list. UI interactions encapsulate what happens and can be triggered by any page event or declarative action. Here’s a list of key differences:

-   Declarative actions place buttons on lists and forms without requiring modifications of the page.
-   UI interactions define the end‑to‑end behavior of UI, logic, and script when triggered.
-   Declarative actions can trigger UI interactions.
-   Declarative actions could be implemented as UI interactions instead of UXF client actions, since they work without page ownership or modification, even when triggering UI like modals.

## Triggers for UI Interactions

You can run a UI interaction from several entry points, depending on the use case:

-   **Declarative action**: ideal when you need a button on a form or list without page customization.
-   **UI Builder page events**: trigger interactions from buttons, component events, or custom UI behavior within a page.

## UI interaction types

When you create an interaction, you choose a type that determines the context it works with:

-   **Generic**: works with any component
-   **Form**: designed for form-specific behaviors such as save, validate, and scripting
-   **List**: tailored for list-based actions such as list refresh and scripting

## UI interaction toolbox

The toolbox provides all building blocks available inside the UI interaction editor, including:

-   UI elements like modals, modeless dialogs, and dynamic forms
-   Custom components with Component Builder
-   Logic steps such as conditions, if/else branches, and navigation
-   Form or list actions, when available for that interaction type
-   Client and server script steps
-   Data-binding inputs and configurable properties

**Note:** Toolbox components depend on the interaction type such as form, list, or generic.

![UI interactions toolbox.](../image/uib-uii-toolbox.png "UI interactions toolbox example")

-   **[Create a UI interaction](../task/create-ui-interaction-show-alert.md)**  
Create a UI interaction and attach it to a component event in UI Builder. UI interactions are reusable flows that combine UI, logic, and scripts into a single unit, including custom UI built with Component Builder, and can be triggered from any component event on a page.
-   **[Trigger a UI interaction from a page event](../task/trigger-ui-interaction-from-page-event.md)**  
Attach a UI interaction to a UI Builder page event so the interaction runs when a user performs an action on a component.
-   **[Delete a UI interaction](../task/delete-ui-interaction.md)**  
Delete a UI interaction when it’s no longer needed or when you must replace it with a new version. Although UI interactions can be edited after creation, some foundational properties are intentionally locked to avoid data and runtime errors. In those cases, deletion might be required.
-   **[UI interaction toolbox steps](../reference/uib-ui-interaction-steps.md)**  
Find details about UI interaction toolbox steps, organized by interaction type, with step descriptions and any available outgoing events. Steps are added to a UI interaction using the toolbox in the UI interaction editor. The available steps depend on the type you selected when you created the UI interaction, whether Generic, Form, or List.
-   **[Working with UI interaction demo data](working-with-demo-interactions.md)**  
Demo UI interactions give you simple, ready‑made examples that demonstrate common UI Interaction patterns. You can duplicate these samples to explore how interactions work, experiment safely, and use them as starting points when building your own experiences.

**Parent Topic:**[Manage actions in UI Builder pages](work-events.md)

