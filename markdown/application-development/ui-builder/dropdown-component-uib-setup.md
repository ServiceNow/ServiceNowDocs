---
title: Dropdown component setup
description: The Dropdown component enables users to select one or more options using a dropdown menu.Define the styles, button size of the dropdown menu, and ARIA properties value of your Dropdown component with these properties.Select event handlers to configure the actions \(events\) provided with the Dropdown component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/dropdown-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Dropdown component setup

The Dropdown component enables users to select one or more options using a dropdown menu.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Dropdown that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "dropdown-content-tree.png"\] Alt text: Image showing dropdown content tree

2.  Select the Dropdown component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Dropdown label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Dropdown component properties

Define the styles, button size of the dropdown menu, and ARIA properties value of your Dropdown component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_ipx_wll_qnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Placeholder text \[placeholder\]

</td><td>

Default label text when no items are selected. If you do not specify a value, especially in the case of iconic dropdowns, provide `tooltipContent` and/or an `aria-label` through the **configAria** property.

</td></tr><tr><td>

Variant\[variant\]

</td><td>

Selects button style of the dropdown trigger.Possible choices are:

-   `primary`
-   `primary-selection`
-   `secondary`
-   `secondary-selection`
-   `tertiary`
-   `tertiary-selection`

</td></tr><tr><td>

Hide container\[bare\]

</td><td>

Makes the dropdown trigger border and background transparent but retains its variant style setting when using an iconic button.

</td></tr><tr><td>

Size\[size\]

</td><td>

Button size of the dropdown trigger: Small, medium, or large.

</td></tr><tr><td>

Search behavior\[search\]

</td><td>

Controls how to filter the items as the user types into the integrated search input.

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Disables the dropdown and prevents the dropdown from opening when the user interacts with it.

</td></tr><tr><td>

Label\[label\]

</td><td>

Sets the value of the label string used.

</td></tr><tr><td>

Label position\[labelPosition\]

</td><td>

Sets the position of the label relative to the dropdown trigger.

</td></tr><tr><td>

Label size\[labelSize\]

</td><td>

Sets the size of the label used.

</td></tr></tbody>
</table><table id="table_zzc_n22_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Placeholder icon\[icon\]

</td><td>

Placeholder icon to include in the dropdown trigger. This icon is replaced with the icon of a selected dropdown item if the item has an icon configured.

</td></tr><tr><td>

Hide caret\[hideCaret\]

</td><td>

Hides the default triangular caret icon that appears in the dropdown trigger.

</td></tr></tbody>
</table><table id="table_mks_522_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show padding\[showPadding\]

</td><td>

Includes side padding on bare buttons. By default, bare buttons with labels don't have side padding.

</td></tr></tbody>
</table><table id="table_jb4_cf2_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List items \[items\]

</td><td>

Array of dropdown itemsDropdown item properties:

-   `id` \(string \| number\): Unique identifier for the item.
-   `label` \{string\}: Text that describes the item.
-   `sublabel` \{string\}: Additional text for the item.
-   `count` \{number\}: Numeric indicator displayed next to the item.
-   `icon` \{string\}: Name of the icon to display next to the item. See the `now-icon` API and icon gallery for the list of valid names. Cannot be used with `presence` or `avatarProps`.
-   `disabled` \{Boolean\}: When true, the dropdown item is visible but not selectable by the user.
-   `presence` \("available" \| "away" \| "busy" \| "offline"\): Online status of a user to display in a dropdown list of users or statuses. Cannot be used with `icon` or `avatarProps`.

</td></tr></tbody>
</table><table id="table_zc3_jf2_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selection\[select\]

</td><td>

Determines the action when a user selects an item in the dropdown menu.The options include:

-   **single**: The panel closes, the trigger label is updated with the label of the selected list item, and the list item is marked as selected.
-   **multi**: The panel stays open, the trigger label is updated with the selected list item count, and the list item's selected state is toggled on or off.
-   **none**: The panel closes, the trigger label is not updated, and the list item is not marked as selected.

</td></tr><tr><td>

Selected items\[selectedItems\]

</td><td>

Array of IDs representing selected dropdown panel items. If multi-select mode isn't enabled, each time the user selects a list item, the previously selected ID is replaced with the new ID. If multi-select mode is enabled, IDs are added to or removed from the list. Use `manage-selected-items` to override the default behavior and handle the NOW\_DROPDOWN\#SELECTED\_ITEMS\_SET event manually.

</td></tr><tr><td>

Hide selected item\[hideLabel\]

</td><td>

Hides the selected items in the dropdown trigger. By default, the dropdown displays the selected item or a count of selected items in place of the placeholder text of the dropdown trigger label.

</td></tr></tbody>
</table><table id="table_bzw_hg2_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Panel position\[panelFitProps\]

</td><td>

Properties to configure the dropdown panel.Valid keys are:

-   **position**: Array of possible positions in which to place the panel, relative to its target, such as `bottom-start` or `top-start`.
-   **constrain**: Object specifying size constraints relative to the panel's target. Choices are: `minHeight`, `minWidth`, `maxWidth` and `maxHeight`.
-   **offset**: Number of pixels to offset the panel from the trigger.

</td></tr><tr><td>

Opened\[opened\]

</td><td>

Automatically updates when the user opens or closes the dropdown. Use `manage-opened` to override the default behavior and handle the NOW\_DROPDOWN\#OPENED\_SET event manually.

</td></tr></tbody>
</table><table id="table_cq5_3h2_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tooltip text\[tooltipContent\]

</td><td>

Text displayed inside the tooltip.

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

An object whose keys reference a specific HTML element within the dropdown. The value of each key is an object that contains an ARIA property and corresponding value. These ARIA properties are set on the specified element. The `trigger` key corresponds to the inner HTML `<button>` that acts as the dropdown trigger.

</td></tr></tbody>
</table>## Dropdown component events

Select event handlers to configure the actions \(events\) provided with the Dropdown component.

The Events tab shows the events used by the Dropdown component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the dropdown actions to the data you want to display to your users. Expand the event in the list and add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_mzv_1ml_qnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dropdown list visible

</td><td>

The user opens the dropdown menu, and the content renders in the DOM. The `content` property is a node list containing the dropdown's inner `now-dropdown-list` element.

</td></tr><tr><td>

Dropdown list hidden

</td><td>

The user closes the dropdown menu, and the content is fully removed from the DOM.

</td></tr><tr><td>

Dropdown opened set

</td><td>

The user opens or closes the dropdown menu.Payload contains:

-   **true**: Dropdown opens
-   **false**: Dropdown closes

</td></tr><tr><td>

Selected items changed

</td><td>

The user changes the selected items and the Selection is set to **Single** or **Multi**. The event contains these keys:-   **value**: An array containing either a single ID or multiple IDs of the selected items.
-   **items**: An array of objects of the item or items selected from the dropdown list.

</td></tr><tr><td>

Item selected

</td><td>

The user selects an item and the Selection is set to **None**. The event contains a reference to the clicked item. Handle this action for dropdown menus in which `select="none"`.

</td></tr></tbody>
</table>