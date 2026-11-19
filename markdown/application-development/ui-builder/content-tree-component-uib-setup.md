---
title: Content tree component setup
description: The Content tree component combines and organizes data into an expandable and selectable tree structure. You can configure the tree structure to include options such as identifiers, highlighted values, chevrons, text, icons, and dividers.Configure the appearance and features of the Content tree component.Select event handlers to configure the actions \(events\) provided with the Content tree component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/content-tree-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Content tree component setup

The Content tree component combines and organizes data into an expandable and selectable tree structure. You can configure the tree structure to include options such as identifiers, highlighted values, chevrons, text, icons, and dividers.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Content tree that differentiates it from other components in the [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "content-tree-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Content tree component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Content tree label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Content tree component properties

Configure the appearance and features of the Content tree component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_bfr_rky_znb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size

</td><td>

size

</td><td>

Size of tree item label and icon.

</td></tr><tr><td>

Selection

</td><td>

select

</td><td>

Behavior when a user clicks a selectable tree item. Choose from the following options.-   **single** - only one tree item can be selected at a time
-   **multi** - multiple tree items can be selected at the same time
-   **none** - no tree items can be selected

</td></tr><tr><td>

Overflow

</td><td>

overflow

</td><td>

Behavior when tree items are too wide to fit in the space given to the tree. Choose from the following options.-   **scroll** - the entire tree scrolls horizontally in its container
-   **truncate** - the item text is truncated to prevent side scrolling
-   **wrap** - the item text wraps over multiple lines to prevent side scrolling

</td></tr><tr><td>

Trigger icon

</td><td>

triggerIcon

</td><td>

Type of expand/collapse icon a parent item displays.

</td></tr><tr><td>

Highlight immediate parent

</td><td>

highlightSelectedParent

</td><td>

Option to highlight the parent of the current selection with a different highlight color.

</td></tr><tr><td>

Hide icons on default

</td><td>

showActionsOnHover

</td><td>

Option to show icons only on hover.

</td></tr><tr><td>

Show dividers

</td><td>

showDividers

</td><td>

Option to display a border on the bottom of each tree item.

</td></tr><tr><td>

Show presence pattern

</td><td>

showPresencePattern

</td><td>

Option to display an accessible presence icon with a pattern to make it distinguishable by a means other than color.

</td></tr><tr><td>

Items

</td><td>

items

</td><td>

Array of tree item objects that describe each item in the tree.

</td></tr><tr><td>

Expanded items

</td><td>

expandedItems

</td><td>

Array of path IDs that trace the path of the item from the root of the tree to the expanded item. A path ID is an array of string or numeric values.

</td></tr><tr><td>

Selected items

</td><td>

selectedItems

</td><td>

Array of path IDs that trace the path of the item from the root of the tree to the selected item. A path ID is an array of string or numeric values.

</td></tr><tr><td>

Loading items

</td><td>

loadingItems

</td><td>

Array of tree items that are actively being loaded or that have recently failed to load children from the server. The array contains a path ID, an optional error flag, and an error message.

</td></tr><tr><td>

Search item

</td><td>

searchTerm

</td><td>

Text value to search for and highlight in tree item labels. Matching is case-insensitive and applies to all occurrences within an item label.

</td></tr><tr><td>

ARIA properties

</td><td>

configAria

</td><td>

A JSON field for configuring ARIA properties, such as **aria-braillelabel**.

</td></tr></tbody>
</table>## Content tree component events

Select event handlers to configure the actions \(events\) provided with the Content tree component.

The Events tab shows the events used by the Content tree component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Content tree actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Content tree item selected|Dispatched when the user selects an item on the content tree.|
|Content tree actionable item clicked|Dispatched when the user clicks an actionable tree item label.|
|Content tree action clicked|Dispatched when a user clicks a tree item action icon.|
|Content tree action mouseleave|Dispatched when a user's mouse stops hovering over a tree item action icon.|
|Content tree action mouseenter|Dispatched when a user's mouse hovers over a tree item action icon.|
|Content tree loading requested|Dispatched when a user triggers loading of a parent item's children from the server.|
|Content tree loading cancelled|Dispatched when a user cancels loading of a parent item's children from the server. Remove the item's path from the Loading items list even if it is currently in the error state. If the request can't be cancelled \(such as it used fetch\) and it succeeds later, then handle its response and add the children without re-expanding the item. If the request can't be cancelled and it fails later, then don't re-add the item to Loading items with an error message.|
|Content tree items set|Dispatched when the Items property should be updated.|
|Content tree expanded items set|Dispatched when the Expanded items property should be updated.|
|Content tree selected items set|Dispatched when the Selected items property should be updated.|

