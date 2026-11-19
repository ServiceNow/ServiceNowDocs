---
title: Ribbon component setup
description: The Ribbon component is a container to display graphical control components that have been configured for a record type.Properties in the Ribbon component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/ribbon-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Ribbon component setup

The Ribbon component is a container to display graphical control components that have been configured for a record type.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Ribbon that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Work with pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "ribbon-content-tree.png"\] Alt text: Shows the Ribbon component in the content tree in UI Builder

2.  Select the Ribbon component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Action bar label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "ribbon-presets.png"\] Alt text: Shows the list of presets available for the Ribbon component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a preset for a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "ribbon-preset-config.png"\] Alt text: Shows the configuration panel for connecting the preset to the required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Ribbon component properties

Properties in the Ribbon component have preset configuration values. You can accept these values or override them manually.

Presets are designed to suit a specific use case. However, you can override a property that has a preset value with a custom configuration, if you find it necessary for your design. For details on overriding and resetting presets, see [Override a preset for a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record ribbon__**

    This preset provides customer and record information, such as contacts and SLAs. This preset requires the **Ribbon** controller.

    Properties included in this preset are:

    -   Table
    -   Sys ID
    -   Widgets
    -   Active
    -   Is Visible
    -   Openframe configured

### Properties

<table id="table_dea_dma_ns3"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

Table name for the record.

</td></tr><tr><td>

Sys ID\[sysId\]

</td><td>

Sys ID for the record.

</td></tr><tr><td>

Widgets\[widgets\]

</td><td>

Collection of widgets to display on the ribbon.

</td></tr><tr><td>

Active\[active\]

</td><td>

When set to **true** the record is active.Default: **true**

</td></tr><tr><td>

Is Visible\[isVisible\]

</td><td>

Option to disable collapsed Ribbon container and the container is visible on the form.Default: **true**

</td></tr><tr><td>

Collapsed\[collapsed\]

</td><td>

Option to enable collapsed state for ribbon container.Default: **false**

</td></tr><tr><td>

Orientation\[orientation\]

</td><td>

Determines the orientation of the widgets on the ribbon.Default: **horizontal**

</td></tr><tr><td>

Openframe configured\[isOpenframeConfigValid\]

</td><td>

Indicates whether or not Openframe is configured. When the Openframe plugin is active, a phone icon appears on a list or record. A user viewing the record can select this icon to initiate an outbound call to another user's business phone number.Default: **false**

</td></tr><tr><td>

Transparent background\[transparentBackground\]

</td><td>

When set to **false**, ribbon container background color is transparent

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Links the property to data from another component, using data resources. For details, see [Connect data to your components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/connect-data.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Define and bind client scripts to components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/define-client-scripts.md).

## Ribbon component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Ribbon component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**. If the component has only one event, and that event doesn't have a preset, the event is displayed, ready for configuration.

\[Omitted image "ribbon-events.png"\] Alt text: Partial list of events for the Ribbon showing the badge that identifies events with presets

### Event handlers

Event handlers work with data resources to link the Ribbon actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record ribbon__**

    This preset provides data handlers for these events:

    -   Open Phone
    -   Preview Record
    -   Add Notification
    -   Remove notifications
    -   Clear notifications
    -   Item selected
    -   Execute UI Actions
    -   Wrapped Action

### Event descriptions

<table id="table_om4_b2c_5nb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open Phone

</td><td>

Action dispatched to open the phone feature.Payload:

-   type: Type. The default is OPEN\_PHONE
-   table: Table to which the record being previewed belongs
-   tableName: Table label to which the record being previewed belongs
-   sysId: Sys ID of the record being previewed
-   phoneNumber: The phone number to dial
-   displayValue: Text value used to represent the record, such as a title, if applicable

</td></tr><tr><td>

Preview Record

</td><td>

Action dispatched to preview a record.Payload:

-   table: The table to which the record being previewed belongs
-   sys\_id: Sys ID of the record being previewed
-   view: Record's view setting
-   query: Additional data passed to the component

</td></tr><tr><td>

Add Notification

</td><td>

Action dispatched once the field declarative action execution has completed to show notification messages. This action is only dispatched when the record contains fields with field decorators.Payload contains **items**:

-   type: Type of message to be displayed. This determines how the notification is styled. Possible types are: **error**, **info**, and **warning**\)
-   message: The notification message

</td></tr><tr><td>

Remove notifications

</td><td>

Dispatched to remove a notification message.Payload contains **items** array of notification objects. Messages are identified by their IDs.

</td></tr><tr><td>

Clear notifications

</td><td>

Dispatched to clear all notification messages.

</td></tr><tr><td>

Item Selected

</td><td>

Dispatched when an item is selected. This is a primary navigation action that opens some content.Payload:

-   table: If the content to render is a record, the table of the record
-   sys\_id: If the content to render is a record, the sys ID of the record
-   parent\_table: The table of the parent record
-   parent\_sys\_id: The sys ID of the parent record
-   renderer\_type: Default is record. For typed renderers \(non-record\) it can be a custom string
-   params: Properties passed to the component rendering the content
-   path: Hierarchy support for breadcrumbs navigation. Objects in the list have the same shape as rest of the payload

</td></tr><tr><td>

Execute UI Actions

</td><td>

Action that is dispatched to execute a specified UI Action.Payload:

-   clientScript: A client script to execute when the UI action is triggered
-   hasClientScript: Whether or not there is an associated clientScript
-   hint: Tooltip for the action button
-   label: Text to display on the action button
-   name: Name of the UI action
-   sysId: Sys ID of the action record
-   type: Type of secondary item
    -   button
    -   menuItem

</td></tr><tr><td>

Wrapped Action

</td><td>

Action that wraps an intended action in a payload.Payload:

-   wrappedAction: An intended action
-   wrappedPayload: Payload of an intended action

</td></tr></tbody>
</table>