---
title: List component setup
description: The List component displays records in configurable columns with sorting and filtering capabilities. Header controls perform various actions on the list, and an optional pagination component provides access to records that overflow the list.Use these properties to specify what records your List displays and how it displays them.To refresh a list, update the Refresh Requested property by binding the value to a client state parameter and changing that value.Select event handlers to configure the actions \(events\) provided with the List component.If you enable the drag and drop feature in a list and want those changes to persist, you must create a "transform" data broker that the Rows Reordered event can call.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/list-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 19
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# List component setup

The List component displays records in configurable columns with sorting and filtering capabilities. Header controls perform various actions on the list, and an optional pagination component provides access to records that overflow the list.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your List that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "list-config-content-tree.png"\] Alt text: component with label displayed in the content tree

2.  To configure the List component, select it using one of these methods:

    -   Click anywhere within the component.
    -   Select the component from the content tree using the label you created for your List component.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## List component properties

Use these properties to specify what records your List displays and how it displays them.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_kmr_ndz_zmb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Menu selection

</td><td>

menuSelection

</td><td>

Target table for the selected list, when the List Menu component is on the page.

</td></tr><tr><td>

Table

</td><td>

table

</td><td>

Source table for the list data. This is a required field. This table can connect to the selected property of the list source in the list menu.

</td></tr><tr><td>

Title

</td><td>

listTitle

</td><td>

Displays the title of the list. Can be connected to the selected property of the list title in the list menu.

</td></tr><tr><td>

List ID

</td><td>

selectedListId

</td><td>

Unique identifier of the data populating the List. The List ID is only used when the list is connected to a list menu to retain modifications to the list, such as column resizing or renaming.

</td></tr><tr><td>

Edit fixed filter

</td><td>

fixedQuery

</td><td>

Creates fixed queries to filter the list for display, using a condition builder. Users can't remove or modify these filters at runtime.

</td></tr><tr><td>

Edit filter

</td><td>

query

</td><td>

Creates a query to filter the list for display, using a condition builder. Can be connected to the selected property of the list conditions in the list menu.

</td></tr><tr><td>

View

</td><td>

view

</td><td>

Platform defined view of the columns to display. This value is overridden by the field list configured in the `columns` property.

</td></tr><tr><td>

Columns

</td><td>

columns

</td><td>

Comma-separated list of fields from the named table to display. This value takes precedence over the default columns provided by the `view` property.

</td></tr><tr><td>

Group by columns

</td><td>

groupByField

</td><td>

Group the list by a specific column.

</td></tr><tr><td>

Max columns

</td><td>

maxColumns

</td><td>

Maximum number of columns to display. A value of **0** displays all columns.

</td></tr><tr><td>

Max rows

</td><td>

limit

</td><td>

Maximum number of rows to display per page. This value input overrides the user preferences. For example, if the value is 10, the list will always display 10 records regardless of user preference. To honor user preferences, leave the field blank.

</td></tr><tr><td>

Action config

</td><td>

actionConfigId

</td><td>

The function you want the declarative action to execute. The values in this field are configured in the **sys\_ux\_action\_config** table.

</td></tr><tr><td>

Hide list actions

</td><td>

hideDeclarativeActions

</td><td>

Show or hide the declarative actions, regardless if the list meets the criteria set.Default: **false**

</td></tr><tr><td>

Highlighted values config

</td><td>

highlightedValueConfigId

</td><td>

Highlighted values configuration you want to use for the list. This is a reference field to list categories configured in the **sys\_ux\_list\_menu\_config** table.

</td></tr><tr><td>

Hide highlighted values

</td><td>

hideHighlightedValues

</td><td>

Show or hide the highlighted values, regardless if the list meets the criteria set. Default: **false**

</td></tr><tr><td>

Hide header

</td><td>

hideHeader

</td><td>

Show or hide the header.Default: **false**

</td></tr><tr><td>

Header size

</td><td>

variantHeader

</td><td>

Changes header with variant sizes. Available sizes are small \(sm\), medium \(md\), or large \(lg\). This field is only visible when the **hideHeader** property is **false**.Default: **size: 'lg'**

</td></tr><tr><td>

Heading level

</td><td>

headingLevel

</td><td>

Changes the level of a heading in the hierarchy. This value can be any positive integer. This field is only visible when the **hideHeader** property is **false** Default: **1**

</td></tr><tr><td>

