---
title: Standard list page template setup
description: The Standard list page template is built with a record list bundle and a list menu component, both of which have preset configuration values. This page template can display any record list and is intended for use in large displays as a full screen experience.Properties in the Standard list page template have preset configuration values. You can accept these values or override them manually. The List Controller used in this page template provides configurable properties.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller and no manual configuration is required. If the component has events that are not included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/standard-list-page-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 15
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Standard list page template setup

The Standard list page template is built with a record list bundle and a list menu component, both of which have preset configuration values. This page template can display any record list and is intended for use in large displays as a full screen experience.

## Before you begin

This page template contains preset configuration values. Presets automatically configure properties and event handlers for a page template, making it ready to work when you create your page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the page template. Controllers provide the configuration data and event binding the components in the page template need to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have selected the page template and are ready to configure any properties and events not included in the preset. For instructions on accessing and using features in UI Builder, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest page template functionality. Go to the store to make sure you have the latest version of the template.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for the Standard list page template and for the components used in the page.

    Descriptive labels makes finding individual components easier in a page template. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select a component to configure using one of these methods:

    -   Click anywhere within the component.
    -   Select the Action bar label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

3.  Either select **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Standard list page template properties

Properties in the Standard list page template have preset configuration values. You can accept these values or override them manually. The List Controller used in this page template provides configurable properties.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

