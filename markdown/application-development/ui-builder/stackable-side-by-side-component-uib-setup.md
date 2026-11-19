---
title: Stackable Side by Side Panel component setup
description: The Stackable Side by Side Panel is a container used to display 2 components side-by-side \(50%,50%\) or stacked \(100%,100%\). This container has presets inherited from the UI page controller when used with the Activity Stream and Activity Stream Compose components.Properties in the Stackable Side by Side Panel component have preset configuration values when used as a container for the Activity Stream and Activity Stream Compose components. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/stackable-side-by-side-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Stackable Side by Side Panel component setup

The Stackable Side by Side Panel is a container used to display 2 components side-by-side \(50%,50%\) or stacked \(100%,100%\). This container has presets inherited from the UI page controller when used with the Activity Stream and Activity Stream Compose components.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Stackable Side by Side Panel that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "stackable-side-by-side-content-tree.png"\] Alt text: Shows the stackable side by side panel component in the UI Builder content tree

2.  Select the Stackable Side by Side Panel component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Stackable Side by Side Panel label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "stackable-side-by-side-presets.png"\] Alt text: Shows the list of available presets for the stackable side by side panel component

3.  Select either **None** to configure the component properties manually, or select the preset for the UI Controller Record Page to use pre-configured properties and events.

    No configuration is necessary with this controller. The Stackable Side by Side Panel component is automatically configured to use the UI page controller when the preset is selected.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Stackable Side by Side Panel component properties

Properties in the Stackable Side by Side Panel component have preset configuration values when used as a container for the Activity Stream and Activity Stream Compose components. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record stackable side by side panel for activity stream combo__**

    This preset provides slots for the Activity Stream and Activity Stream Compose components that can be displayed side-by-side or stacked. This preset requires the **UI Controller Record Page** controller.

    Properties included in this preset are:

    -   Mode
    -   Minimum width required to display side-by-side
    -   Use available height

### Properties

<table id="table_tab_6di_olq"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Initial mode\[initialMode\]

</td><td>

Initial display mode to use to render the component before the component automatically detects which mode is recommended for the available space. The choices are: Auto, Stacked, or Side by sideDefault: **Stacked**

</td></tr><tr><td>

Mode\[mode\]

</td><td>

Display mode for the components. When set to **Auto**, the layout changes based on the available space. When set to **Stacked**, components are stacked regardless of the available space.

</td></tr><tr><td>

Minimum width required to display side-by-side\[sideBySideMinWidthPx\]

</td><td>

Minimum width in pixels required to display components in side-by-side mode.Default: **700**

</td></tr><tr><td>

Use available height\[useAvailableHeight\]

</td><td>

Sets whether the components fill the entire available height of the panel.

</td></tr></tbody>
</table>To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**:Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Stackable Side by Side Panel component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required.

The Events tab shows the events used by the Stackable Side by Side Panel component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**. If the component has only one event, and that event doesn't have a preset, the event is displayed, ready for configuration.

\[Omitted image "stackable-side-by-side-events.png"\] Alt text: Shows the events available in the preset for stackable side by side panel

### Event handlers

Event handlers work with data resources to link the Stackable Side by Side Panel actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record stackable side by side panel for activity stream combo__**

    This preset provides data handlers for the **Mode recommended** event.


### Event descriptions

<table id="table_5ui_lag_naf"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mode recommended

</td><td>

The component has detected a new recommended mode and/or side-by-side availability.Payload:

-   `recommendedMode`: Recommended mode, can be stacked or side-by-side depending on available width.
-   `canSwitchMode`: Is there enough space for the mode to be changed? Default: **false**

</td></tr></tbody>
</table>