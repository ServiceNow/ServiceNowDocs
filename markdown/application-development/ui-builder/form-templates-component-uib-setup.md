---
title: Form Templates component setup
description: The Form Templates component enables you to create and update pre-existing templates to automate data entry on reoccurring records.Properties in the Form Templates component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/form-templates-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Form Templates component setup

The Form Templates component enables you to create and update pre-existing templates to automate data entry on reoccurring records.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

You can apply one preset to a single instance of a component on a page. There are two types of controllers available: the UI page controller and the Record controller. The Record controller retrieves metadata and configurations for the page definition. UI page controllers retrieve data related to page behavior, such as component preference states and cross-component behaviors.

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Form Templates that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "form-templates-content-tree.png"\] Alt text: Shows the Form Template component in the content tree.

2.  Select the Form Templates component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Form Templates label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "form-template-presets.png"\] Alt text: Shows the presets available for the form template component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "form-templates-preset-config.png"\] Alt text: Shows the configuration panel for connecting the preset to the required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Form Templates component properties

Properties in the Form Templates component have preset configuration values. You can accept these values or override them manually.

Presets are designed to suit a specific use case. However, you can override a property that has a preset value with a custom configuration, if you find it necessary for your design. For details on overriding and resetting presets, see [Override a preset for a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record form template__**

    This preset facilitates the creation and maintenance of form templates and helps automate data entry on recurring forms. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Table
    -   View
    -   Sys ID
    -   fields

### Properties

<table id="table_xzl_mwj_snb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

Table to which the templates are applied.

</td></tr><tr><td>

Refresh Requested\[refreshRequested\]

</td><td>

A timestamp value defining when to request a form refresh.

</td></tr><tr><td>

View\[view\]

</td><td>

Form view to use when creating or editing a template.

</td></tr><tr><td>

Sys ID\[sysId\]

</td><td>

Sys ID of the record to which the template is applied.

</td></tr><tr><td>

fields\[fields\]

</td><td>

Map of fields that are shown in the form.

</td></tr><tr><td>

Hide my templates\[hideMyTemplates\]

</td><td>

Shows or hides the My Templates tab.Default: **false**

</td></tr><tr><td>

Hide sort button\[hideSorting\]

</td><td>

Shows or hides the sort button.Default: **false**

</td></tr><tr><td>

Hide favorite features\[hideFavorite\]

</td><td>

Shows or hides the favorite icon in the template card and the Favorites tab.Default: **false**

</td></tr><tr><td>

Ask confirmation when same template is applied on a record\[askConfirmationOnSameTemplate\]

</td><td>

Determines if a message displays asking for confirmation when a user applies the same template again on a record.Default: **false**

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md)
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md)

## Form Templates component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Form Templates component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**. If the component has only one event, and that event doesn't have a preset, the event is displayed, ready for configuration.

\[Omitted image "form-templates-events.png"\] Alt text: Shows the events for form templates component. None are marked with preset data handlers

### Event handlers

Event handlers work with data resources to link the Form Templates actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

\[Omitted image "form-templates-event-handlers.png"\] Alt text: Shows events in form templates with data handlers configured

### Preset events

-   **__Record form template__**

    This preset doesn't have any events.


### Event descriptions

<table id="table_m21_jxj_snb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add Notifications

</td><td>

Notifications added to the page. Notifications inform the user of errors while interacting with the component. For example, deleting or uploading an attachment.Payload: **items**: List of notifications to display

-   `type`: Type of message to display. This determines how notification is styled. The available types are:
    -   `error`
    -   `info`
    -   `warning`
-   `message`: The notification message
-   `contentType`: Type of content to be passed. Accepts `html` or `string` options. For `html`, the caller is responsible for escaping all data to avoid XSS attacks. For `string`, content is automatically escaped.

</td></tr><tr><td>

Clear notifications

</td><td>

Action to clear all notifications.

</td></tr><tr><td>

Preview Record \(template\)

</td><td>

Action to preview a given template for creation or editing.Payload:

-   `table`: Table name
-   `sys_id`: Sys ID of the record
-   `view`: Record's view setting
-   `query`: Template query to add initial value for the template value field

</td></tr></tbody>
</table>