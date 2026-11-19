---
title: Form Record Presence component setup
description: The Form Record Presence component adds avatars when other users are viewing the record at the same time.Properties in the Form Record Presence component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/form-record-presence-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Form Record Presence component setup

The Form Record Presence component adds avatars when other users are viewing the record at the same time.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Form Record Presence that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "form-record-presence-content-tree.png"\] Alt text: Shows the form record presence component in the content tree in UI Builder

2.  Select the Form Record Presence component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Form Record Presence label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "form-record-presence-presets.png"\] Alt text: Shows the list of presets for the form record presence component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "form-record-presence-preset-config.png"\] Alt text: Shows the configuration panel for connecting the selected preset to the controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Form Record Presence component properties

Properties in the Form Record Presence component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record presence__**

    This preset displays avatars for other users who are viewing the record concurrently. If 2 other users are viewing the record, their avatars are both displayed. If more than 2 are present, the first 2 user avatars are displayed with a third overflow trigger “avatar”. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Table
    -   Sys ID
    -   Is Openframe Config Valid

### Properties

<table id="table_ski_dma_rk4"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table \[table\]

</td><td>

Table name for this record.

</td></tr><tr><td>

Sys ID\[sysId\]

</td><td>

Sys ID for this record.

</td></tr><tr><td>

Is Openframe Config Valid\[isOpenframeConfigValid\]

</td><td>

Indicates whether or not Openframe is configured. When the Openframe plugin is active, a phone icon appears on the popover list beside each avatar. A user viewing the record can select this icon to initiate an outbound call to another user's business phone number.Default: **false**

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Form Record Presence component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required.

The Events tab shows the events used by the Form Record Presence component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**. If the component has only one event, and that event doesn't have a preset, the event is displayed, ready for configuration.

\[Omitted image "form-record-presence-events.png"\] Alt text: Shows the list of events for the selected preset

### Event handlers

Event handlers work with data resources to link the Form Record Presence actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record presence__**

    This preset provides data handlers for these events:

    -   Open Phone
    -   Add Notification
    -   User Status

### Event descriptions

<table id="table_xyw_9uq_lor"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open Phone

</td><td>

Event dispatched to open a phone. Opens the dial up pad or makes a call if the phone number is provided.Payload:

-   `type`: The type.
-   `table`: The table to which the record being previewed belongs.
-   `tableName`: The table label to which the record being previewed belongs.
-   `sysId`: The sys Id of the record being previewed.
-   `phoneNumber`: The phone number to dial.
-   `displayValue`: Text value used to represent the record, such as a title, if applicable.

</td></tr><tr><td>

Add Notification

</td><td>

Adding notifications to the page.Payload includes **items**:

-   `type`: Type of message to be displayed. This determines how the notification is styled. The possible types are **error**, **info**, and **warning**.
-   `message`: The notification message.

</td></tr><tr><td>

User Status

</td><td>

Shows whether another present user is just viewing or typing.Payload:

`userId`: \(optional\). If not provided, the behavior should fall back to checking the **userSession** information. This info should already be populated by the preset in **activtyStream** and **recordPresence**.

</td></tr></tbody>
</table>