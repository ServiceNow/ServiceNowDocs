---
title: Typeahead Multi component setup
description: The Typeahead Multi component supplements input fields with a dropdown panel of options in which more than one option can be selected. As users type into the field, multiple values are suggested. As typing continues, the suggested values are filtered or recomputed.Configure the filtering and display capabilities of your Typeahead Multi component with these properties.Select event handlers to configure the actions \(events\) provided with the Typeahead Multi component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/typeahead-multi-uib-component-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Typeahead Multi component setup

The Typeahead Multi component supplements input fields with a dropdown panel of options in which more than one option can be selected. As users type into the field, multiple values are suggested. As typing continues, the suggested values are filtered or recomputed.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Typeahead Multi component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "typeahead-multi-content-tree.png"\] Alt text: Content tree showing label "User dropdown typeahead multi"

2.  Select the Typeahead Multi component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Typeahead Multi label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Typeahead Multi component properties

Configure the filtering and display capabilities of your Typeahead Multi component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_uty_y1y_xnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **horizontal**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **vertical** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr><tr><td>

Read-only\[readonly\]

</td><td>

By enabling this property, the user cannot modify the value of the input field. The input field is not disabled in this setting.

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Disables user click interactions when `true`. The typeahead multi component is grayed out when disabled.

</td></tr><tr><td>

Search behavior\[search\]

</td><td>

Controls how to filter the items as the user types into the input.Values:

-   **Managed**: No filtering occurs
-   **Initial**: Items whose label or sublabel begins with the input value are displayed. Case-insensitive.
-   **Contains**: Items whose label or sublabel begins with the input value are displayed. Case-insensitive.

 Default: **Managed**

</td></tr><tr><td>

Auto-focus\[autofocus\]

</td><td>

When **true**, the focus is automatically placed inside the input on page load.

</td></tr></tbody>
</table><table id="table_p1w_k2c_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Placeholder text\[placeholder\]

</td><td>

Use this property to set a placeholder text for the input field. This text should suggest to the user what input is expected.

</td></tr><tr><td>

Value\[value\]

</td><td>

Value for the input field.**Note:** This field remains empty unless it has pre-populated data.

</td></tr><tr><td>

Manage value\[manageValue\]

</td><td>

If set to **true**, overrides automatic updates to the **Value** property. Use the **Field updated** event to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Name\[name\]

</td><td>

Name of the field control. Dispatched with the field value on user interaction.

</td></tr><tr><td>

Max. characters\[maxLength\]

</td><td>

Maximum number of characters for the typeahead field.

</td></tr></tbody>
</table><table id="table_olm_l2c_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List items\[items\]

</td><td>

An array of `DropdownListItem` or `DropdownListSection` objects that the user can select from.Default: `[{\"id\":\"usr1\",\"label\":\"User 1\",\"sublabel\":\"user1@servicenow.com\",\"avatarProps\":{\"userName\":\"User 1\",\"imageSrc\":\"http://i.pravatar.cc/24?u=33\",\"presence\":\"away\"}},{\"id\":\"usr2\",\"label\":\"User 2\",\"sublabel\":\"user2@servicenow.com\",\"avatarProps\":{\"userName\":\"User 2\",\"imageSrc\":\"http://i.pravatar.cc/24?u=34\",\"presence\":\"busy\"},\"disabled\":true},{\"id\":\"usr3\",\"label\":\"User 3\",\"sublabel\":\"user3@servicenow.com\",\"avatarProps\":{\"userName\":\"User 3\",\"imageSrc\":\"http://i.pravatar.cc/24?u=35\",\"presence\":\"offline\"}}]`

</td></tr><tr><td>

Selected items\[selectedItems\]

</td><td>

An array of `DropdownListItem` objects representing each selected item. Populated automatically with the selected items in the Items field.Default: `[]`

</td></tr><tr><td>

Manage selected items\[manageSelectedItems\]

</td><td>

If set to **true**, overrides automatic updates to the **Selected items** property. Use the **Multiple items selected** event to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Item size constraints\[itemsListConstrain\]

</td><td>

Optional sizing constraints to enforce on the items list popover. For each property, a positive integer can be specified that sets that constraint in pixels. You can also set the value to `target` for `width`, `minWidth`, or `maxWidth` keys. In this case, the items list is sized to match the width of the input field.Valid keys:

-   `width`
-   `minWidth`
-   `maxWidth`
-   `height`
-   `minHeight`
-   `maxHeight`

</td></tr></tbody>
</table><table id="table_dvg_m2c_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Label describing the overall purpose of the select fieldDefault: **Label**

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

When **true**, the graphic that indicates the field is required is visually hidden. Set this property to **true** for forms where most fields are required. If this property is **true**, also set the **Optional** flag for any fields that are not requiredDefault: **false**

</td></tr><tr><td>

Optional\[optional\]

</td><td>

Visually indicates that the field is optional.Default: **false**

</td></tr><tr><td>

Helper text\[helperContent\]

</td><td>

If set, a popover button appears next to the field label for displaying additional hint text to the user. Such text can include password requirements or other instructions for completing the field. Use plain text for the text to be translatable.

</td></tr></tbody>
</table><table id="table_ybz_m2c_4fc"><thead><tr><th>

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

If set to **true**, overrides automatic updates to the **Invalid** property. Use the **Typeahead multi invalid set** event to intercept the requested change and handle it manually.Default: **false**

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
</table><table id="table_zqm_2lc_4fc"><thead><tr><th>

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
</table>## Typeahead Multi component events

Select event handlers to configure the actions \(events\) provided with the Typeahead Multi component.

The Events tab shows the events used by the Typeahead Multi component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Typeahead Multi actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_vml_d2y_xnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Typeahead multi list visible

</td><td>

Dispatched when the typeahead menu opens and renders the content. This event is dispatched only after the typeahead menu is rendered in the DOM API. The payload contains the components inner `now-dropdown-list` element.

</td></tr><tr><td>

Typeahead multi list hidden

</td><td>

Dispatched when the typeahead menu has been closed and removed.

</td></tr><tr><td>

Typeahead multi invalid set

</td><td>

Dispatched when interaction with a field is complete and the validity of the field has changed. Contains the name and value of the field and a Boolean saying whether it's valid or not. To handle this action manually, set the `manage-invalid` property.

</td></tr><tr><td>

Multiple items selected

</td><td>

Dispatched when the user selects one or more items. Contains an array of IDs of the selected items. To handle this action manually, set the `manage-selected-items` property.

</td></tr><tr><td>

Field updated

</td><td>

Dispatched when the user changes the input field value. Contains the name and current value of the input field.

</td></tr><tr><td>

Typeahead multi enter keydown

</td><td>

Dispatched when the Enter key is pressed while focus is inside the typeahead, without highlighting an item from the items list. The payload contains the following:-   `name`: Name of the input field
-   `value`: Value of the input field

</td></tr></tbody>
</table>