Hide title

</td><td>

hideTitle

</td><td>

Show or hide the title in the list header.Default: **false**

</td></tr><tr><td>

Hide record count badge

</td><td>

hideTitleRowCount

</td><td>

Show or hide the row count in the list header.Default: **false**

</td></tr><tr><td>

Hide refresh button

</td><td>

hideRefreshButton

</td><td>

Show or hide the refresh button in the list header.Default: **false**

</td></tr><tr><td>

Hide "Last refreshed" text

</td><td>

hideLastRefreshedText

</td><td>

Show or hide the text label that displays the time of the last list refresh.Default: **false**

</td></tr><tr><td>

Hide menu button

</td><td>

hideMenuButton

</td><td>

Show or hide the menu button.Default: **false**

</td></tr><tr><td>

Hide option to save as

</td><td>

hideOptionToSaveAs

</td><td>

Disables the option in the gear menu for users to save a list in the My List tab of the list menu component.**Note:** To prevent users from creating their own custom lists, this property and the **Hide tabs** property in the list menu component must both be set to **true**. Hiding the **Save as** option for the list component alone doesn't restrict the user from creating new lists in List Menu.

 Default: **false**

</td></tr><tr><td>

Hide sharing button

</td><td>

hideListSharing

</td><td>

Hides the sharing button in the list header.Default: **true**

</td></tr><tr><td>

Hide panel button

</td><td>

hideFilterPanel

</td><td>

Show or hide filter panel and filter panel toggle button.Default: **false**

</td></tr><tr><td>

Hide panel footer

</td><td>

hidePanelFooter

</td><td>

Hides the entire footer of the filter panel.Default: **false**

</td></tr><tr><td>

Hide panel restore

</td><td>

hidePanelRestore

</td><td>

Hides the button that enables users to restore default filters.Default: **false**

</td></tr><tr><td>

Hide panel advanced

</td><td>

hidePanelAdvanced

</td><td>

Hides the button that activates the advanced filter capabilities.Default: **false**

</td></tr><tr><td>

Hide panel condition delete

</td><td>

hidePanelConditionDelete

</td><td>

Prevents the ability for users to remove filters in the list.Default: **false**

</td></tr><tr><td>

Collapse list menu icon

</td><td>

listMenuOpen

</td><td>

Controls the direction of the list menu icon when the list opens. This determines whether the list menu is expanded or collapsed initially.Default: **true**

</td></tr><tr><td>

Hide quick edit

</td><td>

hideQuickEdit

</td><td>

Show or hide the quick edit button. This property enables users to open a panel and interact with the record form and activity stream. Default: **false**

</td></tr><tr><td>

Hide select all

</td><td>

hideSelectAll

</td><td>

Disables the ability of a user to select all the records in a list.Default: **false**

</td></tr><tr><td>

Hide checkbox hover

</td><td>

hideCheckboxHover

</td><td>

Disables the check box hover functionality, which only displays a check box on hover. When this property evaluates to **true** check boxes are always displayed in the list.Default: **false**

</td></tr><tr><td>

Hide row selector

</td><td>

hideRowSelector

</td><td>

Show or hide row selector check boxes.Default: **false**

</td></tr><tr><td>

Hide unnecessary row selectors

</td><td>

hideUnnecessaryRowSelectors

</td><td>

Hides any unnecessary selectors.Default: **true**

</td></tr><tr><td>

Hide column grouping

</td><td>

hideColumnGrouping

</td><td>

Show or hide the control that permits the grouping of records by column.Default: **false**

</td></tr><tr><td>

Hide column resizing

</td><td>

columnsResized

</td><td>

Show or hide the column resizing button and sliders.Default: **false**

</td></tr><tr><td>

Hide column filtering

</td><td>

hideColumnFiltering

</td><td>

Show or hide column-level filters.Default: **false**

</td></tr><tr><td>

Hide column sorting

</td><td>

hideColumnSorting

</td><td>

Show or hide column sorting in the column headers.Default: **false**

</td></tr><tr><td>

Hide column personalization

</td><td>

hidePersonalization

</td><td>

Disables ability to add, remove, or changing the order of columns at runtime in the list.Default: **false**

</td></tr><tr><td>

Hide drag-and-drop-columns

</td><td>

hideColumnReorder

</td><td>

Allows a user to reorder a column by dragging it to a different position.Default: **false**

</td></tr><tr><td>

