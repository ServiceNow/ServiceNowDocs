---
title: Record List bundle
description: Use the Record List bundle for a configurable group of components that enable you to display a list on your page.The Record List Header provides contextual information about a list.Properties in the Record List Header component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.The Presentational List component acts as the list body and displays data from any data source in column and rows that you can sort, filter, and edit.Configure the properties for Presentational List.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/record-list-bundle-component-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 24
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Record List bundle

Use the Record List bundle for a configurable group of components that enable you to display a list on your page.

The Record List bundle provides a List Controller data layer and a group of components which includes the Record List Header, Presentational List, and Pagination Control components.

You can drag the Record List bundle onto your page and receive expected functionality while simultaneously using detailed configurations for individual components. For example, if you have a use case for a list with a custom header, you can drag the Record List bundle onto the page, delete the Record Header, and build your own header.

## List Controller data resource

The List Controller data resource acts as the data layer for the Record List bundle. It fetches and formats data displayed on your list and handles the logic to integrate features by enabling presets.

## Record List Header component

The Record List Header component uses the List Controller data resource to provide a preset for contextual information about your list.

## Presentational List component

The Presentational List component acts as the list body and displays data from any data source in column and rows that you can sort, filter, and edit.

## Pagination Control component

Pagination Control component divides large sets of content into consolidated pages and enables you to navigate through pages with a navigation tool at the bottom of the page.

For information on configuring Pagination Control in UI Builder, see [Pagination Control component setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/pagination-control-component-uib-setup.md).

**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Record List Header component setup

The Record List Header provides contextual information about a list.

### Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

### Procedure

1.  Define a label for Record List Header that differentiates it from other components in the content tree.

    \[Omitted image "record-list-header-content-tree.png"\] Alt text: Record List Header in content tree

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Record List Header component using one of these methods:

    -   Click anywhere within the component.
    -   Select the label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "record-list-header-presets.png"\] Alt text: Record List Header presets

3.  Either select **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    \[Omitted image "record-list-controller.png"\] Alt text: List Controller configuration panel

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


## Record List Header component properties

Properties in the Record List Header component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record list header__**

    This preset displays heading information and actions for a record list. This preset requires the List Controller.

    Properties included in this preset are:

    -   Show inline padding
    -   Size
    -   Show title
    -   Wrap title
    -   Title
    -   Show subtitle
    -   Subtitle
    -   Show count
    -   Count
    -   Record count limit
    -   Allow manual refresh
    -   Allow field personalization
    -   Allow dot walking when personalizing fields
    -   Show option to copy URL
    -   Allow keyword search
    -   Show filter button for condition builder panel
    -   Expand condition builder panel
    -   Allow declarative actions
    -   Actions configuration for declarative actions

### Properties

<table id="table_shb_bcz_xfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show inline padding\[showInlinePadding\]

</td><td>

Show padding on the inline direction, which is left and right in a horizontal writing mode.Default: **true**

</td></tr><tr><td>

Size\[headerSize\]

</td><td>

Use the large size for full-page lists and opt for the medium or small size for those within a more confined space, like a dashboard or playbook.

</td></tr></tbody>
</table><table id="table-uib-props"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show title\[showTitle\]

</td><td>

Show title of the list in the header.Default: **true**

</td></tr><tr><td>

Wrap title\[enableTitleWrap\]

</td><td>

Allow the title to wrap into multiple lines instead of being truncated when it doesn't fit in one line.Default: **true**

</td></tr><tr><td>

Title\[title\]

</td><td>

Title of the list.

</td></tr><tr><td>

Show subtitle\[showSubtitle\]

</td><td>

Show subtitle of the list in the header.Default: **true**

</td></tr><tr><td>

Subtitle\[subtitle\]

</td><td>

Subtitle of the list, usually the time it was last refreshed.

</td></tr></tbody>
</table><table id="table_jmf_wcz_xfc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Show count\[showCount\]

