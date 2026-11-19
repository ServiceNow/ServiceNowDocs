---
title: Agent assist component setup
description: Agent Assist enables agents to receive automatic search results that show possible solutions for records they open.Properties in the Agent Assist component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/agent-assist-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Agent assist component setup

Agent Assist enables agents to receive automatic search results that show possible solutions for records they open.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Agent Assist that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "agent-assist-content-tree.png"\] Alt text: Shows the Agent Assist component in the UI Builder content tree

2.  Select the Agent Assist component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Agent Assist label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "agent-assist-presets.png"\] Alt text: Shows the list of available presets for the Agent Assist component and the option for selecting manual configuration

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "agent-assist-preset-config.png"\] Alt text: Shows the preset configuration panel and the properties required to connect this preset to its required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Agent assist component properties

Properties in the Agent Assist component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record agent assist__**

    This preset assists users in fulfilling a request by displaying related articles, incidents or cases, and recommending possible resolutions. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Table config
    -   Table
    -   Sys ID
    -   Form fields
    -   New record

### Properties

<table id="table_tkh_l2w_rnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table config\[cxsTableConfig\]

</td><td>

Contextual search table configuration.

</td></tr><tr><td>

Table\[table\]

</td><td>

Table name of the record on which agent assist appears.

</td></tr><tr><td>

Sys ID\[sysId\]

</td><td>

Sys ID of the record on which agent assist appears.

</td></tr><tr><td>

Form fields\[fields\]

</td><td>

Form fields to include from the record on which agent assist appears.

</td></tr><tr><td>

New record\[isNewRecord\]

</td><td>

Option to define if the record is a new record.Default: **false**

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Agent assist component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Agent Assist component. Events with presets are marked with the **Preset** badge. To show all events, select **+ Add event mapping**.

\[Omitted image "agent-assist-events.png"\] Alt text: Shows the list of agent assist events included with the preset, marked with the preset badge

### Event handlers

Event handlers work with data resources to link the Agent Assist actions to the data you want to display to your users. Select the event in the list to add one or more event handlers. For information about event handlers, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "agent-assist-events-add-handler.png"\] Alt text: Shows a preset event for Agent Assist with an event handler that adds alert notification to the action

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record agent assist__**

    This preset provides data handlers for these events:

    -   Save record
    -   Trigger form UI Action
    -   Set record value

### Event descriptions

|Event|Description|
|-----|-----------|
|Open record|Action to open a record in a Workspace sub tab.|
|Add notifications|Array of notification objects.|
|Save record|Action to save the current record.|
|Trigger form UI action|Action that triggers a form UI action.|
|Set record value|Action that sets a record value.|

