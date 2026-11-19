---
title: List - Related component setup
description: The List - Related component is used in a record to see and access tables that have relationships to the record you’re viewing.Configure the filtering and sorting capabilities of your List - Related component with these properties.Select event handlers to configure the actions \(events\) provided with the List - Related component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/list-related-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# List - Related component setup

The List - Related component is used in a record to see and access tables that have relationships to the record you’re viewing.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your List - Related that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "list-related-content-tree.png"\] Alt text: List- Related content tree.

2.  Select the List - Related component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the List - Related label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## List - Related component properties

Configure the filtering and sorting capabilities of your List - Related component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_lcc_qsb_kvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

Source table for the list data. Optionally, you can add a fixed filter to display specific records from the selected table. This is a required field.

</td></tr><tr><td>

Parent table\[parentTable\]

</td><td>

The parent table associated with the related list.

</td></tr><tr><td>

Parent record sysID\[parentRecordSysId\]

</td><td>

The Sys ID of the record for the related list.

</td></tr><tr><td>

Edit fixed filter\[fixedQuery\]

</td><td>

Apply fixed query filters to filter the list. Users can't edit or remove a fixed filter.

</td></tr></tbody>
</table><table id="table_gxw_ysb_kvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View\[view\]

</td><td>

Platform defined view of the columns to display. This value is overridden by the field list configured in the columns property. By default this field populates with a UIB view when one exists, or it will reference the Default view.

</td></tr><tr><td>

Columns\[columns\]

</td><td>

Comma-separated list of fields from the named table to display.

</td></tr><tr><td>

Number of displayed columns\[maxColumns\]

</td><td>

Maximum number of columns to display. A value of **0** displays all columns.

</td></tr><tr><td>

Edit filter\[query\]

</td><td>

Opens a condition builder to create a query for filtering the list. This filter can be removed by the user at runtime.

</td></tr><tr><td>

Group by\[groupByField\]

</td><td>

Group the list by a specific column.

</td></tr><tr><td>

Hide highlighted values\[hideHighlightedValues\]

</td><td>

Show or hide the highlighted values, regardless if the list meets the criteria set.Default: **false**

</td></tr><tr><td>

Highlighted values\[highlightedValueConfigId\]

</td><td>

Selects the highlighted values configuration to use for the list. This field is required if you are using highlighted values for the list.

</td></tr><tr><td>

Hide highlighted content\[hideHighlightContent\]

</td><td>

Disables the user's ability to highlight text. Use this property in conjunction with search results.Default: **false**

</td></tr><tr><td>

Highlighted content\[highlightContent\]

</td><td>

Specifies the text that should be highlighted in the list.

</td></tr><tr><td>

Hide links\[hideLinks\]

</td><td>

Removes all the links in the list. Reference fields and links will render as plain text.Default: **false**

</td></tr><tr><td>

Enable word wrap\[wordWrap\]

</td><td>

Determines if the text wraps in all columns of the list regardless of user preference.Default: **false**

</td></tr><tr><td>

Override word wrap user preference\[overrideWordWrapUserPref\]

</td><td>

Overrides word wrap configured in user preferences and always observes the setting in this property.Default: **false**

</td></tr><tr><td>

Maximum characters\[maxCharLimit\]

</td><td>

Integer that determines the maximum characters allowed in a grid row cell. Text exceeding this limit truncates.Default: **4000**

</td></tr></tbody>
</table><table id="table_txm_ywb_kvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide option to personalize columns\[hidePersonalization\]

</td><td>

Disables ability to add, remove, or changing the order of columns at runtime in the list.Default: **false**

</td></tr><tr><td>

Disable dotwalk\[hideDotwalk\]

</td><td>

Disables the dotwalk capability in list personalization. This property is effective only when the **Hide column personalization** flag is set to **false**.Default: **false**

</td></tr><tr><td>

Hide option to drag-and-drop columns\[hideColumnReorder\]

</td><td>

Allows a user to reorder a column by dragging it to a different position.Default: **false**

</td></tr><tr><td>

Hide option to group records\[hideColumnGrouping\]