</td><td>

Show badge for the number of list items.Default: **true**

</td></tr><tr><td>

Count\[count\]

</td><td>

The number to be displayed in a badge, usually representative of the number of items in a list.

</td></tr><tr><td>

Record count limit\[recordCountLimit\]

</td><td>

Limits the number of records shown in a list for better performance. For example, if a list has 1 million records, you can show the first 10,000 with a count of 10,000 or more. If you don't set a limit or use a negative number, all records will be fetched.

</td></tr></tbody>
</table><table id="table_fpt_gdz_xfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow manual refresh\[showRefreshButton\]

</td><td>

Allow users to manually refresh the list by selecting the Refresh button.Default: **true**

</td></tr><tr><td>

Allow field personalization\[showEditColumnsButton\]

</td><td>

Allow users to choose the fields and order to display with the Personalize columns option.Default: **true**

</td></tr><tr><td>

Allow dot walking when personalizing fields\[enableDotWalk\]

</td><td>

Lets users drill down into nested columns when personalizing them.Default: **true**

</td></tr><tr><td>

Show option to copy URL\[showCopyURLButton\]

</td><td>

Show option to copy the URL of the list’s current state, not just from the browser.Default: **false**

</td></tr><tr><td>

Allow keyword search\[showSearchButton\]

</td><td>

Allow users to search list data with the Search button. This only works for indexed tables.Default: **true**

</td></tr><tr><td>

Show filter button for condition builder panel\[showConditionBuilderButton\]

</td><td>

Show the filter button that allows users to expand or collapse the condition builder panel.Default: **true**

</td></tr><tr><td>

Expand condition builder panel\[showConditionBuilderPanel\]

</td><td>

Choose whether to expand or collapse the condition builder panel.Default: **false**

</td></tr></tbody>
</table><table id="table_k4r_ydz_xfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow declarative actions\[enableDeclarativeActions\]

</td><td>

Lets users take actions like editing and creating records directly from the list header.Default: **true**

</td></tr><tr><td>

Actions configuration for declarative actions\[actionConfigId\]

</td><td>

The action configuration to use to populate the declarative actions.

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Record List Header component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

\[Omitted image "record-list-header-events.png"\] Alt text: Record List Header Events tab

The Events tab shows the events used by the Record List Header component. Events with presets are marked with the **Preset** badge. To show events that do not have preset configurations, select **+ Add event mapping**. If the component has only one event and that event does not have a preset, the event is displayed and is ready for configuration.

### Event handlers

Event handlers work with data resources to link the Record List Header actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record list header__**

    This preset provides data handlers for these events:

    -   Back button clicked
    -   Cancel filter panel button clicked
    -   Copy URL button clicked
    -   Declarative action client script button clicked
    -   Declarative action redirect requested
    -   Declarative action server script failed
    -   Declarative action server script succeeded
    -   Declarative action wrapped clicked
    -   Edit columns button clicked
    -   Header alert action clicked
    -   Header toggle set
    -   List layout item set
    -   Predicate Builder update button clicked
    -   Refresh button clicked
    -   Search submitted

### Event descriptions

