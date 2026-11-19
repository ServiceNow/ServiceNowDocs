---
title: Display Value Block component setup
description: The Display Value Block component displays view-only record content to a user in portal pages and applications, using a configurable accordion.Properties in the Display Value Block component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/display-value-block-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Display Value Block component setup

The Display Value Block component displays view-only record content to a user in portal pages and applications, using a configurable accordion.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Display Value Block that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "display-value-block-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Display Value Block component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Display Value Block label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "display-value-block-presets.png"\] Alt text: Shows the list of presets for display value block and the selection for manual configuration

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "display-value-block-preset-config.png"\] Alt text: Shows the preset configuration panel that connects the preset to the required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Display Value Block component properties

Properties in the Display Value Block component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record secondary values__**

    This preset displays relevant, read-only fields that provide the necessary context for users to perform their tasks. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Items
    -   Layout type
    -   Hide labels
    -   Display inline
    -   Max lines per value
    -   Rows before toggle shown

### Properties

<table id="table_nwz_jqr_nnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title\[table\]

</td><td>

Title of the component displayed at top-left in a header tag.

</td></tr><tr><td>

Items\[items\]

</td><td>

Array of label-value items. Labels can have one or more values. Values can be rendered as a string, text link, or highlighted value.

</td></tr><tr><td>

Layout type\[layoutType\]

</td><td>

Property to position label-value items in relation to each other. The possible choices are:-   `vertical`: Displays label-value pairs stacked
-   `horizontal`: Displays label-value pairs side-by-side.
-   `horizontal-equal`: Displays label-value pairs side-by-side, expanding to equally fill its parent container.

</td></tr><tr><td>

Delimiter\[delimiter\]

</td><td>

Character displayed as a delimiter between label value pairs.

</td></tr><tr><td>

Hide labels\[hideLabels\]

</td><td>

Option to hide labels. If this property is set to **true**, the `displayInline` property is hidden.Default: **false**

</td></tr><tr><td>

Display inline\[displayInline\]

</td><td>

Option to display labels and values side-by-side rather than stacked. This property is not available if the `hideLabels` property is set to **true**.Default: **false**

</td></tr><tr><td>

Max lines per value\[maxLinesPerValue\]

</td><td>

Maximum number of lines for a text type value before it truncates. To prevent truncation, enter a value of 0.

</td></tr><tr><td>

Rows before toggle shown\[rowsBeforeToggleShown\]

</td><td>

Number of rows to render on the screen. If the number of actual rows is greater than the value of this property, excess rows are hidden.

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Display Value Block component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Display Value Block component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**. If the component has only one event, and that event doesn't have a preset, the event is displayed, ready for configuration.

\[Omitted image "display-value-block-events.png"\] Alt text: Shows a single event for the display value block that doesn't have a preset. The control for adding an event handler is already displayed

### Event handlers

Event handlers work with data resources to link the Display Value Block actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record secondary values__**

    This preset doesn't have any events.


### Event descriptions

<table id="table_pp2_lqr_nnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Link Clicked

</td><td>

User selects an item of type `text-link`. The action contains all the data for the item representing the text-link selected.Payload contains `item`: Item representing the clicked text-link

-   `label`
-   `value`

</td></tr></tbody>
</table>