---
title: Using sets in layouts
description: Learn about the various ways sets can be displayed and about their settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/layouts-sets.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure sets, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Using sets in layouts

Learn about the various ways sets can be displayed and about their settings.

## Display types

Sets can be displayed in several ways:

-   As table rows where each index is displayed horizontally:

    \[Omitted image "cpq-sets-layouts-display-types-table-rows.png"\] Alt text: Display types

-   As table columns where each index is displayed vertically:

    \[Omitted image "cpq-sets-layouts-display-types-table-columns.png"\] Alt text: Display types

-   As list rows:

    \[Omitted image "cpq-sets-layouts-display-types-list-rows.png"\] Alt text: Display types

-   As a set repeater where each index is tied to a tier:

    \[Omitted image "cpq-sets-layouts-display-types-set-repeater.png"\] Alt text: Display types

    Set repeaters are distinct in their administration. For more information about set repeaters, see [Creating a Set Repeater](https://logikio.atlassian.net/wiki/spaces/CS/pages/1614446937/Creating+a+Set+Repeater).


To manage the different display types, find the set in the Layout Wizard and select the gear icon. Here the admin has two options for Display Type: Table and List. Table is a basic grid, while List is a series of tiles.

\[Omitted image "cpq-sets-layouts-display-types.png"\] Alt text: Display types

## General settings

-   Expand Direction: Allows the user to specify how the set is formatted.
    -   Rows: Each index is displayed as a row. As the set size increases, it will expand down the page.
    -   Columns: Each index is displayed as a column As the set size increases, it will expand horizontally to the right.
-   Maximum Height: The height of the set.
-   Show Index \(Table Display Type only\): Whether the index is displayed in the set.

    \[Omitted image "cpq-sets-layouts-general-settings-show-index.png"\] Alt text: General settings

-   Index Label Template \(Table Display Type Only\): display a prefix or suffix string to the index numbers. Helps provide context of each index.

    \[Omitted image "cpq-sets-layouts-general-settings-index-level-template-1.png"\] Alt text: layout

    \[Omitted image "cpq-sets-layouts-general-settings-index-level-template-2.png"\] Alt text: General settings

-   Vertical Alignment \(List Display Type Only\): Control the alignment.
    -   Middle

        \[Omitted image "cpq-sets-layouts-general-settings-vertical-alignment-middle.png"\] Alt text: General settings

    -   Top

        \[Omitted image "cpq-sets-layouts-general-settings-vertical-alignment-top.png"\] Alt text: General settings


## Message settings

These options allow the admin to control how and where messages are displayed.

\[Omitted image "cpq-sets-layouts-message-settings.png"\] Alt text: Message settings

-   Show message summary: summarizes all message actions and recommendation messages in one position. Toggling this to true will show the summary. Toggling to false, removes the summary.
-   Message summary position: display the message summary above or below the set. The following image shows Show Message Summary = true and Message Summary Position = Top.

    \[Omitted image "cpq-sets-layouts-message-settings-1.png"\] Alt text: Message settings

-   Show message indicator inside cell \(table display type only\): places a color-coded triangle in the cell that caused the message.
-   Show message when hovering indicator \(table display type only\): displays messages when users hover over the color-coded triangle.

    \[Omitted image "cpq-sets-layouts-message-settings-2.png"\] Alt text: Message settings


## Size settings

The size of the set refers to the number of indexes that will be displayed. This is applicable to sets with the size type of field, not for associate picklist sets. A size of 1 means that there is 1 index. A size of 10 means that there are 10 indexes.

\[Omitted image "cpq-sets-layouts-size-settings.png"\] Alt text: Message settings

-   Show size field: shows or hides the size field.

    \[Omitted image "cpq-sets-layouts-size-settings-show-size-field.png"\] Alt text: Message settings

-   Show Increment Size Button: control whether the green + icon is visible.

    \[Omitted image "cpq-sets-layouts-size-settings-show-increment-size.png"\] Alt text: Message settings

-   Size Field Display Type: Pick between a number field or a slider field for user input.

    \[Omitted image "cpq-sets-layouts-size-settings-size-field-display-type.png"\] Alt text: Message settings

-   Placement of Size Field: Control the location of the size field relative to the set itself.
-   Submit Size Changes on Field Input \(Table Display Type Only\): When true, the set adjusts according to any keystroke change in the size input field.
-   Display a Confirmation Before Submitting Size Changes \(Table Display Type Only\): This property displays the confirmation button when set true. False hides the confirmation button.

## Inline control settings

These settings refer to options in the index column menus.

\[Omitted image "cpq-sets-layouts-inline-control-settings.png"\] Alt text: Inline control settings

-   Show Add Button Before an Index: showAddBefore: show/hide the **Add Row Above** control.
-   Show Add Button After an Index: showAddAfter: show/hide the **Add Row Below** control.
-   Show Dropdown Controls: show or hide the inline size control menu.

    \[Omitted image "cpq-sets-layouts-inline-control-settings-menu.png"\] Alt text: Inline control settings

    The dropdown controls setting refers to the caret icon on the index. It is not to be confused with the green bar for inserting indexes. Add Row Above and Add Row Below refer to the other controls here.


## Selection settings

Selection settings apply only to the list display type. These controls affect how the user interacts with a set that is displayed as a list.

\[Omitted image "cpq-sets-layouts-selection-settings.png"\] Alt text: Inline control settings

-   Show Selector: toggles selectors on and off.
-   Selection Type: choose between Single or Multiple. Single will appear as radio buttons and Multiple will appear as check boxes.

    Example of single selection where Show Selector is true:

    \[Omitted image "cpq-sets-layouts-selection-settings-single.png"\] Alt text: Inline control settings

    Example of multiple selection where Show Selector = false:

    \[Omitted image "cpq-sets-layouts-selection-settings-multiple.png"\] Alt text: Inline control settings

-   Boolean field for selection: specify a field in the set that will be marked as true. This is required for the selection to work. If desired, the value can be displayed in the set itself:

    \[Omitted image "cpq-sets-layouts-selection-settings-boolean.png"\] Alt text: Inline control settings


**Note:** All of the set settings are editable in the value column of the layout CSV file. Admins are still able to update the JSON there and make changes. If this method is chosen, the entire list of properties does not need to be included, but be sure to keep the proper data structure intact.

## Search settings

Search settings apply only to the list display type.

\[Omitted image "cpq-sets-layouts-search-settings.png"\] Alt text: Inline control settings

## Search settings \(List display type only\)

-   Source Field: The global field that, when the user changes, triggers the UI to search based on the value of the field.
-   Target Field: The set subfield that has its value compared to the source fieldʼs value to determine whether it is a match.

## Displaying aggregates

Aggregates are a way to evaluate the data in a set. Set aggregates have five types and can aggregate on any field type. The types are:

-   Average
-   Count
-   Max
-   Min
-   Sum

For example, a sum aggregate on a number field will add all the instances of that subfield across all indexes. The admin can display that aggregate just as with any other field in the layout by specifying the field in the Layout Wizard.

The variable name for aggregates have the following syntax: `set.{set variable name}.{aggregate variable name}`

**Related topics**  


[How sets interact with the rest of a blueprint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/how_sets_interact_with_the_rest_of_the_blueprint.md)

[Creating set aggregates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/creating_set_aggregates.md)