<table id="table_gzl_ndm_dcc"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Back button clicked\[NOW\_RECORD\_LIST\_HEADER\#BACK\_BUTTON\_CLICKED\_ACTION\]

</td><td>

A user clicks the back button to dispatch back button clicked action.

</td></tr><tr><td>

Cancel filter panel button clicked\[NOW\_RECORD\_LIST\_HEADER\#CLOSE\_FILTER\_PANEL\_ACTION\]

</td><td>

A user clicks the cancel button to close the filter panel.

</td></tr><tr><td>

Copy URL button clicked\[NOW\_RECORD\_LIST\_HEADER\#COPY\_URL\_BUTTON\_CLICKED\_ACTION\]

</td><td>

A user clicks the copy URL button.

</td></tr><tr><td>

Declarative action client script button clicked\[NOW\_RECORD\_LIST\_HEADER\#DECLARATIVE\_ACTION\_CLIENT\_SCRIPT\_EXECUTE\_ACTION\]

</td><td>

A user clicks a declarative action button to execute the client script defined in the action.

</td></tr><tr><td>

Declarative action redirect requested\[NOW\_RECORD\_LIST\_HEADER\#DECLARATIVE\_ACTION\_REDIRECT\_REQUESTED\]

</td><td>

A declarative action server script request to navigate a user to a given record after execution.Payload:

-   table: Table of the record that will be opened.
-   sys\_id: Sys ID of the record that will be opened.
-   query: Query of the record that will be opened.
-   parent\_table: If applicable, parent table of the record that will be opened.
-   parent\_sys\_id: If applicable, parent sys ID of the record that will be opened.

</td></tr><tr><td>

Declarative action server script failed\[NOW\_RECORD\_LIST\_HEADER\#DECLARATIVE\_ACTION\_SCRIPT\_FAILED\]

</td><td>

A declarative action server-side script fails.Payload:

-   action: Details of the action that invoked the server-side update.
-   model: Details of the model on which the server-side update was invoked.

</td></tr><tr><td>

Declarative action server script succeeded\[NOW\_RECORD\_LIST\_HEADER\#DECLARATIVE\_ACTION\_SCRIPT\_SUCCESS\]

</td><td>

A declarative action server-side script executes successfully.Payload:

-   action: Details of the action that invoked the server-side update.
-   model: Details of the model on which the server-side update was invoked.

</td></tr><tr><td>

Declarative action wrapped clicked\[NOW\_RECORD\_LIST\_HEADER\#DECLARATIVE\_ACTION\_WRAPPED\_CLICKED\_ACTION\]

</td><td>

A user clicks a UXF declarative action button to dispatch a client action.Payload:

wrappedAction: The key of the client action.

wrappedPayload: The payload associated with the client action.

</td></tr><tr><td>

Edit columns button clicked\[NOW\_RECORD\_LIST\_HEADER\#EDIT\_COLUMNS\_BUTTON\_CLICKED\]

</td><td>

A user clicks the edit columns button to open the edit columns modal.

</td></tr><tr><td>

Header alert action clicked\[NOW\_RECORD\_LIST\_HEADER\#HEADER\_ALERT\_CLICKED\_ACTION\]

</td><td>

A user clicks the action button in the internal alert.Payload:

action: String name of a Seismic action to dispatch.

</td></tr><tr><td>

Header toggle set\[NOW\_RECORD\_LIST\_HEADER\#HEADER\_TOGGLE\_SET\_ACTION\]

</td><td>

A user toggles the header toggle on or off.Payload:

isToggleOn: The value of the toggle.

</td></tr><tr><td>

List layout item set\[NOW\_RECORD\_LIST\_HEADER\#LIST\_LAYOUT\_ITEM\_SET\_ACTION\]

</td><td>

A user selects a list layout item.Payload:

value: The ID of the selected layout.

</td></tr><tr><td>

Predicate Builder update button clicked\[NOW\_RECORD\_LIST\_HEADER\#PREDICATE\_BUILDER\_SET\_QUERY\_ACTION\]

</td><td>

A user clicks the Predicate Builder update button to update list query.

</td></tr><tr><td>

Refresh button clicked\[NOW\_RECORD\_LIST\_HEADER\#REFRESH\_BUTTON\_CLICKED\]

</td><td>

A user clicks the refresh button.

</td></tr><tr><td>

Search submitted\[NOW\_RECORD\_LIST\_HEADER\#SEARCH\_REQUESTED\]

</td><td>

A user submits a search term in the search input field.Payload:

searchText: The submitted search text.

</td></tr></tbody>
</table>## Presentational List component setup

The Presentational List component acts as the list body and displays data from any data source in column and rows that you can sort, filter, and edit.

### Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

### Procedure

1.  Define a label for Presentational List that differentiates it from other components in the content tree.

    \[Omitted image "presentational-list-component-tree.png"\] Alt text: Presentational List in content tree

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Presentational List component using one of these methods:

    -   Click anywhere within the component.
    -   Select the Presentational List label you created for your component in the content tree.
    \[Omitted image "presentational-list-presets.png"\] Alt text: Presentational List presetsThe preset selection panel appears in the pane on the right.

3.  Either select **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    \[Omitted image "record-list-controller.png"\] Alt text: List Controller configuration panel

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


## Presentational List component properties

Configure the properties for Presentational List.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Connected list__**

    This preset sets the data, default display, end user capabilities, selection options and cell content properties. This preset requires the **list** controller.

    Properties included in this preset are:

    -   Type
    -   Layouts
    -   Show inline padding
    -   Table
    -   Edit fixed query
    -   Let users get live updates
    -   Turn on infinite scrolling
    -   View
    -   Columns
    -   Number of columns to display
    -   Number of records per page
    -   Edit default filter
    -   Group by
    -   Expand all groups
    -   Nest by
    -   Allow selection
    -   Show option to select all
    -   Only allow record selection on when required by actions
    -   Display all records as selected on initial load
    -   Records to display as selected
    -   Allow expanding and collapsing all groups at once
    -   Allow quick edit
    -   Enforce view rules in quick edit
    -   Allow form navigation in quick edit
    -   Allow column filtering
    -   Allow column sorting
    -   Allow column grouping
    -   Allow column resizing
    -   Allow column reordering
    -   Allow row reordering
    -   Allow cell filtering
    -   Allow users to edit cell content in a popover
    -   Allow clickable text
    -   Allow reference field links
    -   Fetch highlighted values
    -   Highlighted values configuration
    -   Shade alternate rows
    -   Wrap cell content
    -   Max characters per cell

### Properties

<table id="table_pgk_lpy_xfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type\[listType\]

</td><td>

List types provide default feature sets that offer varied levels of functionality. Choose a type that provides your end users with the list capabilities they need.Default: **Default**

</td></tr><tr><td>

Layouts\[layouts\]

</td><td>

Select how to display data. List layout presents data in rows and columns. Gallery layout displays data in a card-based format. If you choose multiple layouts, users will be able to switch between them.Default: **List only**

</td></tr><tr><td>

Show inline padding\[showInlinePadding\]

</td><td>

Includes padding on the leading side of the list. When false, the list is flush with the edge of the container.Default: **true**

</td></tr></tbody>
</table><table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

Select the table data to display in the list.

</td></tr><tr><td>

Edit fixed filter\[fixedQuery\]

</td><td>

Apply fixed query filters to filter the list. These cannot be modified by the user.

</td></tr><tr><td>

Let users get live updates\[enableLiveList\]

</td><td>

When enabled, the list will subscribe to live updates. The system property glide.lists.live\_list\_enabled must be added and enabled. Enabling this feature may slow the list experience.**Only by refreshing** shows an indicator on the refresh button when updates are available.

**Automatically** adds a toggle to the list header for users to turn on automatic updates. If they don't turn it on, they can still get updates by refreshing.

Default: **Never**

</td></tr><tr><td>

Turn on infinite scrolling\[enableInfiniteScroll\]

</td><td>

When enabled, lets users scroll through a list without selecting page buttons, so pagination will be hidden.Default: **false**

</td></tr></tbody>
</table><table id="table_c1t_dqd_2cc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View\[view\]

</td><td>

Predefined column selection and, as defined in the \[sys\_ui\_view\] table.

</td></tr><tr><td>

Columns\[columns\]

</td><td>

Instead of using a view, you can select fields as columns and set their order.

</td></tr><tr><td>

Number of columns to display\[maxColumns\]

</td><td>

Choose how many columns to display from the view or from the columns you selected. For example, if a view has 15 columns, you can choose to show only the first 5.

</td></tr></tbody>
</table><table id="table_rpn_fry_xfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of records per page\[rowLimit\]

</td><td>

Set the number of records to display in the list or on each page of the list if pagination is present.

</td></tr><tr><td>

Edit default filter\[query\]

</td><td>

Users can change the default filter.

</td></tr><tr><td>

Group by\[groupBy\]

</td><td>

Group records by a data field. For example, you can group a list of employees by office location.

</td></tr><tr><td>

Expand all groups\[expandAllGroups\]

</td><td>

When true, expands all groups in the table.Default: **false**

</td></tr><tr><td>

Nest by\[orderBy\]

</td><td>

Nest parent and child records by specifying fields. For example, you can have multiple products nested under each product bundle.

</td></tr></tbody>
</table><table id="table_exs_4ry_xfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow selection\[selectionEnabled\]

</td><td>

Allows users to select items in the list. This can be overridden on a per-item basis in row definitions.Default: **true**

</td></tr><tr><td>

Show option to select all\[selectAllEnabled\]

</td><td>

Lets users select all items by checking a box in the header row.Default: **true**

</td></tr><tr><td>

Only allow record selection on when required by actions\[onlyEnableSelectionWhenRequiredByActions\]

</td><td>

Many declarative actions require selection of one or more records. When enabled, this property hides the checkboxes on the list if there are no such actions in the action bar.Default: **false**

</td></tr><tr><td>

Display all records as selected on initial load\[allRowsSelected\]

</td><td>

Default: **true**

</td></tr><tr><td>

Records to display as selected\[selectedRowIds\]

</td><td>

Sys\_ids of records to display as selected.

</td></tr></tbody>
</table><table id="table_rc1_qrd_2cc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow expanding and collapsing all groups at once\[toggleAllGroupsEnabled\]

</td><td>

Shows a chevron button in the header row of a list layout or a text button above the groups in a gallery layout.

</td></tr><tr><td>

Allow quick edit\[enableQuickEdit\]

</td><td>

The quick edit feature allows you to click on a row action icon to open up a panel in which you can edit the associated record.Default: **true**

</td></tr><tr><td>

Enforce view rules in quick edit\[enforceViewRulesForQuickForm\]

</td><td>

Dynamically select a view for the form in the quick edit panel based on Workspace View Rules. If no matching rules are found, use the view selected for the list, or the default view if none is selected.Default: **true**

</td></tr><tr><td>

Allow form navigation in quick edit\[enableQuickFormNavigation\]

</td><td>

Lets users move between records using up and down buttons on the quick edit panel.Default: **true**

</td></tr><tr><td>

Allow column filtering\[columnFilteringEnabled\]

</td><td>

Allows users to filter the list with a column filter row under the header row.Default: **true**

</td></tr><tr><td>

Allow column sorting\[enableSorting\]

</td><td>

Allows users to sort the list by selecting a column header.Default: **true**

</td></tr><tr><td>

Allow column grouping\[enableGrouping\]

</td><td>

Allows users to group the list by selecting a column action from the column header or creating a grouping rule with the Group by button in the list header.Default: **true**

</td></tr><tr><td>

Allow column resizing\[columnResizingEnabled\]

</td><td>

Allows users to resize columns by dragging the bar handle in column headers.Default: **true**

</td></tr><tr><td>

Allow column reordering\[rowDragDropEnabled\]

</td><td>

Allows users to drag and drop columns with drag handles in each column header.Default: **true**

</td></tr><tr><td>

Allow row reordering\[columnDragDropEnabled\]

</td><td>

Allows users to drag and drop rows with drag handles in each row.Default: **false**

</td></tr><tr><td>

Allow cell filtering\[enableCellFiltering\]

</td><td>

Allows users to filter the list by a cell with the show matching or filter out cell action.Default: **true**

</td></tr><tr><td>

Allow users to edit cell content in a popover\[cellEditingEnabled\]

</td><td>

Allows users to edit cell content in a popover.Default: **true**

</td></tr></tbody>
</table><table id="table_h5z_prd_2cc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow clickable text\[clickableTextEnabled\]

</td><td>

Allows text to be selected including URLs, actionable links, and person links.Default: **true**

</td></tr><tr><td>

Allow reference field links\[enableLinks\]

</td><td>

When enabled, reference field links will be active.Default: **true**

</td></tr><tr><td>

Fetch highlighted values\[runHighlightedValuesQuery\]

</td><td>

Render highlighted values in the list based on a predefined configuration.Default: **true**

</td></tr><tr><td>

Highlighted values configuration\[highlightedValueConfigId\]

</td><td>

The highlighted value configuration you want to use to render highlighted values.

</td></tr><tr><td>

Shade alternate rows\[shadeAlternateRows\]

</td><td>

Apply a background color to every other row in the list.

</td></tr><tr><td>

Wrap cell content\[wrapCellContent\]

</td><td>

Allows multiple lines of text in a cell up to the maximum character limit before truncation.

</td></tr><tr><td>

Max characters per cell\[maxCharacters\]

</td><td>

Sets the maximum character limit for cell content before truncation. This can be overridden on a per-column basis.Default: **4000**

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Presentational List component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

\[Omitted image "presentational-list-events.png"\] Alt text: Presentational list events

The Events tab shows the events used by the Presentational List component. Events with presets are marked with the **Preset** badge. To show events that do not have preset configurations, select **+ Add event mapping**. If the component has only one event and that event does not have a preset, the event is displayed and is ready for configuration.

### Event handlers

Event handlers work with data resources to link the Presentational List actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Connected list__**

    This preset provides data handlers for these events:

    -   Expanding and collapsing groups
    -   Requesting cell edits
    -   Submitting cell edits
    -   Selecting cell link
    -   Selecting cell person
    -   Applying column filter
    -   Reordering columns
    -   Updating column width
    -   Selecting context action
    -   Dispatching custom cell/popover/overlay action
    -   Selecting header cell text
    -   Selecting message action
    -   Toggling row checkbox
    -   Focusing on a row
    -   Reaching scroll bottom

### Event descriptions

<table id="table_nr3_s2m_dcc"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All groups expanded/collapsed\[NOW\_LIST\#ALL\_GROUPS\_TOGGLED\]

</td><td>

The all groups expand/collapse button in the header row is clicked.Payload:

isExpanded: Boolean indicating whether this group is expanded.

</td></tr><tr><td>

Cell edit requested\[NOW\_LIST\#CELL\_EDIT\_REQUESTED\]

</td><td>

A cell is double-clicked or entered when cell editing is on, to request a cell edit.Payload:

-   context: The context of the location of the cell edit action.
-   componentTag: Component tag to render inside the cell editor.

</td></tr><tr><td>

Cell edit submitted\[NOW\_LIST\#CELL\_EDIT\_SUBMITTED\]

</td><td>

A cell editor popover's apply button is pressed.Payload:

-   context: The location context of cell edit.
-   oldValue: Previous value of the cell before the edit.
-   newValue: New value entered during cell edit.

</td></tr><tr><td>

Cell link selected\[NOW\_LIST\#CELL\_LINK\_CLICKED\]

</td><td>

A user selects an actionable link in a non-disabled link-type cell.Payload:

-   cell: The cell that contains the content being selected.
-   event: The name of the event that is dispatched when the content is clicked.
-   context: Context of location of this cell and the data of the cell.

</td></tr><tr><td>

Cell person clicked\[NOW\_LIST\#CELL\_PERSON\_CLICKED\]

</td><td>

Content in a \(non-disabled\) person type cell is clickedPayload:

-   cell: The cell that contains the content being selected.
-   event: The name of the event that is dispatched when the content is clicked.
-   context: Context of the location of this cell.

</td></tr><tr><td>

Column filter applied\[NOW\_LIST\#COLUMN\_FILTER\_APPLIED\]

</td><td>

A user submits changes to a column's filter condition, including clearing the filter.Payload:

-   columnKey: The key of the column that the filter was applied to.
-   oldValue: The previous filter value. It may be empty if the filter did not exist or if the previous operator did not require a value.
-   newValue: The new filter value. It may be empty if the filter is cleared or if the operator does not require a value. It may be the same as the old value if other parts of the filter have changed.
-   oldOperator: The old filter operator. It may be empty if the filter did not exist.
-   newOperator: The new filter operator. It may be the same as the old operator if other parts of the filter have changed.

</td></tr><tr><td>

Column reordered\[NOW\_LIST\#COLUMNS\_REORDERED\]

</td><td>

A column is dragged to a new relative location.Payload:

-   oldColumns: Array containing old column data.
-   newColumns: Array containing new column data.
-   reorderedColumns: The columns that have been reordered.

</td></tr><tr><td>

Column widths updated\[NOW\_LIST\#COLUMN\_WIDTHS\_UPDATED\]

</td><td>

A column is dragged to adjust width using resize slider.Payload:

data: The object containing data related to column resize operation.

</td></tr><tr><td>

Context action clicked\[NOW\_LIST\#CONTEXT\_ACTION\_CLICKED\]

</td><td>

A list context action is clicked, either through the row actions icon buttons, the row actions context menu, the column header actions popover, the group actions, or the cell actions popover.Payload:

-   actionItem: The action item containing identifying info for the action clicked.
-   context: Context for the action clicked.

</td></tr><tr><td>

Custom cell/popover/overlay action dispatched\[NOW\_LIST\#CUSTOM\_COMPONENT\_ACTION\_DISPATCHED\]

</td><td>

Any action from the provided list of custom cell/popover/overlay actions is dispatched.Payload:

-   context: The context of the location of the interaction.
-   cellContext: The cell context context of the location of the interaction.

</td></tr><tr><td>

Group expanded/collapsed\[NOW\_LIST\#GROUP\_TOGGLED\]

</td><td>

The group expand/collapse button on an individual group is clicked.Payload:

-   groupContext: Context information about the group that was interacted with.
-   isExpanded: Whether the group is expanded or not.
-   groupIdsException: The Array with group ids that are expanded.

</td></tr><tr><td>

Header cell text clicked\[NOW\_LIST\#HEADER\_CELL\_TEXT\_CLICKED\]

</td><td>

A list header cell's text is clicked.Payload:

column: The column ID of the clicked column header.

</td></tr><tr><td>

Message action clicked\[NOW\_LIST\#MESSAGE\_OVERLAY\_ACTION\_CLICKED\]

</td><td>

An action within an actionable message is clicked.Payload:

-   action: The name of the action emitted by the actionable message.
-   location: Whether this was emitted from the top or the bottom actionable message.
-   key: The unique identifier for this actionable message.

</td></tr><tr><td>

Row check box toggled\[NOW\_LIST\#ROW\_SELECT\_TOGGLED\]

</td><td>

A user selects or deselects a check box in a row.Payload:

-   value: Identifying key of the row whose checkbox was toggled.
-   checked: Boolean indicating whether the new value of the checkbox is checked or unchecked.
-   selectedRows: Array of IDs representing the selected rows.

</td></tr><tr><td>

Row focused\[NOW\_LIST\#ROW\_FOCUSED\]

</td><td>

Any body row or cell in the list is clicked.Payload:

context: The location context of the focused row.

</td></tr><tr><td>

Virtualized scrolling bottom reached\[NOW\_LIST\#VIRTUALIZED\_SCROLL\_BOTTOM\_REACHED\]

</td><td>

A user reaches the bottom of the list when virtualized scrolling is enabled.

</td></tr></tbody>
</table>