Hide dotwalk

</td><td>

hideDotwalk

</td><td>

Disables the dotwalk capability in list personalization. This property is effective only when the **Hide column personalization** flag is set to **false**.Default: **false**

</td></tr><tr><td>

Hide drag and drop

</td><td>

hideDragDrop

</td><td>

Disables the ability to drag and drop rows. Not recommended for use with sorting.Default: **true**

</td></tr><tr><td>

Hide cell filter

</td><td>

hideCellFilter

</td><td>

Show or hide **Show matching** and **Filter out** cell-level filters.Default: **false**

</td></tr><tr><td>

Hide inline editing

</td><td>

hideInlineEditing

</td><td>

Prevents users from editing values in a list.Default: **false**

</td></tr><tr><td>

Hide highlight content

</td><td>

hideHighlightContent

</td><td>

Prevents users from highlighting text. Most often used in conjunction with search results.Default: **false**

</td></tr><tr><td>

Highlight content

</td><td>

highlightContent

</td><td>

Specify the text that should be highlighted in the list and the color to use. You can define the patterns to highlight using JS regular expressions.

</td></tr><tr><td>

Hide links

</td><td>

hideLinks

</td><td>

Removes all the links in the list. Reference field links and links are rendered in plain text. This setting overrides the setting in the **Hide reference links** property.Default: **false**

</td></tr><tr><td>

Override word wrap user preference

</td><td>

overrideWordWrapUserPref

</td><td>

Overrides word wrap configured in user preferences and always observes the setting in this property.Default: **false**

</td></tr><tr><td>

Word wrap

</td><td>

wordWrap

</td><td>

Determines if the text wraps in all columns of the list, regardless of user preference.Default: **false**

</td></tr><tr><td>

Max characters

</td><td>

maxCharLimit

</td><td>

Determines the maximum characters allowed in a grid row cell. Text exceeding this limit truncates.Default: **4000**

</td></tr><tr><td>

Hide reference links

</td><td>

isRefList

</td><td>

Prevents links in reference fields from being selectable in the list but doesn't affect the links in the first column. If the **Hide links** property is set to true, reference field links are rendered in plain text, regardless of the setting in this property.Default: **false**

</td></tr><tr><td>

Hide empty state image

</td><td>

hideEmptyStateImage

</td><td>

Show or hide the empty state image for the list.Default: **false**

</td></tr><tr><td>

Hide pagination

</td><td>

hidePagination

</td><td>

Show or hide the pagination sub-component for the list.Default: **false**

</td></tr><tr><td>

Hide pages

</td><td>

hidePages

</td><td>

Show or hide the pagination component's pages.Default: **false**

</td></tr><tr><td>

Hide range

</td><td>

hideRange

</td><td>

Show or hide the pagination component's range.Default: **false**

</td></tr><tr><td>

Hide row count

</td><td>

hideRowCount

</td><td>

Show or hide the pagination component's row count.Default: **false**

</td></tr><tr><td>

Hide previous page

</td><td>

hidePreviousPage

</td><td>

Hides the pagination control that displays the previous page.Default: **false**

</td></tr><tr><td>

Hide First page

</td><td>

hideFirstPage

</td><td>

Show or hide the pagination component's first page arrow.Default: **false**

</td></tr><tr><td>

Hide last page

</td><td>

hideLastPage

</td><td>

Show or hide the pagination component's last page arrow.Default: **false**

</td></tr><tr><td>

Hide next page

</td><td>

hideNextPage

</td><td>

Hides the pagination control that displays the next page.Default: **false**

</td></tr><tr><td>

Hide rows per page selector

</td><td>

hideLimitSelector

</td><td>

Show or hide the pagination component's rows per page selector.Default: **false**

</td></tr><tr><td>

Tiny ID

</td><td>

tiny

</td><td>

A generated sys\_ID that represents a shared list and its applied conditions. Tiny IDs are used to hold URL parameters that are too long for a browser.

</td></tr><tr><td>

Error

</td><td>

error

</td><td>

Content to display when an error occurs.

</td></tr><tr><td>

Selected records

</td><td>

selectedRecords

</td><td>

Specify which rows can be selected with a simple array sys\_ids of the records to select - mark checked.

</td></tr><tr><td>

Refresh requested

</td><td>

refreshRequested

</td><td>

