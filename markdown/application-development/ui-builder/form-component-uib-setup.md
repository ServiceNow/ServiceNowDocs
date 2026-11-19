---
title: Form component setup
description: The Form component groups fields into sections based on the form layout configuration of the given view and provides user input fields.Properties in the Form component have preset configuration values. You can accept these values or override them manually.The Events tab shows the events used by the Form component. If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/form-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 16
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Form component setup

The Form component groups fields into sections based on the form layout configuration of the given view and provides user input fields.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Form that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "form-content-tree.png"\] Alt text: Shows the content tree in UI Builder with the unique name for the form component

2.  Select the Form component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Action bar label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "form-presets.png"\] Alt text: Shows the list of presets for the form component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "form-presets-config.png"\] Alt text: Shows the preset configuration panel for connecting the preset to the required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Form component properties

Properties in the Form component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record form__**

    This preset provides a complete record form with user input fields and related records. This preset requires the **Form** controller.

    Properties included in this preset are:

    -   Sections
    -   Fields
    -   Table
    -   Related Lists
    -   Sys ID
    -   View
    -   Configuration
    -   Changed Fields in serialized JSON string
    -   Encoded Record
    -   User Session information
    -   Form Messages

### Legacy form and multiple forms

You can have 2 or more forms on a page. However, if you want to add a form to a legacy page with an existing form, you must do the following:

1.  Because the legacy form controller doesn’t have a preset, you must add the **Form controller preset** to it:

    1.  Select the data resource **Form Controller**.
    2.  In the **Edit Form Controller** dialog, select **Form controller preset** from the list of presets.
    \[Omitted image "form-form-controller.png"\] Alt text: Edit form controller dialog with preset drop down expanded and Form controller preset selected

2.  When you add multiple forms to a page, the form controller for the first form you add is mapped to the page app shell. This mapping enables the form to communicate with the app shell elements, for example to display form information in a browser tab, and in notifications. When you already have a legacy form on a page and you add another form, you must specify which form you want to map to the page app shell:

    **Note:** The **Is mapped to App Shell** property is set on the form controller not the form component.

    1.  Select the form controller for the form.
    2.  In the **Edit Form Controller** dialog, scroll to the bottom of the list of properties in the **Config** tab.
    3.  Select the **Is mapped to App Shell** property.

        \[Omitted image "form-controller-maptoappshell.png"\] Alt text: Edit Form Controller dialog scrolled to the bottom and showing cursor on the Is mapped to App Shell toggle


### Form controller property

<table id="id_awh_vhc_hbc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Is mapped to App Shell\[isMappedToAppShell\]

</td><td>

To support multiple forms on a page, must be set to **true** for each unique Form controller instance.

 Default: **true** for the first form placed on a page; **false** for a legacy form and for all other forms.

</td></tr></tbody>
</table>### Properties

<table id="table_qr1_bkp_rnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

Table name for the record header.

</td></tr><tr><td>

Sys ID\[sysId\]

</td><td>

Sys ID for the record header.

</td></tr><tr><td>

Workspace ID\[workspaceConfigId\]

</td><td>

Sys ID for workspace configuration this record is in.

</td></tr><tr><td>

Query\[query\]

</td><td>

An encoded query string to filter the fields displayed.

</td></tr></tbody>
</table><table id="table_ht2_fqr_ydc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View\[view\]

</td><td>

View to use to display the record.

</td></tr><tr><td>

Forced view name\[forcedViewName\]

</td><td>

View to use to override the view designated using the **view** property.

</td></tr><tr><td>

Enable previous record button\[enablePreviousRecordButton\]

</td><td>

Shows or hides the previous button. When **true**, the previous button is visible and the previous record is available.Default: **false**

</td></tr><tr><td>

Enable next record button\[enableNextRecordButton\]

</td><td>

Shows or hides the next button. When **true**, the next button is visible and the next record is available.Default: **false**

</td></tr><tr><td>

Show nav record buttons\[showNavRecordButtons\]

</td><td>

Shows or hides the up and down navigation record buttons.Default: **false**

</td></tr><tr><td>

Sections\[sections\]

</td><td>

Sections used to group fields in the form. Sections can be manually set to an array of static values or linked to a data resource.

</td></tr><tr><td>

Fields\[fields\]

</td><td>

Array of field objects. Each object contains the information that is passed to the rendered field component.

</td></tr><tr><td>

