---
title: List selector component setup
description: List selector is a visual component used to add, remove, or move multiple items in a form or list.Configure the items to appear in your List selector component.Select event handlers to configure the events provided with the List selector component. Event handlers work with data resources to link the List selector actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/list-selector-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# List selector component setup

List selector is a visual component used to add, remove, or move multiple items in a form or list.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for List selector that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "list-selector-content-tree.png"\] Alt text: List selector displayed in the page content tree.

2.  Select the List selector component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "list-selector-properties.png"\] Alt text: Shows the available properties for the list selector component in the config panel


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## List selector component properties

Configure the items to appear in your List selector component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mode\[mode\]

</td><td>

Population method for the list of available items. Select from the following modes:-   **Manual mode**: Requires setting a root table and manually defining the fields from that table to display in the available items list. Dot-walking is supported in manual mode only if the item has references defined. This is the default mode.
-   **Connected mode - table description**: Displays all the fields available in the specified table. When you select this mode, you can enable dot-walking to select fields referenced in other tables.

Default: **Manual mode**

</td></tr><tr><td>

View type\[viewType\]

</td><td>

Selects how to display the component. The choices are: -   **Compact**: Shows Available items in a single panel.
-   **Two panels**: Shows the Available items and Selected items in separate panels.
-   **Dot walk**: Splits the Available items list into two panels to display the dot walked path.

Default: **Dot walk**

</td></tr><tr><td>

Items Root\[itemsRoot\]

</td><td>

Root panel to be opened when the component opens. This property is only available for Manual mode.

</td></tr><tr><td>

Table name\[tableName\]

</td><td>

Table from which to display the fields in the list. This property is only available for Connected mode.

</td></tr><tr><td>

Allow Dot Walking\[allowDotWalking\]

</td><td>

If set to **true**, displays a selection tree that includes reference fields for dot-walking. This property is only available for Connected mode.Default: **false**

</td></tr><tr><td>

Show Variables\[showVariables\]

</td><td>

If set to **true**, displays variables and questions in available items.Default: **false**

</td></tr><tr><td>

Show extended fields\[showExtendedFields\]

</td><td>

If set to **true**, displays extended fields in available items. To align list selector with legacy dot-walking components **showExtendedFields** value should be bound to **glide.ui.list.allow\_extended\_fields**.

 Default: **false**

</td></tr><tr><td>

Included system ID\[includeSysId\]

</td><td>

If set to **true**, includes sysId in list of fields shown. This property is only available for Connected mode.Default: **false**

</td></tr><tr><td>

Items\[items\]

</td><td>

Items object for the manual population of available items. This property is only available for Manual mode.

</td></tr><tr><td>

Selected items\[selectedItems\]

</td><td>

List of selected fields for the list.

</td></tr><tr><td>

Unselectable items\[unselectableItems\]

</td><td>

List of items that are not selectable.

</td></tr><tr><td>

Available bucket label\[availableLabel\]

</td><td>

Label for the Available columns panel.

</td></tr><tr><td>

Selected bucket label\[selectedLabel\]

</td><td>

Label for the Selected columns panel.

</td></tr><tr><td>

Show count\[showCount\]

</td><td>

Badge showing the number of items in the available and selected columns panels.Default: **true**

</td></tr><tr><td>

Headers level\[headersLevel\]

</td><td>

Available and selected headings level \(1-6\). Doesn't affect title design.Default: **6**

</td></tr><tr><td>

Disable reorder of selected items \[disableReorder\]

</td><td>

Prevents users from reordering items in the Selected items list.Default: **false**

</td></tr><tr><td>

Show selected item path\[showSelectedItemPath\]

</td><td>

Opens the path to an item in the Available Items list when the user clicks that item in the Selected items list. For example: The user navigates to **action** &gt; **user** &gt; **location** and adds **location** to the Selected Items list. The user then continues to select items in the Available Items list. If the user selects **location** in the Selected Items list, the navigation path in the Available Items list changes to **action** &gt; **user** &gt; **location**.Default: **false**

</td></tr><tr><td>

Always show hidden controls \[showHiddenControls\]

</td><td>

If set to **true**, reveals all hidden controls inside the component. Some controls, such as the popover trigger, are hidden until the user hovers over the relevant element or puts focus in that element.Default: **false**

</td></tr><tr><td>

Search behavior\[search\]

</td><td>

As the user types into the integrated search input, determines how to filter the list items. Choices are: -   **initial**
-   **contains**

Default: **initial**

</td></tr><tr><td>

Hide reset warning message\[hideResetWarning\]

</td><td>

When set to **true**, hides reset warning message when list selector data reset after **tableName** or **itemsRoot** changes.

</td></tr></tbody>
</table>## List selector component events

Select event handlers to configure the events provided with the List selector component. Event handlers work with data resources to link the List selector actions to the data you want to display to your users.

The Events tab shows the events used by the List selector component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

\[Omitted image "list-selector-events.png"\] Alt text: Shows the events included with the list selector component

### Event handlers

Event handlers work with data resources to link the List selector actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Event descriptions

<table id="table_chr_fhz_fyb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selected items changed\[SELECTED\_ITEM\_SET\]

</td><td>

The user changes the list of selected items.Payload shows the entire selected items list.

</td></tr><tr><td>

Item selected\[ITEM\_SELECTED\]

</td><td>

The user selects or deselects and item.Payload:

-   **item**: The selected or deselected item
-   **selected**: Evaluates to **true** if the item is selected and **false** if the item is deselected.

</td></tr><tr><td>

Item expand requested\[ITEM\_EXPAND\_REQUESTED\]

</td><td>

The user clicks the chevron to expand an item.Payload:

-   **category**: Category of the selected item
-   **itemId**: The selected item's ID.
-   **item**: The expanded item object

</td></tr><tr><td>

Scroll reached bottom\[SCROLLED\_TO\_BOTTOM\]

</td><td>

The user reached the end of the category items by scrolling to the bottom of the panel.The payload includes **category**: The scrolled catetory \(panel\).

</td></tr></tbody>
</table>