---
title: List - Simple component setup
description: The List-Simple component is a list for smaller spaces such as landing pages, where the list is likely one of many components on a page.Configure the filtering and sorting capabilities of your List-Simple component with these properties.Select event handlers to configure the actions \(events\) provided with the List-Simple component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/list-simple-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# List - Simple component setup

The List-Simple component is a list for smaller spaces such as landing pages, where the list is likely one of many components on a page.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your List-Simple that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "list-simple-content-tree.png"\] Alt text: List - Simple content tree.

2.  Select the List-Simple component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the List-Simple label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## List - Simple component properties

Configure the filtering and sorting capabilities of your List-Simple component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
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

Edit fixed filter\[fixedQuery\]

</td><td>

Apply fixed query filters to filter the list. Users can't edit or remove a fixed filter.

</td></tr><tr><td>

Follow filters\[followFilters\]

</td><td>

Set Follow filters to true in order to have the simple list reflect changes from the dashboard filter. When set to false, the simple list will not respond to the changes in the dashboard filter.Default: **true**

</td></tr></tbody>
</table><table id="table_gxw_ysb_kvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

Maximum rows\[limit\]

</td><td>

Maximum number of rows to display per page. This value input overrides user preferences. For example, if the value input is set to 10, the list always displays 10 records regardless of user preference. To honor user preferences, leave the field blank.

</td></tr><tr><td>

Hide "View all" footer\[hideViewAll\]

</td><td>

Show or hide **View All** link at the footer of list. Default: **false**

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

</td></tr><tr><td>

Hide empty state image\[hideEmptyStateImage\]

</td><td>

Show or hide the empty state image for the list.Default: **false**

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

Hide column resizing\[hideColumnResizing\]

</td><td>

Show or hide the column resizing button and header sliders. Default: **false**

</td></tr><tr><td>

Hide column filteringhideColumnFiltering\]

</td><td>

Show or hide column level filtering option.Default: **true**

</td></tr><tr><td>

Hide column sorting\[hideColumnSorting\]

</td><td>

Show or hide the column sorting controls in grid headers.Default: **false**

</td></tr></tbody>
</table><table id="table_ih3_ywc_2cc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Show border\[showBorder\]

</td><td>

Displays a border around the list.Default: **false**

</td></tr><tr><td>

Bare\[bare\]

</td><td>

If true, removes padding around list to provide more compact positioning on the page.Default: **true**

</td></tr></tbody>
</table><table id="table_btk_tzb_kvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide header\[hideHeader\]

</td><td>

Option to show or hide the header.Default: **false**

</td></tr><tr><td>

Hide title\[hideTitle\]

</td><td>

Show or hide the title in the list header.Default: **false**

</td></tr><tr><td>

Title\[listTitle\]

</td><td>

Title to display at the top of the list.

</td></tr><tr><td>

Hide total number of records\[hideTitleRowCount\]

</td><td>

Show or hide the row count in the list header.Default: **false**

</td></tr><tr><td>

Hide last refresh information\[hideLastRefreshedText\]

</td><td>

Show or hide the text label that displays the time of the last list refresh.Default: **false**

</td></tr><tr><td>

Hide option to refresh\[hideRefreshButton\]

</td><td>

Show or hide the refresh button in the list header.Default: **false**

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

</td></tr></tbody>
</table>## List-Simple component events

Select event handlers to configure the actions \(events\) provided with the List-Simple component.

The Events tab shows the events used by the List-Simple component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the List-Simple actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_ovm_lqx_pnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scroll Updated

</td><td>

The user scrolls the list. This event triggers once per second. Payload:

-   **timestamp**: Timestamp when the scroll of the table was initiated
-   **table**: Name of the current table

</td></tr><tr><td>

Reference link clicked

</td><td>

The user clicks the first link in a row. Payload:

-   **row**: The row object, containing the ID and display value
-   **table**: Name of the table to which the selected row belongs
-   **listTable**: Name of the table viewed when selecting a row
-   **nativeEvent**: The event object
-   **sys\_id**: System ID of the record selected

</td></tr><tr><td>

"View All" Clicked

</td><td>

User selects the `View All` link.Payload:

-   **listTitle**: Title of the list being viewed
-   **table**: Table name of the list being viewed
-   **query**: Query condition applied to the list being viewed
-   **columns**: Visible columns in the list being viewed

</td></tr><tr><td>

Data Fetch Requested

</td><td>

Data is requested by a record list. Payload includes **timestamp**: Timestamp when the data fetch was requested for the table

</td></tr><tr><td>

Data Fetch Succeeded

</td><td>

A data fetch succeeded. Payload:

-   **listTitle**: Title to display at the top of the list
-   **query**: Encoded query string that filters results of the current table
-   **table**: Name of the current table
-   **timestamp**: Timestamp when the data fetch request for the table succeeded

</td></tr><tr><td>

Data Fetch Failed

</td><td>

A user data request has failed.Payload includes: `error`: The error object containing the reason the data fetch failed

</td></tr></tbody>
</table>