Related Lists\[relatedLists\]

</td><td>

A list of records related to the current record.

</td></tr></tbody>
</table><table id="table_g4j_gqr_ydc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide form context menu\[isContextMenuHidden\]

</td><td>

Shows or hides the form context menu.Default: **false**

</td></tr><tr><td>

Hide "Jump to section navigation"\[isSectionMenuHidden\]

</td><td>

Shows or hides the context menu section "Jump to section navigation".Default: **false**

</td></tr><tr><td>

Hide "More form options"\[isFormOptionsHidden\]

</td><td>

Shows or hides the context menu section "More form options".Default: **false**

</td></tr><tr><td>

Hide "View"\[isViewSectionHidden\]

</td><td>

Hides view that is used to render the form when set to **true**. Default: **false**

</td></tr></tbody>
</table><table id="table_jhd_hqr_ydc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide all section titles\[isSectionTitleHidden\]

</td><td>

Shows or hides all the section titles. If **disableCollapse** is set to **true**, the entire section header is hidden.Default: **false**

</td></tr><tr><td>

Hide first section title\[isFirstSectionTitleHidden\]

</td><td>

Shows or hides the first section title. If `disableCollapse` is set to **true**, the entire section header is hidden.Default: **false**

</td></tr><tr><td>

Disable section collapsing\[disableCollapse\]

</td><td>

Lets user collapse sections.Default: **false**

</td></tr><tr><td>

Section Heading Level\[sectionHeadingLevel\]

</td><td>

Use to define the section heading level from 1 to 6 for the section headers.Default: **2**

</td></tr></tbody>
</table><table id="table_dy4_gkd_cfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable unsaved field indicator\[enableUnsavedFieldIndicator\]

</td><td>

Shows or hides a field-level indicator when a field is in an unsaved state. If set to **false**, an indicator in the form of a black dot appears next to each field with updates that aren't saved.Default: **true**

</td></tr><tr><td>

Enable unsaved field indicator background\[enableBgColorForUnsavedFieldIndicator\]

</td><td>

Enable unsaved field indicator must be set to **true** to use this property.Shows or hides a background color indicator that displays a background color to fields that have unsaved changes.

Default: **false**

</td></tr><tr><td>

Hide field context menu\[isFieldContextMenuHidden\]

</td><td>

Whether admins can access the field context menu. If set to **false**, the field context menu is hidden. When **true**, admins can't access the field context menu.Default: **true**

</td></tr><tr><td>

Label wrapping limit \(px\)\[labelWrappingLimit\]

</td><td>

Wraps the label instead of truncating it if the container width is less than the limit specified.Default: truncates the label

</td></tr></tbody>
</table><table id="table_w4s_hqr_ydc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Landmark\[landmark\]

</td><td>

Includes the component as a part of the keyboard shortcut landmark focus, allowing keyboard-only users to quickly navigate through a page and between primary components.Default: **false**

</td></tr></tbody>
</table><table id="table_cs3_3qr_ydc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration\[config\]

</td><td>

Stores configuration details such as show/hide activity stream.Default: showActivityStream: **false**

</td></tr><tr><td>

Changed fields in serialized JSON string\[serializedChanges\]

</td><td>

Shows the serialized dirty fields string.

</td></tr><tr><td>

Encoded record\[encodedRecord\]

</td><td>

Contains properties for rendering the activity stream component.

</td></tr><tr><td>

User session Information\[userSession\]

</td><td>

Contains the user session information.Default: **@context.session.user**

</td></tr><tr><td>

Form messages\[formMessages\]

</td><td>

Messages that appear on the form.Array properties:

-   **type**: Type of message to be displayed. The message type determines how the notification is styled \(error\|info\|warning\).
-   **message**: The message to display.

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Form component events

The Events tab shows the events used by the Form component. If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**. If the component has only one event, and that event doesn't have a preset, the event is displayed, ready for configuration.

\[Omitted image "form-preset-events.png"\] Alt text: Shows a partial list of the events with presets for the form component

### Event handlers

Event handlers work with data resources to link the Form actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record form__**

    This preset provides data handlers for these events:

<table id="table_plk_mwc_35b"><tbody><tr><td>

-   Preview Record
-   Item Selected
-   Add Notification
-   Remove Notifications
-   Clear Notifications
-   Remove form message
-   Screen Status Changed
-   Execute UI Action
-   Refresh Requested
-   Set Value
-   Add Option
-   Remove Option
-   Set Read Only


