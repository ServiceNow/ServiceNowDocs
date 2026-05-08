---
title: Event handler generation
description: Now Assist event handler generation enables you to configure event handlers for UI components using natural language, eliminating the need for manual configuration of complex routing parameters and binding expressions.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [Explore, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Event handler generation

Now Assist event handler generation enables you to configure event handlers for UI components using natural language, eliminating the need for manual configuration of complex routing parameters and binding expressions.

In UI Builder, event handlers define how a component responds to user interactions, such as a button select or a reference link selection. Configuring these handlers manually requires knowledge of specific parameters, page routing structures, and binding syntax — all of which can be time-consuming and error-prone, particularly for developers who are new to the platform.

With Now Assist event handler generation, you describe the desired behavior in plain language. Now Assist interprets the prompt, identifies the correct destination page or URL, maps any required parameters, and generates a complete configuration. You review the result before applying it, and you can edit any field using the standard form controls before saving.

## Benefits

Now Assist event handler generation provides the following benefits:

-   **Faster configuration**

    Natural language input replaces manual form-filling, significantly reducing the time needed to set up event handlers.

-   **Reduced complexity**

    Now Assist interprets intent and populates routing parameters, destination pages, and bindings automatically.

-   **Intelligent parameter binding**

    Now Assist can bind page parameters dynamically from state parameters or event payloads, enabling context-aware navigation without manual binding expressions.

-   **Contextual sample prompts**

    The Now Assist panel displays relevant sample prompts based on the pages and components available in the current experience, so you can start quickly without composing a prompt from scratch.

-   **Human review before applying**

    Generated configurations are presented as a read-only preview before being committed. Developers can accept and edit, or reject and re-prompt, ensuring accuracy at every step.


## How Now Assist generates event handler configurations

When you add an event handler to a component in UI Builder and open the Now Assist configuration panel, the system presents a text field where you describe the behavior you want. You can enter your own prompt or select from the sample prompts displayed.

Now Assist processes the prompt against the available pages, parameters, and event payloads in the current experience and generates a configuration. The result is displayed as a read-only preview. You review the destination, parameter bindings, and trigger settings, then choose to accept and edit, or reject the result.

If you accept, the configuration is applied to the component. You can continue editing individual fields using the standard form controls before selecting **Add** to save the handler.

## Supported event handlers

Now Assist event handler generation supports the three most commonly used event handlers in UI Builder:

-   **Open page or URL**

    The Open page or URL event handler navigates the user to a page when a component event triggers. The destination can be a page within the current experience or an external URL.

    For pages in the current experience, you select the target page and provide any required parameters, such as a table name or sys\_id. For external URLs, you enter the full URL. Both destination types support an **Open in new tab** option.

    Parameters can be bound statically or dynamically from state parameters or event payload fields. Advanced mode exposes additional binding fields for route, fields, and params.

-   **Open and close modal dialog**

    The Open and close modal dialog event handler opens or closes a modal dialog in the current experience when a component event triggers. Now Assist can configure this handler based on a natural language description of which dialog to open or close and under what conditions.

-   **Viewport load requested**

    The Viewport load requested event handler triggers the loading of a specific viewport within the experience when a specified event triggers. Now Assist can configure this handler based on a natural language description of the target viewport and the triggering event.


## Event payloads and parameter binding

Some component events dispatch a payload — a set of data values emitted by the source component when the event triggers. When a payload is available, Now Assist can bind destination parameters directly to payload fields, enabling fully dynamic navigation without any static values.

For example, the Reference link clicked event on a list component dispatches the following payload fields: `listTable`, `nativeEvent`, `record_id`, `row`, `sys_id`, and `table`. Now Assist can map these fields to the corresponding parameters of a record page destination automatically, so that selecting any reference link in the list opens the correct record.

When an event has no payload — such as the Button clicked event — parameters must be bound from state parameters or entered as static values.

**Parent Topic:**[Exploring UI generation](exploring-ui-generation.md)

**Related topics**  


[Configure an event handler with Now Assist](../task/configure-an-event-handler-with-now-assist.md)

[Use case: Configure an event handler with Now Assist](use-case-event-handler-generation.md)