To view the default preset configuration values in this page template, see the instructions in [View properties and events in the Controller API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

### List menu presets

The List menu component uses the **List menu** preset. This preset displays tabs of selectable lists inside the List menu component and requires the **List Controller**.

### Record list bundle presets

The Record list bundle has the following presets:

-   **Record list header**

    This preset displays heading information and actions for a record list. This preset requires the **List Controller**.

-   **Connected list**

    This preset provides a list that displays data from a ServiceNow table. This preset requires the **List Controller**.

-   **List pagination**

    Allows user to paginate within a list on the page. This preset requires the **List Controller**.


### Manual configuration

To configure preset properties manually, select the lock icon to put the field into an editable state, and then enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

### List Controller properties

To configure the List Controller properties, open the data inspector and select **List Controller** in the Data resources panel. Configuring these properties doesn't affect the upgrade of this page template.

\[Omitted image "list-controller-properties.png"\] Alt text: Shows the configurable list controller properties displayed in the data inspector for the standard list page template

<table id="table_jl4_cf1_xzb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

Source table for the list data. This is a required field. This table can connect to the selected property of the list source in the list menu.

</td></tr><tr><td>

List title\[listTitle\]

</td><td>

Displays the title of the list. Can be connected to the selected property of the list title in the list menu.

</td></tr><tr><td>

Edit fixed filter\[fixedQuery\]

</td><td>

Creates fixed queries to filter the list for display, using a condition builder. Users can't remove or modify these filters at runtime.

</td></tr><tr><td>

Edit filter\[query\]

</td><td>

Creates a query to filter the list for display, using a condition builder. Can be connected to the selected property of the list conditions in the list menu.

</td></tr><tr><td>

Group by\[groupByField\]

</td><td>

Group the list by a specific column.

</td></tr><tr><td>

View\[view\]

</td><td>

Platform defined view of the columns to display. This value is overridden by the field list configured in the `columns` property.

</td></tr><tr><td>

Columns\[columns\]

</td><td>

Comma-separated list of fields from the named table to display. This value takes precedence over the default columns provided by the `view` property.

</td></tr><tr><td>

Number of displayed columns\[columnLimit\]

</td><td>

Adjusts the number of columns to display. If the selected view contains too many columns, configure the number you want to show. This property also applies to columns selected manually by the user.

</td></tr><tr><td>

Number of displayed rows\[rowLimit\]

</td><td>

Maximum number of rows to display. When the pagination control component is present, this property applies on a per-page basis.

</td></tr><tr><td>

Current page\[currentPage\]

</td><td>

Current page index. Page 0 corresponds to the first page of data.

</td></tr><tr><td>

Enable column sorting

</td><td>

When set to **true**, allows users to sort columns by selecting the column header.Default: **true**

</td></tr><tr><td>

Column filtering popover display

</td><td>

Determines which actions users can take on a column in the popover opened from the column header action menu. You can select to disable the popover, which hides the action menu. The selections are as follows: -   Allow only filtering
-   Allow only grouping
-   Allow both \(default\)
-   Disallow column filtering popover entirely

</td></tr><tr><td>

Enable cell filtering

</td><td>

Allows users to filter cell values by **Show Matching** or **Filter Out**. When this property is set to **false**, the cell action menu is hidden.Default: **true**

</td></tr><tr><td>

Enable declarative actions

</td><td>

Displays declarative action buttons in the header action bar.**true**

</td></tr><tr><td>

List actions configuration\[actionConfigId\]

</td><td>

Action configuration you want to use to populate the declarative actions that appear in the list.

</td></tr><tr><td>

Select all records cross the list

</td><td>

Selects all records in the list when the list loads.

</td></tr><tr><td>

Selected records

</td><td>

Sys IDs of all the records to display selected when the list loads.

</td></tr><tr><td>

Excepted records

</td><td>

If all records are selected on load, define a list of records to exclude from the selection.

</td></tr><tr><td>

Enable quick edit

</td><td>

Controls display of the row action icon that triggers the quick edit panel, in which users can edit the record in that row.Default: **true**

</td></tr><tr><td>

Only enable selection when required by actions

</td><td>

Hides checkboxes if there aren't any appropriate actions in the action bar for the rows selected.Default: **true**

</td></tr><tr><td>

Enable reference links\[isRefList\]

</td><td>

Enables selectable reference links in the list. If this property is set to **false**, reference links are rendered in plain text and can't be selected.Default: **true**

</td></tr><tr><td>

Enable live list

</td><td>

Subscribes the list to live updates. Users are notified of updates but must refresh the list to see them. Enabling this feature can slow list performance.Default: **false**

</td></tr><tr><td>

Record count limit\[recordCountLimit\]

</td><td>

Sets a limit to the number of records that are counted. This setting helps performance when displaying lists with a very high number of records. The record count stops at the number configured in this property and appends a + sign to the count to indicate that additional records are included.

</td></tr><tr><td>

Fetch highlighted values

</td><td>

Fetches a highlighted value configuration and renders highlighted values in the list. If this property is enabled, you can also select a predefined highlighted value configuration.Default: **false**

</td></tr><tr><td>

Highlighted values

</td><td>

Highlighted value configuration to use in the list.

</td></tr><tr><td>

Enable dot walking when editing columns\[enableDotWalk\]

</td><td>

Enables users to dotwalk through nested columns when column editing is enabled.Default: **true**

</td></tr><tr><td>

Transform script\[transformScriptSysId\]

</td><td>

Script to run that edits how the data is displayed. You can write a custom script to take actions such as toggling feature flags, editing columns or row ordering, and adding custom data. Your custom script runs after the default transform script runs.

</td></tr><tr><td>

List menu configuration ID

</td><td>

Sys ID of the List menu content to render. This value references a record in the **sys\_ux\_list\_menu\_config** table.

</td></tr><tr><td>

Selected list ID

</td><td>

Sys ID of a list record in the **sys\_ux\_list** or **sys\_us\_my\_list** table. Use this ID when the list is configured with a List menu.

</td></tr><tr><td>

Related list parent table

</td><td>

Name of the parent table associated with this related list.

</td></tr><tr><td>

Parent record

</td><td>

Record in which the related list appears.

</td></tr><tr><td>

Related list name

</td><td>

Name of the related list

</td></tr><tr><td>

Tiny ID\[tinyId\]

</td><td>

A generated sys\_ID that represents a shared list and its applied conditions. Tiny IDs are used to hold URL parameters that are too long for a browser.

</td></tr><tr><td>

Column preference key

</td><td>

Key to use for sourcing and saving a user preference that specifies which columns to show and their order. Use this configuration if the component can't correctly determine the page ID used to save column preferences. The key must contain lowercase letters and numbers only and must be between 24 and 32 characters.

</td></tr></tbody>
</table>## Standard list page template events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller and no manual configuration is required. If the component has events that are not included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Standard list page template. Events with presets are marked with the **Preset** badge. To show events that do not have preset configurations, select **+ Add event mapping**. If the component has only one event and that event does not have a preset, the event is displayed and is ready for configuration.

### Event handlers

Event handlers work with data resources to link the Standard list page template actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Resizable panes events

These are the events for the Resizable panes component that contains the List menu and the Record list bundle.

-   **__Preset events__**

    The **List menu resizable pane** preset provides data handlers for these events:

    -   Pane sizes changed \[NOW\_RESIZABLE\_PANES\#PANE\_SIZES\#CHANGED\]: The user changes the size of the pane. The payload contains the updated **dividerPosition** value.
    -   Divider button clicked \[NOW\_RESIZBLE\_PANES\#DIVIDER\_BUTTON\#CLICKED\]: The user selects the divider button.
-   **__Non-preset events__**

    Pane displayed changed \[NOW\_RESIZABLE\_PANES\#PANE\_SIZES\#CHANGED\]

    You can add an event handler to this event.


### List Menu events

All the events for the List Menu in the Record List bundle are preset events.

-   **List menu item clicked \[SN\_NOW\_LIST\_MENU\#ITEM\_CLICKED\]**

    A user clicks on a list in the menu content tree.

    Payload:

    -   description: item
    -   fieldType: json
    -   label: Item
    -   name: item
    -   typeMetadata: object
-   **List menu action clicked \[SN\_NOW\_LIST\_MENU\#ACTION\_CLICKED\]**

    A user attempts to perform actions such as Save, Save a copy, Rename, or Delete on a list in the menu.

-   **List menu tab clicked \[SN\_NOW\_LIST\_MENU\#TAB\_CLICKED\]**

    A user clicks a tab on the list menu.

    Payload:

    -   description: selectedTabId
    -   fieldType: string
    -   label: Seleced Tab Id
    -   name: selectedTabId
    -   typeMetadata: string
-   **List menu item expanded \[SN\_NOW\_LIST\_MENU\#EXPANDED\_ITEMS\_SET\]**

    A user expands one or more items on the list menu.

    Payload:

    -   description: expandedItems
    -   fieldType: json
    -   label: Expanded Items
    -   name: expandedItems
    -   typeMetadata: array
-   **List menu items reordered \[SN\_NOW\_LIST\_MENU\#ITEMS\_SET\]**

    A user drags and drops an item to reorder the list they created.

    Payload:

    -   description: menuItems
    -   fieldType: json
    -   label: Menu Items
    -   name: menuItems
    -   typeMetadata: array
-   **List menu header action clicked \[SN\_NOW\_LIST\_MENU\#HEADER\_ACTION\_CLICKED\]**

    A user clicks on a header action in the list menu.

    Payload:

    -   description: Name of the header action clicked
    -   fieldType: string
    -   label: Action
    -   name: action
    -   typeMetadata: string

### Record List header events

All the events for the Record List header in the Record List bundle are preset events.

-   **Search submitted \[NOW\_RECORD\_LIST\_HEADER\#SEARCH\_REQUESTED\]**

    The user submits a search term in the search input field with a payload of

    Payload: @payload.searchText.

-   **Edit filters button clicked \[NOW\_RECORD\_LIST\_HEADER\#CONDITION\_BUILDER\_BUTTON\_CLICKED\]**

    The user clicks the filter button to open the modal to edit a filter.

    Payload:

    -   route: edit-filters
    -   size: lg
    -   ariaLabel: Edit Filters
    -   bare: true
-   **Refresh button clicked \[NOW\_RECORD\_LIST\_HEADER\#REFRESH\_BUTTON\_CLICKED\]**

    The user clicks the button to refresh the list.

    Payload:

    -   hideLoader: @payload.hideLoader
    -   fromButton: true
-   **Edit columns button clicked \[NOW\_RECORD\_LIST\_HEADER\#EDIT\_COLUMNS\_BUTTON\_CLICKED\]**

    The user clicks the edit columns button to open the modal to edit a column. This action dispatches these additional preset events:

    -   Open edit columnhs modal \[LIST\_CTRL\#OPEN\_EDIT\_COLUMNS\_MODAL\]
    -   Check list personalized \[LIST\_CTRL\#CHECK\_LIST\_PERSONALIZED\]
-   **Declarative Action Client Script Button Clicked \[NOW\_RECORD\_LIST\_HEADER\#DECLARATIVE\_ACTION\_CLIENT\_SCRIPT\_BUTTON\_CLICKED\]**

    The user clicks the declarative action button to execute the client script defined for the action. This action dispatches the LIST\_CTRL\#DECLARATIVE\_ACTION\_CLIENT\_SCRIPT\_EXECUTION\_REQUESTED event

    Payload: **data**: @payload.data

-   **Delcarative action server script succeeded**

    A declarative action server-side script executes successfully. This action dispatches the LIST\_CTRL\#HANDLE\_DA\_SCRIPT\_SUCCESS event.

    Payload:

    -   action: @payload.action
    -   model: @payload.model
-   **Delcarative action server script failed**

    A declarative action server-side script failed. This action dispatches the LIST\_CTRL\#HANDLE\_DA\_SCRIPT\_FAILED event.

    Payload:

    -   action: @payload.action
    -   model: @payload.model

### Record list events

All the events for the Record List in the Record List bundle are preset events.

-   **Row focused \[SN\_RECORD\_LIST\_DATA\_BROKER\#LIVE\_LIST\_ROW\_FOCUSED\]**

    A user clicks any body row or cell in the list.

-   **Header cell text clicked \[NOW\_LIST\#HEADER\_CELL\_TEXT\_CLICKED\]**

    A user clicks a list header cell.

-   **Context action clicked \[NOW\_LIST\#CONTEXT\_ACTION\_CLICKED\]**

    A user clicks a list context action either through the row actions icon buttons, the row actions context menu, the column header actions popover, the group actions, or the cell actions popover.

-   **Column header action button clicked \[NOW\_LIST\#COLUMN\_HEADER\_ACTION\_BUTTON\_CLICKED\]**

    A user clicks a column header action button.

-   **Row checkbox clicked \[NOW\_LIST\#ROW\_SELECT\_TOGGLED\]**

    A user toggles a row checkbox.

-   **Cell link clicked \[NOW\_LIST\#CELL\_LINK\_CLICKED\]**

    A user clicks an actionable link in a \(non-disabled\) link type cell.

-   **Cell person clicked \[NOW\_LIST\#CELL\_PERSON\_CLICKED\]**

    A user clicks the content in a \(non-disabled\) person type cell.

-   **Custom cell/popover/overlay action dispatched \[NOW\_LIST\#CUSTOM\_COMPONENT\_ACTION\_DISPATCHED\]**

    A user dispatches any action from the provided list of custom cell, popover, or overlay actions.

-   **Group expanded/collapsed \[NOW\_LIST\#GROUP\_TOGGLED\]**

    A user clicks the group expand/collapse button for an individual group.

-   **All groups expanded/collapsed \[NOW\_LIST\#ALL\_GROUPS\_TOGGLED\]**

    A user clicks the expand/collapse button for all groups in the header row.

-   **Message action clicked \[NOW\_LIST\#ACTIONABLE\_MESSAGE\_ACTION\_CLICKED\]**

    A user clicks an action within an actionable message.

-   **Column reordered \[NOW\_LIST\#COLUMNS\_REORDERED\]**

    A user drags a column to a new relative location.

    Payload:

    -   fieldType: json
    -   label: Data
    -   name: data
    -   typeMetadata: object
        -   oldColumns: array
        -   newColumns: array
        -   reorderedColumns: array
-   **Column widths updated \[NOW\_LIST\#COLUMN\_WIDTHS\_UPDATED\]**

    A user drags a column to adjust its width using the resize slider.

    Payload:

    -   fieldType: json
    -   label: Data
    -   name: data
    -   typeMetadata: object
        -   columnKey: string
        -   oldWidth: string
        -   updatedWidth: string
        -   columnWidths: object
-   **Cell editing requested \[NOW\_LIST\#CELL\_EDIT\_REQUESTED\]**

    A user double-clicks on a cell to open a cell editing popover

-   **Cell edit submitted \[NOW\_LIST\#CELL\_EDIT\_SUBMITTED\]**

    A user clicks the Apply button in a cell editing popover.


### Pagination control events

All the events for the pagination control in the Record List bundle are preset events.

-   **Pagination control selected page set \[NOW\_PAGINATION\_CONTROL\#SELECTED\_PAGE\_SET\]**

    The user selects a page or selects the pagination control.

    Payload:

    -   name: value
    -   label: Value
    -   fieldType: number
    -   typeMetadata: number
-   **Pagination control selected size set \[NOW\_PAGINATION\_CONTROL\#SELECTED\_PAGE\_SIZE\_SET\]**

    The user selects a page size from the dropdown list.

    Payload:

    -   name: value
    -   label: Value
    -   fieldType: number
    -   typeMetadata: integer

### List Controller events

The following List Controller events aren't included in the preset. You can configure event handlers on these events without affecting the upgrade of this page template.

-   **Add list notifications requested**

    Add notifications to the page level notification list.

-   **Clear all list notifications requested**

    The user clears all notifications.

-   **Reference link clicked**

    The user selects a reference link \(navigation item\).

-   **Create new record**

    The user selects the button to create a new record \(navigation item\).

-   **Selected list id from list menu has been updated**

    The ID of a list in the list menu changes.