Unique value that forces a refresh whenever it changes.For example, you can bind this to a client state parameter and use script to set that parameter to 'Date.now\(\)' whenever you want a refresh.

</td></tr></tbody>
</table>## Refresh list on button click

To refresh a list, update the Refresh Requested property by binding the value to a client state parameter and changing that value.

### Before you begin

Role required: admin or ui\_builder\_admin

### Procedure

1.  Create a Client State parameter, such as **refreshRequested**.

2.  Add an event mapping, such as "on button click", and choose an **Update Client State parameter**.

3.  Switch to "Script" mode and use the following script.

    ```
    function evaluateEvent({api, event}) {
       return {
          propName: "refreshRequested",
          value: Date.now()
       };
    }
    ```

4.  When the user clicks a button, the value of **refreshRequested** changes, thus notifying the component to refresh the list.


## List component events

Select event handlers to configure the actions \(events\) provided with the List component.

The Events tab shows the events used by the List component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the list actions to the data you want to display to your users. Expand the event in the list and add one or more event handlers. For information about event handlers, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_alw_qnt_1nb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inline Editing Update Records Requested

</td><td>

The user edits a field in the list. The payload contains the names of the columns of the edited fields and their updated values, the sys IDs of the edited records, and the current table.

</td></tr><tr><td>

Inline Editing Validate Update Records Completed

</td><td>

Inline edited values have been validated and updated. The payload contains the sys IDs of the updated rows and the error, info, and trivial messages that resulted from the change.

</td></tr><tr><td>

Row Clicked

</td><td>

The user selects the first link in a row. Payload:

-   **row**: Row object containing the ID and display value
-   **table**: Name of the table to which the row belongs
-   **listTable**: Name of the table being viewed when selecting a row.
-   **nativeEvent**: The event object
-   **sys\_id**: The Sys ID of the selected record

</td></tr><tr><td>

New Button Clicked

</td><td>

User clicks the **New** declarative action in UIB. The payload contains the current and parent table for the list.

</td></tr><tr><td>

Selected Record Count Updated

</td><td>

The user selects a row. Payload:

-   **selectionCount**: Total number of records selected
-   **allRecordsSelected**: Indicates whether all the records in a table have been selected
-   **selectedRecords**: If **allRecordsSelected** is false, contains all the records that have been selected on a page
-   **exceptedRecords**: If **allRecordsSelected** is true, contains the records that have been deselected
-   **query**: Encoded query string that filters results of the current table
-   **table**: Name of the current table

</td></tr><tr><td>

Page Updated

</td><td>

The page changes. Payload:

-   **page**: Page to which the user wants to navigate
-   **prevPage**: Page from which the user is navigating
-   **table**: Name of the current table

</td></tr><tr><td>

Limit Updated

</td><td>

The limit of the number of records the user want to view on a page changes. Payload:

-   **limit**: Number of records a user would like to view on a page
-   **prevLimit**: Previous number of records a user viewed on a page
-   **table**: Name of the current table

</td></tr><tr><td>

Query Updated

</td><td>

A query string changes.Payload:

-   **query**: New encoded query string to apply to the table
-   **prevQuery**:
-   **table**:

</td></tr><tr><td>

Scroll Updated

</td><td>

The user scrolls the list. The event triggers once per second. Payload:

-   **timestamp**: Current timestamp of the initiated scroll of the table
-   **table**: Name of the current table

</td></tr><tr><td>

Data Fetch Requested

</td><td>

Data is requested by a record list. The event contains the Unix timestamp and these parameters to fetch new list data:Payload contains **timestamp**: Current timestamp of the data fetch requested for the table

</td></tr><tr><td>

Data Fetch Succeeded

</td><td>

A data request succeeds. The event contains the Unix timestamp and the list model.Payload:

-   **listTitle**: Title to display at the top of the list
-   **query**: Encoded query string that filters results of the current table
-   **table**: Name of the current table
-   **timestamp**: Current timestamp of the data fetch request success for the table

</td></tr><tr><td>

Data Fetch Failed

</td><td>

Action fired when a data request fails. Payload contains **error**: Error object containing the reason the data fetch failed

</td></tr><tr><td>

Menu Item Selected

</td><td>

The user selects an item from a list menu. Payload contains **name**: Name of the item that the user selected from the cell dropdown menu

</td></tr><tr><td>

Form-edit Preview Record Clicked

</td><td>

Action that fires when clicking the info icon of a field on the quick-edit form. Payload:

