---
title: Select component setup
description: The Select component is a form control that provides dropdown options for user selection.Configure the appearance and features of the Select component.Select event handlers to configure the actions \(events\) provided with the Select component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/select-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Select component setup

The Select component is a form control that provides dropdown options for user selection.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Select component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "select-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Select component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Select label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Select component properties

Configure the appearance and features of the Select component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_vdx_q5l_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Choose the **small** \(sm\) or **medium** \(md\) size.Default: **medium**

</td></tr><tr><td>

Search behavior\[search\]

</td><td>

Controls how to filter selectable items as the user types into the integrated search input. Choose from the following options.-   **None** - Hides integrated search input and prevents filtering
-   **Managed** - Filter items manually
-   **Initial** - Filter items whose label or sublabel begin with the input value \(case insensitive\)
-   **contains**- Filter items whose label or sublabel contain the input value \(case insensitive\)

</td></tr><tr><td>

Disabled

</td><td>

Option to disable the selection dropdown and prevent user interactions. The color of the component is muted to indicate that it's unavailable.

</td></tr><tr><td>

Auto-focus\[autofocus\]

</td><td>

Option to place focus inside the component when the page loads.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **horizontal**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **vertical** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr></tbody>
</table><table id="table_b3l_3vl_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List items\[items\]

</td><td>

An array of dropdown list items and/or dropdown list sections that the user can select from.

</td></tr><tr><td>

Selected item\[selectedItem\]

</td><td>

The ID of the selected item from the list items array.

</td></tr><tr><td>

Item size constraints\[itemsListConstrain\]

</td><td>

Object of sizing constraints properties to enforce on the item list. Set the following sizing properties.-   **width** - Default width of the item in pixels. Specify the string `target` to set the item width to the Select component width.
-   **minWidth** - Minimum width of the item in pixels. Specify the string `target` to set the item width to the Select component width.
-   **maxWidth** - Maximum width of the item in pixels. Specify the string `target` to set the item width to the Select component width.
-   **height** - Default height of the item in pixels
-   **minHeight** - Minimum height of the item in pixels
-   **maxHeight** - Maximum height of the item in pixels

</td></tr></tbody>
</table><table id="table_h2d_pvl_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Text describing the purpose of the select input to the user. The text displays above the list component.

</td></tr><tr><td>

Wrap label\[wrapLabel\]

</td><td>

If the label doesn't fit on one line, wraps the label.

</td></tr><tr><td>

Required\[required\]

</td><td>

Option to require users to enter a component value before they can complete the form.

</td></tr><tr><td>

Hide required indicator\[hideRequiredIndicator\]

</td><td>

Option to visually show or hide the required indicator for the component. Use this for forms where most components are required, along with the **Optional** property to highlight the components that are not required.

</td></tr><tr><td>

Optional\[optional\]

</td><td>

Option to visually indicate that the user does not need to complete the component before completing the form. Use this for forms where most components are required, along with the **Hide required indicator** property to highlight the components that are not required.

</td></tr><tr><td>

Helper text\[helperContent\]

</td><td>

Instructions to guide user interaction with the component such as password requirements. When defined, an iconic button with a popover appears next to the field label to display the text. Use plain text to allow the text to be translatable.

</td></tr><tr><td>

Read onlyreadonly

</td><td>

Option to make the field read-only to prevent users from modifying the value.Default: **false**

</td></tr></tbody>
</table><table id="table_tdk_vvl_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

Option to visually indicate that the component is in an incorrect state. Use this for forms that validate input to guide users to correct invalid component values.

</td></tr><tr><td>

Alert messages\[messages\]

</td><td>

Array of alert messages that display below the field. The following list describes each object's properties:-   `content`: The text of the alert message.
-   `status`: The type of alert to display.
-   `icon`: Icon to display at the start of the alert message.

Default:

```

{
    "name": "content",
    "label": "Content",
    "fieldType": "string",
    "translatable": true
},
{
    "name": "status",
    "label": "Status",
    "fieldType": "choice",
    "typeMetadata": {
        "choices": [
            {
                "label": "Critical",
                "value": "critical"
            },
            {
                "label": "Warning",
                "value": "warning"
            },
            {
                "label": "Positive",
                "value": "positive"
            },
            {
                "label": "Info",
                "value": "info"
            },
            {
                "label": "Suggestion",
                "value": "suggestion"
            }
        ]
    }
},
{
    "name": "icon",
    "label": "Icon",
    "fieldType": "icon"
}

```

</td></tr></tbody>
</table><table id="table_bbp_xvl_dwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ARIA properties\[configAria\]

</td><td>

An object whose keys reference a specific HTML element within the dropdown. The value of each key is an object that contains an ARIA property and corresponding value. These ARIA properties are set on the specified element. The `trigger` key corresponds to the inner HTML `<button>` that acts as the dropdown trigger.

</td></tr><tr><td>

Landmark\[landmark\]

</td><td>

Enable the Landmark Focus keyboard shortcut to focus on this select.

</td></tr></tbody>
</table>## Select component events

Select event handlers to configure the actions \(events\) provided with the Select component.

The Events tab shows the events used by the Select component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Select actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Select list visible|Dispatched when the select menu opens and renders the content. This action only fires after the select menu is rendered in the DOM. The `content` property is a node list containing the select menu's inner `now-dropdown-list` element.|
|Select list hidden|Dispatched when the select menu has been closed and removed. This action only fires after the select menu is fully removed from the DOM.|
|Select invalid set|Dispatched when the input is required and the user has not selected an option from the drop down list. Set the **manage-invalid** property to override the default behavior and handle this action manually.|
|Item selected|Dispatched when the user selects an item from the dropdown list. Set the **manage-selected-item** property to override the default behavior and handle this action manually.|
|Select search term set|Dispatched when the user inputs text in the internal search field.|