</td><td>

-   Set Visible
-   Show Related List
-   Hide Related List
-   Show Related Lists
-   Hide Related Lists
-   Clear Messages
-   Hide Field Message
-   Clear value
-   Hide All Field Messages
-   Set Label
-   Set Field Placeholder
-   Set Section Display
-   Set User Value


</td><td>

-   Add Info Message
-   Add Warning Message
-   Add Error Message
-   Show Field Message
-   Set Field mandatory
-   Reload Form
-   Save a form
-   Submit Form
-   Clear Choice Options
-   Add Form Message
-   Clear Form Message
-   Clear All Form Messages
-   Toggle Annotations


</td></tr></tbody>
</table>
### Event descriptions

<table id="table_ujd_2n5_rnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Preview Record

</td><td>

Action dispatched to preview a record.Payload:

-   `table`: The table to which the record being previewed belongs.
-   `sys_id`: The sys ID of the record being previewed.
-   `query`: Additional data passed to the component.
-   `params`: Properties passed to the component.
-   `multiInstField`: Field that is used in conjunction with route and params to support multiple instance of a content.

</td></tr><tr><td>

Item Selected

</td><td>

Primary navigation action that opens some content.Payload:

-   `table`: If the content to render is a record, the table of the record.
-   `sys_id`: If the content to render is a record, the sys Id of the record
-   `parent_table`: The table of the parent record.
-   `parent_sys_id`: The sys ID of the parent record.
-   `render_type`: Default is **record**. For typed renderers \(non-record\) it can be a custom string.
-   `params`: Properties passed to the component rendering the content.
-   `path`: Hierarchy support for breadcrumbs navigation. Objects in the list have the same shape as rest of the payload.

</td></tr><tr><td>

Add Notification

</td><td>

Informs the user of any errors while interacting with the component such as deleting or uploading an attachment. Action dispatched once the field declarative action execution has completed. This action is only dispatched when the record contains fields with field decorators.Payload contains `items`

-   `type`: Type of message to be displayed. The message type determines how the notification is styled \(error\|info\|warning\).
-   `message`: The notification message.

</td></tr><tr><td>

Remove notifications

</td><td>

Notifications are removed. Payload contains `items`: Array of notification objects to remove, identified by their IDs.

</td></tr><tr><td>

Clear notifications

</td><td>

Action to clear all notifications.

</td></tr><tr><td>

Remove form message

</td><td>

A single form message is removed, by index.Payload contains `index`: Index of the message to remove

</td></tr><tr><td>

Wrapped Action

</td><td>

Action that wraps an intended action in a payload.Payload:

-   `wrappedAction`: An intended action
-   `wrappedPayload`: Payload of an intended action

</td></tr><tr><td>

Screen Status Changed

</td><td>

Action dispatched to indicate that form is dirty.

</td></tr><tr><td>

Execute UI Action

</td><td>

Action that is dispatched to execute the specified UI Action.

</td></tr><tr><td>

Refresh Requested

</td><td>

Action dispatched on successful field declarative action executions for server script action. This action is only dispatched when the record contains fields with field decorators.

</td></tr><tr><td>

Set Value

</td><td>

User sets a value for a given field.Payload:

-   `fieldName`: Name of the field for which the value is being set
-   `value`: Value to which the field is being set
-   `displayValue`: Display value of the field being set

</td></tr><tr><td>

Add Option

</td><td>

Adds an option to a choice type.Payload:

-   `fieldName`: Name of the field to which the options is added
-   `choiceValue`: Value of the option
-   `choiceLabel`: Label of the option
-   `choiceIndex`: Index of the inserted option

</td></tr><tr><td>

Remove Option

</td><td>

An option is removed from a choice list.Payload:

-   `fieldName`: Name of a field
-   `choiceValue`: The choice value

</td></tr><tr><td>

Set Read Only

</td><td>

Sets a field to read-only when true.Payload:

-   `fieldName`: Name of the field to set to read-only
-   `readonly`: If true, set the given field read only

</td></tr><tr><td>

Set Visible

</td><td>

Sets the field visible if true. Makes the field hidden if false.Payload:

-   `fieldName`: Name of the field being set
-   `visibility`: If true, set the given field to visible

</td></tr><tr><td>

Show Related List

</td><td>

Shows the specified related list on the form.Payload: `listTableName`: Specifies the name of the related list to show