-   **table**: Name of the table to which the selected field belonged
-   **sys\_id**: Sys ID of the record field selected

</td></tr><tr><td>

List Edit Columns Requested

</td><td>

The user selects the **Edit columns** action from the list actions toolbar. Payload:

-   **timestamp**: Timestamp when the edit column was requested
-   **currentListData**: Object of current list metadata for the edit columns list action:
    -   title
    -   table
    -   columns
    -   conditions
    -   selectedListId
-   **update**: Object of list data that will be updated for the edit columns list action

</td></tr><tr><td>

List Delete Requested

</td><td>

The user selects the **Delete** action from the list actions toolbar. Payload contains **timestamp**: Timestamp of when the list delete was requested

</td></tr><tr><td>

List Rename Requested

</td><td>

The user selects the **Rename** action from the list actions toolbar. Payload:

-   **timestamp**: Timestamp of when the list rename was requested
-   **currentListData**: Object of current list metadata for the delete list action:
    -   title
    -   table
    -   columns
    -   conditions
    -   selectedListId
-   **update**: Object of list data that will be updated for the rename list action. The property included is **title**.

</td></tr><tr><td>

List Columns Reset Requested

</td><td>

The user clicks **Column reset** from the actions toolbar. Payload contains **columnWidths**: Empty array indicating the column width request to reset

</td></tr><tr><td>

List Save As Requested

</td><td>

The user selects the **Save** as action from the list actions toolbar.Payload:

-   **timestamp**: Timestamp when the list save was requested
-   **currentListData**: Object of current list metadata for the save as list action:
    -   title
    -   table
    -   columns
    -   conditions
    -   selectedListId
-   **update**: Object of list data to update for the save as list action:
    -   title
    -   table
    -   columns
    -   conditions

</td></tr><tr><td>

List Save Requested

</td><td>

The user selects the **Save** action from the list actions toolbar. Payload:

-   **timestamp**: Timestamp of when save was requested
-   **currentListData**: Object of current list metadata for the save list action:
    -   title
    -   table
    -   columns
    -   conditions
    -   selectedListId
-   **update**

</td></tr><tr><td>

Wrapped Action

</td><td>

A `WRAPPED_CLICKED` declarative action is emitted that wraps an action in a JSON payload.Payload:

-   **wrappedAction**: Intended action
-   **wrappedPayload**: Payload of an intended action

</td></tr><tr><td>

List Menu Toggled

</td><td>

The user clicks the list menu toggle button. Payload contains **listMenuOpen**: Boolean indicating if the list menu is open

</td></tr><tr><td>

Refresh Requested

</td><td>

The user clicks the button to refresh the list. Payload:

-   **timestamp**: Timestamp of when the refresh was requested
-   **fromButton**: Indicates that the refresh was triggered by a button interaction

</td></tr><tr><td>

List Sharing \(Tiny ID\) Updated

</td><td>

Triggered when a new tiny ID is generated. Used for sharing a list and its applied conditions.Payload cocntains **tiny**: Tiny ID, which is a generated ID used for sharing lists

</td></tr><tr><td>

Add Notification

</td><td>

Action that fires after server script declarative action executes. Payload contains **notifications**: List of notifications to display

-   **type**: Type of message to display. This determines how the notification is styled \(error\|info\|warning\)
-   **message**: Notification message

</td></tr><tr><td>

Rows Reordered

</td><td>

Allows rows reordered by the drag and drop feature to persist. The event payload contains arrays with these sys\_ids:Payload contains **data**

-   **rowsBeforeUpdate**: Rows in current page before reordering occurred
-   **rowsAfterUpdate**: Rows in current page after reordering occurred
-   **movedRows**: Rows that were reordered

 **Important:** This event requires configuration of a special event broker. See the procedure in the next section for details.

</td></tr><tr><td>

Content Items Selected

</td><td>

A highlighted value or action configuration ID is changed to dispatch admin configuration links.

</td></tr></tbody>
</table>## Data broker for persisting reordered lists

If you enable the drag and drop feature in a list and want those changes to persist, you must create a "transform" data broker that the Rows Reordered event can call.

### Before you begin

Role required: admin or ui\_builder\_admin

### Procedure

1.  In the instance, navigate to **Now Experience Framework** &gt; **Data Management** &gt; **Transforms** and select **New**.

