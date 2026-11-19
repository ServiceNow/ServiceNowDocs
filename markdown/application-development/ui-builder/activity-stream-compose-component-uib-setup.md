---
title: Activity Stream Compose component setup
description: Activity Stream Compose enables you to add private or customer-visible comments to a record.Properties in the Activity Stream Compose component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/activity-stream-compose-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Activity Stream Compose component setup

Activity Stream Compose enables you to add private or customer-visible comments to a record.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Activity Stream Compose that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "activity-stream-compose-content-tree.png"\] Alt text: Shows the activity stream compose component in the content tree.

2.  Select the Activity Stream Compose component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Activity Stream Compose label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "activity-stream-compose-presets.png"\] Alt text: Shows the list of presets for the activity stream compose component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "activity-stream-compose-preset-config.png"\] Alt text: Shows the configuration panel for connecting a preset to the required controller for the activity stream compose component

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md)


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Activity Stream Compose component properties

Properties in the Activity Stream Compose component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record compose__**

    This preset tracks messages such as emails, work notes and customer facing comments related to a record. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Table
    -   Sys ID
    -   Fields definition
    -   New record
    -   Bare

### Properties

<table id="table_a5y_jjf_xtb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title\[title\]

</td><td>

Title of the activity stream compose.

</td></tr><tr><td>

Table\[table\]

</td><td>

Name of the table to which the new journal entry is posted.

</td></tr><tr><td>

Sys ID\[sysId\]

</td><td>

Unique identifier for the record.

</td></tr><tr><td>

Fields definition\[fields\]

</td><td>

Object containing available journal fields.Format example: `{ field_name : { name:string, label:string, sys_readonly:bool, readonly:bool, visible:bool, type:'journal_input', maxLength:number }, ... }`

</td></tr><tr><td>

New record\[isNewRecord\]

</td><td>

Shows whether or not the current record is newly created.Default: **false**

</td></tr><tr><td>

Use tabs\[useTabs\]

</td><td>

Displays fields in tabs instead of a dropdown, if space permits. This control doesn't apply when the component is displayed in stacked mode.Default: **true**

</td></tr><tr><td>

Enable rich text editor\[isRichTextEnabled\]

</td><td>

Displays the rich text editor when selected.

</td></tr><tr><td>

Show rich text editor toggle\[isRichTextAvailable\]

</td><td>

Option to make the rich text editor available to users. Default: **false**

</td></tr><tr><td>

Allow journal settings overrides\[allowJournalFieldSettingsOverrides\]

</td><td>

When this property is set to **true**, the `journalFieldSettings` property overrides the journal field data. When this property is set to **false**, `journalFieldSettings` are only defaults and can't override journal field data.Default: **true**

</td></tr><tr><td>

Journal settings\[journalFieldSettings\]

</td><td>

Defines any optional display settings for the journal field. Depending on the value of the `allowJournalFieldSettingsOverrides` property, the `journalFieldSettings` property provides overrides \(true\) or default values \(false\) for the fields defined in the `fields` property.This should be an object with the field names as properties and `journalFieldSettings` as values. Field names should match the ones passed in the `fields` property.

</td></tr><tr><td>

Show post button for mandatory journal fields\[canPostMandatoryFields\]

</td><td>

When set to **true**, shows the Post button even if the journal field is mandatory. When used in a form it is recommended to set this property to **false**.Default: **false**

</td></tr><tr><td>

Show compose title\[showTitle\]

</td><td>

Displays the compose title in the activity stream.Default: **false**

</td></tr><tr><td>

Show field labels\[showFieldLabels\]

</td><td>

Determines if the labels should be shown in compose.Default: **true**

</td></tr><tr><td>

Is side by side view available\[isSideBySideViewAvailable\]

</td><td>

Displays an option to switch to a side-by-side view.Default: **false**

</td></tr><tr><td>

Is side by side view enabled\[isSideBySideViewEnabled\]

</td><td>

Show or hide the option to select the side-by-side view.Default: **false**

</td></tr><tr><td>

Fit to parent\[fitToParent\]

</td><td>

Expands compose to full height of parent container. This requires a defined height on the parent.

</td></tr><tr><td>

Bare\[bare\]

</td><td>

Removes the padding and background from the component.Default: **true**

</td></tr><tr><td>

Email Action\[emailAction\]

</td><td>

Enables a new Email tab beside Worknotes and Additional comments, and defines the properties to compose an email.

</td></tr><tr><td>

Activity compose title\[composeTitle\]

</td><td>

Text to show for the title of the activity compose component.Default: **Compose**

</td></tr><tr><td>

Post button variant\[postButtonVariant\]

</td><td>

Style variant for the post button.Choices: **primary**, **secondary**, **tertiary**

</td></tr><tr><td>

Post button size\[postButtonSize\]

</td><td>

Determines the size of the Post button.Default: **sm**

Choices: **sm** \(small\), **md** \(medium\), **lg** \(large\)

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Activity stream compose component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Activity Stream Compose component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**.

\[Omitted image "activity-stream-compose-events.png"\] Alt text: Shows the events list for the activity stream compose component. None of the events are included in the preset

### Event handlers

Event handlers work with data resources to link the Activity Stream Compose component actions to the data you want to display to your users. Select the event in the list to add one or more event handlers. For information about event handlers, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "activity-stream-compose-event-config.png"\] Alt text: Shows the activity stream compose events ready to be configured with event handlers

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record compose__**

    This preset doesn't include any events


### Event descriptions

<table id="table_czb_nhy_wtb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Initial state requested

</td><td>

Activity Stream Compose component requests that the state variables be initialized.Payload: `requestedState`

</td></tr><tr><td>

Display changed

</td><td>

Activity Stream Compose component renders empty or with content. This event identifies the current status.Payload: `isEmpty`

</td></tr><tr><td>

Email action completed

</td><td>

The user has completed or cancelled the email action.Payload:

-   `reason`
-   `newEmailAction`

</td></tr><tr><td>

Set setting requested

</td><td>

User has changed a setting in the Activity Stream Compose settings dropdown.Payload:

-   `name`
-   `value`

</td></tr><tr><td>

Updated field value

</td><td>

User has updated a field value.Payload:

-   `fieldName`
-   `value`
-   `displayValue`

</td></tr></tbody>
</table>