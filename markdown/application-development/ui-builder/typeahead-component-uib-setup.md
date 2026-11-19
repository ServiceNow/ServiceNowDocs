---
title: Typeahead component setup
description: The Typeahead component provides users with a relevant dropdown of selectable options as they type in an input field.Define the controls to filter the search as the user types into the integrated search input fields and the search behavior of the Typeahead component with these properties.Select event handlers to configure the actions \(events\) provided with the Typeahead component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/typeahead-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Typeahead component setup

The Typeahead component provides users with a relevant dropdown of selectable options as they type in an input field.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Typeahead that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "typeahead-multi-content-tree.png"\] Alt text: Image showing Typeahead component content tree

2.  Select the Typeahead component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Typeahead label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Typeahead component properties

Define the controls to filter the search as the user types into the integrated search input fields and the search behavior of the Typeahead component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_xmn_srj_znb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Size of the component in either **small** or **medium**.Default: **medium**

</td></tr><tr><td>

Search behavior\[search\]

</td><td>

Control to filter the items in the integrated search input.

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Disables user click interactions when **True**. The typeahead component is grayed out when disabled.

</td></tr><tr><td>

Read-only\[readonly\]

</td><td>

By enabling this property, the user cannot modify the value of the input field. The input field is not disabled in this setting.

</td></tr><tr><td>

Auto-focus\[autofocus\]

</td><td>

When **True**, the focus is automatically placed inside the input field when the page loads.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **"layout":"horizontal"**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **"layout":"vertical"** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr></tbody>
</table><table id="table_kjl_g1c_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Placeholder text\[placeholder\]

</td><td>

Hint about the expected input text.

</td></tr><tr><td>

Value\[value\]

</td><td>

Value for the input field.**Note:** This field remains empty unless it has pre-populated data.

</td></tr><tr><td>

Manage value\[manageValue\]

</td><td>

If set to **true**, overrides automatic updates to the **Value** property. Use the **Text entered** event to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Name\[name\]

</td><td>

Name of the field control.

</td></tr><tr><td>

Max. characters\[maxLength\]

</td><td>

Maximum number of characters for the typeahead field.

</td></tr></tbody>
</table><table id="table_vvv_rbc_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List items\[items\]

</td><td>

Possible items for selection.

</td></tr><tr><td>

Selected item\[selectedItem\]

</td><td>

ID of the selected item.

</td></tr><tr><td>

Manage selected item\[manageSelectedItem\]

</td><td>

If set to **true**, overrides automatic updates to the **Selected item** property. Use the **Item selected** event to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Item size constraints\[itemListConstrain\]

</td><td>

Sizing constraints on the items list.

</td></tr></tbody>
</table><table id="table_dqd_dbc_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Purpose of the selected field.

</td></tr><tr><td>

Wrap label\[wrapLabel\]

</td><td>

If the label doesn't fit on one line, wraps the label.

</td></tr><tr><td>

Required\[required\]

</td><td>

Use this property to indicate that the user must enter a value in the field before proceeding.Default: **false**

</td></tr><tr><td>

Hide required indicator\[hideRequiredIndicator\]

</td><td>

When true, the graphic that indicates the field is required is visually hidden. Set this property to **true** for forms where most fields are required. If this property is **true**, also set the **Optional** flag for any fields that are not requiredDefault: **false**

</td></tr><tr><td>

Optional\[optional\]

</td><td>

Visually indicates that the field is optional.Default: **false**

</td></tr><tr><td>

Helper text\[helperContent\]

</td><td>

Hint text to the users.

</td></tr></tbody>
</table><table id="table_k2v_hbc_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

When **true**, this flag indicates that the field is in an incorrect state. This information is visually reflected in the field display. This property is set automatically based on the current validity of the input field.

</td></tr><tr><td>

Manage invalid\[manageInvalid\]

</td><td>

If set to **true**, overrides automatic updates to the **Invalid** property. Use the **Typeahead invalid set** to intercept the requested change and handle it manually.Default: **false**

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
</table><table id="table_fgd_pbc_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ARIA properties\[configAria\]

</td><td>

A JSON field for configuring ARIA properties, such as **aria-braillelabel**.

</td></tr><tr><td>

Landmark\[landmark\]

</td><td>

Enable the Landmark Focus keyboard shortcut to focus on this typeahead.

</td></tr></tbody>
</table>## Typeahead component events

Select event handlers to configure the actions \(events\) provided with the Typeahead component.

The Events tab shows the events used by the Typeahead component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Typeahead actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_uzp_bdk_znb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Typeahead list visible

</td><td>

Dispatched when the typeahead menu opens and renders the content. This event is dispatched only after the typeahead menu is rendered in the DOM API. The payload contains the components inner `now-dropdown-list` element.

</td></tr><tr><td>

Typeahead list hidden

</td><td>

Dispatched when the typeahead menu has been closed and removed.

</td></tr><tr><td>

Typeahead invalid set

</td><td>

Dispatched when interaction with a field is complete and the validity of the field has changed.

</td></tr><tr><td>

Item selected

</td><td>

Dispatched when the user selects an item from the dropdown.

</td></tr><tr><td>

Text entered

</td><td>

Dispatched when the user types or pastes text in the field.

</td></tr><tr><td>

Typeahead enter keydown

</td><td>

Dispatched when the Enter key is pressed while focus is inside the typeahead, without highlighting an item from the items list. The payload contains the following:-   `name`: Name of the input field
-   `value`: Value of the input field

</td></tr></tbody>
</table>