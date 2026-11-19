---
title: Lookup component setup
description: Look up a record on any table in card format.Look up a record on any table in card format.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/lookup-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Lookup component setup

Look up a record on any table in card format.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Lookup that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Lookup component using one of these methods:

    -   Click anywhere within the component.
    -   Select the Action bar label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

3.  Either select **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Lookup component properties

Look up a record on any table in card format.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record lookup__**

    This preset adds event binding for Email request, Phone request, and Open record request for the Lookup component. This preset requires the **Form** controller.

    Properties included in this preset are: View.


### Properties

<table id="table_xjc_xzj_c2c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Advanced search configuration\[advancedSearchConfig\]

</td><td>

Configure advanced search options.-   exactMatchSearchFields
-   startsWithSearchFields
-   referenceTables

</td></tr><tr><td>

Allow collapsible state\[allowCollapse\]

</td><td>

Displays a button to toggle the visibility of the linked card content fields.Default: **False**

</td></tr><tr><td>

Allow create new\[allowCreateNew\]

</td><td>

Shows and hides the Create new function.Default: **True**

</td></tr><tr><td>

Allow edit\[allowEdit\]

</td><td>

Shows and hides the Edit function.Default: **True**

</td></tr><tr><td>

Allow unlink\[allowUnlink\]

</td><td>

Shows and hides the Unlink function.Default: **True**

</td></tr><tr><td>

Collapse by default\[collapseByDefault\]

</td><td>

Sets whether to collapse all linked card content when the page first loads.Default: **False**

</td></tr><tr><td>

Enable advanced search\[enableAdvancedSearch\]

</td><td>

Shows and hides the advanced search configuration.Default: **False**

</td></tr><tr><td>

Enable verify\[enableVerify\]

</td><td>

When true, shows the verify button for the linked card.Default: **False**

</td></tr><tr><td>

Field size\[fieldSize\]

</td><td>

Text style for search/linked card fields. Select from the following options:-   Small
-   Medium

Default: **Medium**

</td></tr><tr><td>

Heading\[heading\]

</td><td>

Label for the lookup heading.

</td></tr><tr><td>

Heading style\[headingStyle\]

</td><td>

Text style for heading. Select from the following options: -   Header-primary
-   Header-secondary
-   Header-tertiary
-   Title primary
-   Title secondary
-   Title tertiary

Default: **Header-secondary**

</td></tr><tr><td>

Highlighted values config ID\[highlightedValueConfigId\]

</td><td>

Config ID for highlighted values.

</td></tr><tr><td>

Linked card content fields\[selectedFields\]

</td><td>

List of fields to display on the linked card.

</td></tr><tr><td>

Linked record\[linkedRecordSysId\]

</td><td>

Record to link.

</td></tr><tr><td>

Linked card view\[linkedView\]

</td><td>

Form view used to display fields for the linked card.

</td></tr><tr><td>

Search conditions\[encodedQuery\]

</td><td>

Lookup search conditions.

</td></tr><tr><td>

Search label\[searchLabel\]

</td><td>

Label for the search input field.

</td></tr><tr><td>

Search result fields\[searchFields\]

</td><td>

The fields to use to display field and value pairs in search results.

</td></tr><tr><td>

Search results per page \[searchResultsPerPage\]

</td><td>

Maximum number of search results to display per page.

</td></tr><tr><td>

Search result view\[searchView\]

</td><td>

Form view to use to display fields for search results.

</td></tr><tr><td>

Show empty values\[showEmptyValues\]

</td><td>

Show and hide fields with empty values in search results and linked card. When set to true, fields with empty values display the field title with the field value "No data." When set to false, fields with empty values don't display at all.Default: **False**

</td></tr><tr><td>

Show heading\[showHeading\]

</td><td>

Shows and hides the card heading.

</td></tr><tr><td>

Show link button\[showLinkButton\]

</td><td>

Displays or hides a link icon button for search result cards.Default: **True**

</td></tr><tr><td>

Show record link\[showRecordLink\]

</td><td>

Displays or hides the record header of a linked card. When true, the card header displays.Default: **True**

</td></tr><tr><td>

Table\[table\]

</td><td>

Table to look up.

</td></tr><tr><td>

Verified\[verified\]

</td><td>

Displays a verified badge on the linked card.Default: **False**

</td></tr><tr><td>

Verify button label\[verifyButtonLabel\]

</td><td>

Label for the verify button.

</td></tr><tr><td>

View\[view\]

</td><td>

UI view name to use to show fields in the form.

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Lookup component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Lookup component. Events with presets are marked with the **Preset** badge. To show events that do not have preset configurations, select **+ Add event mapping**. If the component has only one event and that event does not have a preset, the event is displayed and is ready for configuration.

### Event handlers

Event handlers work with data resources to link the Lookup actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record lookup__**

    This preset provides data handlers for these events:

    -   Record lookup email requested
    -   Record lookup phone requested
    -   Record lookup open record requested

### Event descriptions

<table id="table_hxq_ym5_ddc"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record lookup email requested

</td><td>

Request for opening an email field. Payload:-   email
-   label

</td></tr><tr><td>

Record lookup form status changed

</td><td>

Used to forward `CTRL_RECORD#SCREEN_STATUS_CHANGED`.

</td></tr><tr><td>

Record lookup link record data fetch completed

</td><td>

Dispatched when the user saves an edited lookup form. Also dispatched in the following scenarios:-   After linking a contact card or record
-   When the contact form is saved with a display value change
-   On page initial load or page refresh, when a default linked card is already assigned

Payload:

-   table
-   sysID
-   label \(returns the most current display value\)
-   status

</td></tr><tr><td>

Record lookup link requested

</td><td>

Request for linking a record. Payload:-   label
-   sysID
-   table

</td></tr><tr><td>

Record lookup open record requested

</td><td>

Request for opening a reference field. Payload:-   label
-   sysID
-   table

</td></tr><tr><td>

Record lookup phone requested

</td><td>

Request for opening a phone number field. Payload: -   label
-   phoneNumber

</td></tr><tr><td>

Record lookup unlink requested

</td><td>

Request for unlink of selected record.

</td></tr></tbody>
</table>