</td></tr><tr><td>

Hide Related List

</td><td>

Hides a specified related list on the form.Payload contains `listTableName`: Specifies the name of the related list to hide

</td></tr><tr><td>

Show Related Lists

</td><td>

Shows all related lists.

</td></tr><tr><td>

Hide Related Lists

</td><td>

Hides all related lists.

</td></tr><tr><td>

Clear Messages

</td><td>

Clear all form messages.

</td></tr><tr><td>

Hide Field Message

</td><td>

Hides the first \(oldest\) message by a field.Payload:

-   `fieldName`: Name of a field to hide a message
-   `clearAll`: Whether or not to clear all messages.

Default: **false**


</td></tr><tr><td>

Clear Value

</td><td>

The user clears the value of a given field.Payload contains `fieldName`: Name of the field whose value was cleared

</td></tr><tr><td>

Hide All Field Messages

</td><td>

Hide all field messages of a specific type.Payload contains `type`: The type of message to be hidden. The choices are:

-   `info`
-   `warning`
-   `error`

</td></tr><tr><td>

Set Label

</td><td>

Set the label of a specific field.Payload:

-   `fieldName`: Name of the field whose label is being set
-   `label`: Label to display for the field

</td></tr><tr><td>

Set Field Placeholder

</td><td>

Set placeholder text for a specific field.Payload:

-   `fieldName`: Name of the field for which placeholder text is defined
-   `value`: Value to set as the placeholder

</td></tr><tr><td>

Set Section Display

</td><td>

Show or hide a given form section.Payload:

-   `sectionName`: Name of the form section to show or hide
-   `display`: If true, shows a given form section.

</td></tr><tr><td>

Set User Value

</td><td>

Set a value for a given field via user input.Payload:

-   `fieldName`: Name of the field whose value is being set
-   `value`: Value to set in the field
-   `displayValue`: Display value to set

</td></tr><tr><td>

Add Info Message

</td><td>

Add a form message of type `info`.Payload contains `message`: The info message to display

</td></tr><tr><td>

Add Warning Message

</td><td>

Add a form message of type `warning`.Payload contains `message`: The warning message to display

</td></tr><tr><td>

Add Error Message

</td><td>

Add a form message of type `error`.Payload contains `message`: The error message to display

</td></tr><tr><td>

Show Field Message

</td><td>

Show a field message of a specify type.Payload:

-   `fieldName`: Name of the field displaying the message.
-   `type`: Message type. The choices are `info`, `warning`, and `error`.
-   `message`: Message to display.

</td></tr><tr><td>

Hide All Field Messages

</td><td>

Hide field messages of a specific type.Payload contains `type`: The choices are `info`, `warning`, and `error`.

</td></tr><tr><td>

Set Field mandatory

</td><td>

Makes the field required if set to **true**. Makes the field optional if set to **false**.Payload:

-   `fieldName`: Name of the field to set to mandatory
-   `mandatory`: If set to **true**, set the named field to mandatory

</td></tr><tr><td>

Reload Form

</td><td>

Reload the form with the same table and sysId.

</td></tr><tr><td>

Save a form

</td><td>

Save the current record.

</td></tr><tr><td>

Submit Form

</td><td>

Trigger form submission using the given UI action name.Payload contains `submitActionName`: Name of the UI action

</td></tr><tr><td>

Clear Choice Options

</td><td>

Clears all options for a choice list.Payload contains `fieldName`: Name of the field from which the choice list is cleared

</td></tr><tr><td>

Add Form Message

</td><td>

Add a form message of a given type.Payload:

-   `message`: Message to display
-   `type`: The choices are `info`, `warning`, and `error`.

</td></tr><tr><td>

Clear Form Messages

</td><td>

Clear all form messages of a given type.Payload contains `type`: The choices are `info`, `warning`, and `error`.

</td></tr><tr><td>

Clear All Form Messages

</td><td>

Clear all form messages.

</td></tr><tr><td>

Toggle Annotations

</td><td>

Hide all currently shown annotations or show all currently hidden annotations.

</td></tr><tr><td>

Form message button clicked

</td><td>

Event dispatched when a button in a form message is clicked.

</td></tr><tr><td>

Set transaction scope

</td><td>

Edit the form within the provided application scope.

</td></tr><tr><td>

Clear transaction scope

</td><td>

Clear the form's transaction scope.

</td></tr></tbody>
</table>