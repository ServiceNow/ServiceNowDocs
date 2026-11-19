---
title: Action Bar component setup
description: The Action Bar component is used to provide one or more UI elements tied to events that users can trigger. Action items can appear as buttons or as overflow menu items.Properties in the Action Bar component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/action-bar-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Action Bar component setup

The Action Bar component is used to provide one or more UI elements tied to events that users can trigger. Action items can appear as buttons or as overflow menu items.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Action Bar that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "action-bar-content-tree.png"\] Alt text: Shows the Action Bar component in the UI Builder content tree for navigating to the configuration panel

2.  Select the Action Bar component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Action Bar label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "action-bar-presets.png"\] Alt text: Shows the list of presets available with the Action Bar component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

    \[Omitted image "action-bar-preset-config.png"\] Alt text: Shows the input fields for configuring the preset to connect to the required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Action bar component properties

Properties in the Action Bar component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record action__**

    This preset lists an array of action items that let users interact with and take common actions on a page. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Actions
    -   Declarative action form model

### Properties

<table id="table_x5k_rbz_wtb"><thead><tr><th>

Label/property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Actions\[actionNodes\]

</td><td>

Array of actions.

</td></tr><tr><td>

Declarative action form model\[daModel\]

</td><td>

Object that stores form states to evaluate or execute a declarative action.

</td></tr><tr><td>

Declarative action contract\[daClientActionContract\]

</td><td>

Object that stores declarative action context variables and an array of UX event definitions.

</td></tr><tr><td>

Number of anchored buttons\[fixedButtonNumber\]

</td><td>

Minimum number of anchored buttons that should be displayed without overflow.

</td></tr></tbody>
</table>### Manual configuration

To configure the properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Action bar component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Action Bar component, marked with the **Preset** badge.

\[Omitted image "action-bar-event-handler.png"\] Alt text: Shows the list of events available with presets for the Action Bar component

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record action__**

    This preset provides data handlers for the **Request Refresh** event.


### Event descriptions

<table id="table_gj4_xmt_snb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request Refresh

</td><td>

Action dispatched on successful declarative action execution for server script action. **Note:** This action is only dispatched when the action bar contains declarative actions with server script type.

</td></tr></tbody>
</table>