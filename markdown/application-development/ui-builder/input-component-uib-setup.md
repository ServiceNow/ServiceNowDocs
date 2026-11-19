---
title: Input component setup
description: Use the Input component to give your users a place to input text, values, or symbols.Configure the appearance and functionality of your Input component. Choose placeholder text and labels to help users understand what to put into the field.Select event handlers to configure the actions \(events\) provided with the Input component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/input-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Input component setup

Use the Input component to give your users a place to input text, values, or symbols.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Input that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "input-content-tree.png"\] Alt text: UI Builder content tree with the Input component.

2.  Select the Input component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Input label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Input component properties

Configure the appearance and functionality of your Input component. Choose placeholder text and labels to help users understand what to put into the field.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_c1z_1lb_ynb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Size of the component in either small or medium.Default: **Medium**

</td></tr><tr><td>

Type\[type\]

</td><td>

Type of input field. Choose from Text, Email, IP, and Number.

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Disables the input field to prevent users from interacting with it.

</td></tr><tr><td>

Read only\[readonly\]

</td><td>

Prevents users from modifying the input field.

</td></tr><tr><td>

Auto-focus\[autofocus\]

</td><td>

Automatically brings the user to the input field when the page loads.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **"layout":"horizontal"**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **"layout":"vertical"** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr></tbody>
</table><table id="table_dcw_dc1_zcc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value\[value\]

</td><td>

Sets the value for the input field. Leave empty unless you have pre-populated data.

</td></tr><tr><td>

Identifier\[name\]

</td><td>

Reference name for the input field. This identifier is dispatched with the field value when a user interacts with the field.

</td></tr><tr><td>

Placeholder text\[placeholder\]

</td><td>

Text that appears in the input field before the user enters text. Placeholder text helps the user understand what input is expected.

</td></tr><tr><td>

Min. characters\[minlength\]

</td><td>

Sets a minimum number of characters for input fields.

</td></tr><tr><td>

Max. characters\[maxlength\]

</td><td>

Sets a maximum number of characters for input fields.

</td></tr><tr><td>

Multiple addresses allowed\[multiple\]

</td><td>

Lets users enter multiple, comma-separated email addresses in email fields.

</td></tr><tr><td>

Text align\[align\]

</td><td>

Alignment of the text within the input field.

</td></tr><tr><td>

Enable caret slot\[enableCaretSlot\]

</td><td>

When true, a slot is added to the component that follows the user's text cursor.

</td></tr><tr><td>

Mask config\[maskConfig\]

</td><td>

Defines the mask pattern, custom definitions, and placeholder text for formatting the text input. The following list describes the **Mask config** object's properties:-   `mask`: Defines the structure of the input. For example, "000-00-0000"
-   `definitions`: Specifies what kinds of characters are allowed at each position in the mask. For example, `{"0": "[0-9]"}`
-   `maskPlaceholder`: Placeholder text that displays the expected format. For example, "XXX-XX-XXXX"

```
{
  "mask": {
    "type": "string"
  },
  "definitions": {
    "type": "object"
  },
  "maskPlaceholder": {
    "type": "string"
  }
}
```

</td></tr></tbody>
</table><table id="table_orr_32h_zcc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Min. value\[min\]

</td><td>

Sets a minimum number value for number input fields.

</td></tr><tr><td>

Max. value\[max\]

</td><td>

Sets a maximum number value for number input fields.

</td></tr></tbody>
</table><table id="table_zy5_fc1_zcc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

User-visible label describing the input field.

</td></tr><tr><td>

Wrap label\[wrapLabel\]

</td><td>

If the label doesn't fit on one line, wraps the label.

</td></tr><tr><td>

Required\[required\]

</td><td>

Adds an indicator showing that the user must enter a value in the input field before proceeding.

</td></tr><tr><td>

Hide required indicator\[hideRequiredIndicator\]

</td><td>

Hides the required field indicator. You can set this flag to **true** for forms on which most of the fields are required.

</td></tr><tr><td>

Optional\[optional\]

</td><td>

Adds an indicator showing that the user does not need to enter a value into the input field before proceeding.

</td></tr><tr><td>

Helper content\[helperContent\]

</td><td>

Additional information to display to the user, such as password requirements or instructions. Adds an iconic button next to the input label that users can click to show hint text.

</td></tr></tbody>
</table><table id="table_rz4_td1_zcc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

Indicates that the field value is invalid. This state is visually reflected in the field display.

</td></tr><tr><td>

Validation pattern\[pattern\]

</td><td>

Regular expression \(regex\) used to validate user inputs. The applicable regex for each IP address format overrides this property if the type is set to **ipv4** or **ipv6**.

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
</table><table id="table_g1c_wd1_zcc"><thead><tr><th>

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

Enable the Landmark Focus keyboard shortcut to focus on this input.

</td></tr></tbody>
</table>## Input component events

Select event handlers to configure the actions \(events\) provided with the Input component.

The Events tab shows the events used by the Input component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Input actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_kpd_clb_ynb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input invalid set

</td><td>

The user moves focus away from the field and the value is invalid.Payload:

-   `name`: String. Value of the **name** property.
-   `value`: Boolean. Value of the **invalid** property, which is based on the values of the **required** and **pattern** properties.
-   `fieldValue`: String. Value entered in the field.
-   `type`: String. Value of the **type** property.

</td></tr><tr><td>

Input value set

</td><td>

The user moves focus away from the field and the value is valid.Payload:

-   `name`: String. Value of the **name** property.
-   `value`: String. Value entered in the field.

</td></tr><tr><td>

Text entered

</td><td>

The user types or pastes text in the field. The system doesn't validate the value or update the **value** property.Payload:

-   `name`: String. Value of the **name** property.
-   `data`: String. Value entered in the field that triggered the event.
-   `fieldValue`: String. Current value of the field when the event was triggered.

</td></tr><tr><td>

Input enter keydown

</td><td>

The user selects the **Enter** key when focus is inside the input field.

</td></tr><tr><td>

Input selection changed

</td><td>

The user selects or deselects text within the input, either by clicking, tapping, or using the keyboard.Payload:

-   `name`: String. Value of the **name** property.
-   `selection`: String. The selected text within the input field.
-   `selectionStart`: Number. The index of the first selected character within the input field.
-   `selectionEnd`: Number. The index of the character immediately after the selection within the input field.
-   `fieldValue`: String. The current value of the field when the event was triggered.
-   `fieldElement`: JSON. The field element as an object, containing additional metadata about the input field.

</td></tr></tbody>
</table>