2.  Create a data broker server script with a unique name, such as **Persist Order,** with these values:

    -   **Mutates server data**

        Select this check box to ensure that the **Execute** option is available for this data transform.

    -   **Properties**

        ```
        [
            {
                "name": "sourceTable",
                "label": "Source table",
                "fieldType": "String",
                "readOnly": false,
                "mandatory": true,
                "description": "Source table of the list being displayed"
            },
            {
                "name": "eventPayload",
                "label": "Event payload",
                "fieldType": "Object",
                "readOnly": false,
                "mandatory": true,
                "description": "List of rows in current page, before and after update and the list of moved rows"
            }
        ]
        
        ```

    -   **Script**

        ```
        function transform(input) {
            /**
             * tableName = Name of source table of the list
             * orderColumnName = Name of the column that is used for ordering
             * */
            var orderPersistence = new OrderPersistenceAPI("tableName", "orderColumnName");
            return orderPersistence.persistOrder(input);
        }
        ```

3.  Submit the new record.

    Your next task is to create a script include the data broker can call that contains additional logic for re-ordering the rows in a list.

4.  Navigate to **System Definition** &gt; **Script Includes** and select **New**.

5.  Create a record with these field definitions:

    -   **Name**

        OrderPersistenceAPI

    -   **Description**

        This API consists of methods that are used to update the records in a given table, based on the "ordering" column.

    -   **Script**

        ```
        var OrderPersistenceAPI = Class.create();
        OrderPersistenceAPI.prototype = {
            initialize: function(table, column) {
               
            },
            updateOrder: function(movedRows, firstMovedIndex, lastMovedIndex){
                /*This utitlity method would have to be written using the GlideRecord APIs.*/
            },
            persistOrder: function(input) {
                var movedRows = !gs.nil(input.eventPayload.movedRows) ? input.eventPayload.movedRows : [];
                var rowsAfterUpdate = !gs.nil(input.eventPayload.rowsAfterUpdate) ? input.eventPayload.rowsAfterUpdate : [];
                if (movedRows.length >= 0 && rowsAfterUpdate.length >= 0) {
                    // Calculate the new destination index based on the first moved row and last moved row
                    var firstMovedIndex = rowsAfterUpdate.indexOf(movedRows[0]);
                    var lastMovedIndex = rowsAfterUpdate.indexOf(movedRows[movedRows.length - 1]);
                    /**
                     * Make a call to a utility method that will take care of updating
                     * the records based on the column that is used for "ordering".
                     */
                    var result = this.updateOrder(movedRows,firstMovedIndex,lastMovedIndex);
                    return result;
                }
                return false;
            },
            type: 'OrderPersistenceAPI'
        };
        
        ```

6.  Submit the new record.

    The next task is to attach the transform data broker you created to the Rows Reordered event in UI Builder.

7.  In UI Builder select the data resources icon in the frame.

    \[Omitted image "list-open-data-resources.png"\] Alt text: Shows the location of the data resources icon to select in the UI Builder frame

8.  In the data resource instances pane, select **+ Add**.

    \[Omitted image "list-add-data-resource.png"\] Alt text: Shows the action button for adding a data resource

    The **Search data resources** window appears.

9.  In the Applications pane, select **Global** and then expand the list under **Transform** in the Data resources pane.

    \[Omitted image "list-select-data-resource.png"\] Alt text: Shows the list of available transform data brokers

10. Select the transform data broker that you created and select **Add**.

    In our example, we used **Persist Order**.The new transform appears in the list of local data resources instances.

    \[Omitted image "list-data-resource-added.png"\] Alt text: The new transform data broker displayed in the list of local data resource instances

11. Close the data resource window and select the List component in the content tree.

    \[Omitted image "list-client-script-icon.png"\] Alt text: Selecting the list component in the content tree to configure the event

12. Select the **Events** tab in the configuration panel.

13. Expand the **Rows Reordered** event and select **Add a new event handler**.

    \[Omitted image "list-add-event-handler.png"\] Alt text:

    The list of event handlers appears.

14. Search for your transform data broker in the list and select **Execute**.

    \[Omitted image "list-select-new-event-handler.png"\] Alt text: Shows the new data broker that appears in the list of available event handlers

15. Select **Add**.

    The event handler appears under the Rows Reordered event in the Events tab.

    \[Omitted image "list-new-handler.png"\] Alt text: Displays new event handler that is attached to the Rows Reordered event