</td><td>

Show or hide the column grouping option and associated declarative actions.Default: **true**

</td></tr><tr><td>

Hide option to select all records\[hideSelectAll\]

</td><td>

Disables the user's ability to select all the records in a list.Default: **fault**

</td></tr><tr><td>

Show checkboxes only on hover\[hideCheckboxHover\]

</td><td>

Prevents check boxes from appearing only on hover. When set to true, this property always displays check boxes in the list.Default: **false**

</td></tr><tr><td>

Hide selection if action is unavailable\[hideUnnecessaryRowSelectors

</td><td>

Hides any unnecessary selectors.Default: **true**

</td></tr><tr><td>

Hide column resizing\[hideColumnResizing\]

</td><td>

Show or hide the column resizing button and header sliders. Default: **false**

</td></tr></tbody>
</table><table id="table_btk_tzb_kvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title\[listTitle\]

</td><td>

Title to display at the top of the list.

</td></tr><tr><td>

Hide list actions\[hideListActions\]

</td><td>

Hides all list actions in the header toolbar.

</td></tr><tr><td>

List actions configuration\[actionConfig\]

</td><td>

Function you want the declarative action to execute. Only Default and Related lists are supported.

</td></tr><tr><td>

Hide filter panel footer\[hidePanelFooter\]

</td><td>

Hides the entire footer in the filter panel.Default: **fault**

</td></tr><tr><td>

Hide filter panel restore\[hidePanelRestore\]

</td><td>

Hides the button that enables users to restore default filters.Default: **fault**

</td></tr><tr><td>

Hide filter panel advanced\[hidePanelAdvanced\]

</td><td>

Hides the button in the filter panel that launches an advanced search.

</td></tr><tr><td>

Hide option to delete filter conditions\[hidePanelConditionDelete\]

</td><td>

Blocks users from removing filters on the list.Default: **false**

</td></tr></tbody>
</table><table id="table_arn_mvn_lvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide previous page\[hidePreviousPage\]

</td><td>

Hides the pagination control that displays the previous page.Default: **false**

</td></tr><tr><td>

Hide next page\[hideNextPage\]

</td><td>

Hides the pagination control that displays the next page.Default: **false**

</td></tr><tr><td>

Maximum rows\[limit\]

</td><td>

Maximum number of rows to display per page. This value input will override the user preferences. For example, if the value is 10, the list always displays 10 records regardless of user preference. To honor user preferences, leave this field blank.

</td></tr></tbody>
</table><table id="table_b5b_51c_kvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide inline editing\[hideInlineEditing\]

</td><td>

Prevents users from editing the list inline.Default: **true**

</td></tr><tr><td>

Refresh requested\[refreshRequested\]

</td><td>

Object containing a timestamp that can be passed down to trigger a refresh.

</td></tr><tr><td>

Related list name\[relatedListName\]

</td><td>

Title of the related list.

</td></tr></tbody>
</table>## List - Related component events

Select event handlers to configure the actions \(events\) provided with the List - Related component.

The Events tab shows the events used by the List - Related component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the List - Related actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_x3l_njl_qnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scroll Updated

</td><td>

The user scrolls the list. The event triggers once per second. Payload:

-   **timestamp**: Current timestamp when the scroll of the table was initiated
-   **table**: Name of the current table

</td></tr><tr><td>

Preview record button clicked

</td><td>

The user selects the first link in a row. Payload:

-   **row**: Row object containing the ID and display value
-   **table**: Name of the table to which the row belongs
-   **listTable**: Name of the table being viewed when selecting a row.
-   **nativeEvent**: The event object
-   **sys\_id**: The Sys ID of the selected record

</td></tr><tr><td>

Reference link clicked

</td><td>

The user selects the reference link in a cell.Payload:

-   **row**: Row object containing the ID and display value
-   **table**: Name of the table to which the row belongs
-   **listTable**: Name of the table being viewed when selecting a row.
-   **nativeEvent**: The event object
-   **sys\_id**: The Sys ID of the selected record

</td></tr><tr><td>

Related list reference cell link clicked

</td><td>

The user selects a reference link in a cell of a related list.Payload:

-   **row**: Row object containing the ID and display value
-   **table**: Name of the table to which the row belongs
-   **listTable**: Name of the table being viewed when selecting a row.
-   **nativeEvent**: The event object
-   **sys\_id**: The Sys ID of the selected record

</td></tr><tr><td>

Query Updated

</td><td>

A query string is updated. Payload:

-   **query**: New encoded query string to apply to the table
-   **prevQuery**: Previous encoded query string that was applied to the table
-   **table**: Name of the current table

</td></tr><tr><td>

Cell context menu item selected

</td><td>

A user selects an item from the list menu. Payload contains **name**: Name value of the item selected from the cell dropdown menu

</td></tr><tr><td>

Selected records count updated

</td><td>

The user selects a row. Payload:

-   **count**: Total number of records selected
-   **allRecordsSelected**: Indicates whether all the records in a table have been selected
-   **query**: Encoded query string that filters results of the current table
-   **table**: Name of the current table

</td></tr><tr><td>

Data fetch requested

</td><td>

Data is requested by a record list. Displays the current **timestamp** and all required parameters to fetch new list data.Payload includes:

-   **timestamp**: Current timestamp of the data fetch request
-   **columns**
-   **limit**
-   **page**
-   **query**
-   **table**
-   **view**

</td></tr><tr><td>

Data fetch succeeded

</td><td>

A data fetch succeeded. Payload:

-   **timestamp**: Timestamp of the successful data fetch request for the table
-   **listTitle**Title to display at top of list
-   **parentRecordSysId**: Parent record Sys ID
-   **parentTable**: Name of the parent table
-   **query**: Encoded query string that filters results of the current table
-   **relatedListName**: Related list name
-   **table**: Name of the current table
-   **model**:

</td></tr><tr><td>

Data fetch failed

</td><td>

A user data request has failed.Payload: Error object containing the reason the data fetch failed

</td></tr><tr><td>

Refresh requested

</td><td>

The user clicks the button to refresh the list. Payload:

-   **timestamp**: Current timestamp of when the refresh was requested
-   **fromButton**: Indication of whether the refresh was triggered by a button interaction

</td></tr><tr><td>

New record button clicked

</td><td>

User clicks the **New** declarative action in UIB. The payload contains the current and parent table for the list.

</td></tr><tr><td>

Current page updated

</td><td>

The page changes. Payload:

-   **page**: Page to which a user wants to navigate
-   **prevPage**: Page from which a user is navigating
-   **table**: Name of the current table

</td></tr><tr><td>

Row limit updated

</td><td>

The limit of the number of records the user want to view on a page changes. Payload:

-   **limit**: Number of records a user would like to view on a page
-   **prevLimit**: Previous number of records a user viewed on a page
-   **table**: Name of the current table

</td></tr><tr><td>

Inline editing: update record\(s\) requested

</td><td>

The user edits a field in the list. The payload contains the names of the columns of the edited fields and their updated values, the sys IDs of the edited records, and the current table.

</td></tr><tr><td>

Inline editing: update record\(s\) completed

</td><td>

Inline edited values have been validated and updated. The payload contains the sys IDs of the updated rows and the error, info, and trivial messages that resulted from the change.

</td></tr><tr><td>

Notification\(s\) displayed

</td><td>

A notification is displayed on the list.

</td></tr><tr><td>

Action script succeeded

</td><td>

A server script declarative action executes successfully.Payload contains **notifications**: An array of objects that contain the message and type of message to display.

-   **type**: Type of notification to display, such as error, info, or warning. This determines how the notification is styled.
-   **message**: Content of the notification message

</td></tr><tr><td>

Action script failed

</td><td>

A declarative action, server-side script fails to execute.

</td></tr><tr><td>

Wrapped action dispatched

</td><td>

A `WRAPPED_CLICKED` declarative action is emitted that wraps an action in a JSON payload.Payload:

-   **wrappedAction**: An intended action
-   **wrappedPayload**: Payload of an intended action

</td></tr></tbody>
</table>