---
title: Textarea component setup
description: The Textarea component is an input that lets the user enter multiple lines of text. The Textarea component offers design elements to configure the input area and the display of text.Configure the appearance and features of the Textarea component.Select event handlers to configure the actions \(events\) provided with the Textarea component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/textarea-component-uib-setup-2.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Textarea component setup

The Textarea component is an input that lets the user enter multiple lines of text. The Textarea component offers design elements to configure the input area and the display of text.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Textarea that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "textarea-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Textarea component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Textarea label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Textarea component properties

Configure the appearance and features of the Textarea component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_tmk_4g4_jvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Size of the text area. The choices are:-   **small**
-   **medium** \(default\)

 The **small** size reduces the size of text in the component.

</td></tr><tr><td>

Color\[color\]

</td><td>

Sets the text field background color. The choices are:-   **Initial** \(no color\)
-   **Blue**
-   **Yellow**
-   **Green**

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Disables the field to prevent user interactions. The textarea is grayed out.

</td></tr><tr><td>

Read-only\[readonly\]

</td><td>

Prevents users from modifying the component value. The textarea is enabled, but not editable.

</td></tr><tr><td>

Auto-focus\[autofocus\]

</td><td>

Places focus inside the component when the page loads.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **horizontal**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **vertical** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr></tbody>
</table><table id="table_uc1_l34_jvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value\[value\]

</td><td>

Value of the textarea field.

</td></tr><tr><td>

Identifier\[name\]

</td><td>

Name of the component control. Dispatched along with the value on user interaction.

</td></tr><tr><td>

Placeholder text\[placeholder\]

</td><td>

Text that gives the user a hint as to what input is expected.

</td></tr><tr><td>

Min. characters\[minLength\]

</td><td>

Minimum number of characters that the user can enter in the text field.

</td></tr><tr><td>

Max. characters\[maxLength\]

</td><td>

Maximum number of characters that the user can enter in the text field.

</td></tr><tr><td>

Show character counter\[showCounter\]

</td><td>

When true, displays a character counter underneath the textarea to show the user the number of remaining characters, based on the value of the **maxlength** property. When this property is set and character entry exceeds the **maxlength** value, the counter goes below 0 and the field is invalid.

</td></tr><tr><td>

Enable caret slot\[enableCaretSlot\]

</td><td>

When **true**, a slot will be added to the component that follows the user's text cursor.

</td></tr></tbody>
</table><table id="table_ybq_5k4_jvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Text describing the purpose of the component to the user.Default: **Textarea**

</td></tr><tr><td>

Wrap label\[wrapLabel\]

</td><td>

If the label doesn't fit on one line, wraps the label.

</td></tr><tr><td>

Required\[required\]

</td><td>

Requires users to enter a component value before they can complete the form.

</td></tr><tr><td>

Hide required indicator\[hideRequiredIndicator\]

</td><td>

Shows or hides the required indicator for the component. Use this for forms where most components are required, along with the **Optional** property to highlight the components that are not required.

</td></tr><tr><td>

Optional\[optional\]

</td><td>

When **true**, the field is optional and does not need to be completed by the user before completing the form.

</td></tr><tr><td>

Helper text\[helperContent\]

</td><td>

Instructions to guide user interaction with the component such as password requirements. When defined, an iconic button with a popover appears next to the field label to display the text. Use plain text to allow the text to be translatable.

</td></tr></tbody>
</table><table id="table_o3f_sm4_jvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resize\[resize\]

</td><td>

Determines whether the component can be resized and in which direction. The choices are:-   **Both**
-   **Horizontal**
-   **None**
-   **Vertical**

Default: **Vertical**

</td></tr><tr><td>

Height rows\[rows\]

</td><td>

Height of the text area, in characters.

</td></tr><tr><td>

Width columns\[cols\]

</td><td>

Width of the text area, in characters.

</td></tr><tr><td>

Auto-resize\[autoreresize\]

</td><td>

Increases the height of the component as the user adds input.

</td></tr><tr><td>

Disable min height\[disableMinHeight\]

</td><td>

Disables the minimum height of 64 pixels allowed for the component.

</td></tr><tr><td>

Disable max height\[disableMaxHeight\]

</td><td>

Disables the maximum height of 256 pixels allowed for the component.

</td></tr><tr><td>

Autoresize rows limit\[autoresizeRowsLimit\]

</td><td>

Maximum number of rows to allow when the **autoresize** property is set to **true**.

</td></tr></tbody>
</table><table id="table_fj3_yn4_jvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

Visually indicates that the component is in an incorrect state. Use this for forms that validate input to guide users to correct invalid component values.Default: **false**

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
</table><table id="table_h1g_344_jvb"><thead><tr><th>

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

Enable the Landmark Focus keyboard shortcut to focus on this textarea.

</td></tr></tbody>
</table>## Textarea component events

Select event handlers to configure the actions \(events\) provided with the Textarea component.

The Events tab shows the events used by the Textarea component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Textarea actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_hnp_bvz_xnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Text entered

</td><td>

Dispatched when the user types or pastes text in the textarea. Internal validation is not performed, and the actual **Value** property is not updated at this point.Payload:

-   **name**: Name of the field.
-   **data**: Data of the native input event \(usually a typed character\).
-   **fieldValue**: Current value of the field.
-   **fieldElement**: Native textarea HTMLElement.

</td></tr><tr><td>

Textarea invalid set

</td><td>

Dispatched when focus is moved out of the field, and the field contains an invalid value. Validation is based on the setting of the **required** and **maxlength** properties.Payload:

-   **name**: Name of the field
-   **value**: Value of the invalid property
-   **fieldValue**: Content of the text area.

</td></tr><tr><td>

Focus moved

</td><td>

Dispatched when the user moves focus from the textarea and the field contains a valid value.Payload:

-   **name**: Name of the field
-   **value**: Value of the updated value

</td></tr><tr><td>

Textarea selection changed

</td><td>

The user selects or deselects text within the textarea, either by clicking, tapping, or using the keyboard.Payload:

-   `name`: String. Value of the **name** property.
-   `selection`: String. The selected text within the textarea field.
-   `selectionStart`: Number. The index of the first selected character within the textarea field.
-   `selectionEnd`: Number. The index of the character immediately after the selection within the textarea field.
-   `fieldValue`: String. The current value of the field when the event was triggered.
-   `fieldElement`: JSON. The field element as an object, containing additional metadata about the textarea field.

</td></tr></tbody>
</table>