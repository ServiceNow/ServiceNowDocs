---
title: Input URL component setup
description: The Input URL component accepts hyperlinks as input for entering and editing web addresses.Define the value, text, and alert messages of your Input URL component with these properties.Select event handlers to configure the actions \(events\) provided with the Input URL component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/input-url-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Input URL component setup

The Input URL component accepts hyperlinks as input for entering and editing web addresses.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Input URL that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "input-url-content-tree.png"\] Alt text: Image showing Input URL component content tree

2.  Select the Input URL component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Input URL label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Input URL component properties

Define the value, text, and alert messages of your Input URL component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_llt_tfl_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Size of the component in either **small** or **medium**.Default: **Medium**

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Property that prevents the user from interacting with the field or changing its value. The field appears grayed out.

</td></tr><tr><td>

Read-only\[readonly\]

</td><td>

Prevents the user from modifying value in the field. The input field is not in a disabled state with this setting.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **"layout":"horizontal"**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **"layout":"vertical"** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr></tbody>
</table><table id="table_xtg_jvb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value\[value\]

</td><td>

Value of the input field. Unless the input field has pre-populated data, leave this property empty.

</td></tr><tr><td>

Manage value\[manageValue\]

</td><td>

If set to **true**, overrides automatic updates to the **Value** property. Use the **Input url value set** event to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Identifier\[name\]

</td><td>

Reference name for the input field dispatched with the field value when the user interacts with the field.

</td></tr><tr><td>

Placeholder text\[placeholder\]

</td><td>

Hint text displayed in the input field before the user has entered a value.

</td></tr><tr><td>

Min characters\[minlength\]

</td><td>

Minimum number of characters allowed for the input field.

</td></tr><tr><td>

Max characters\[maxlength\]

</td><td>

Maximum number of characters allowed for the input field.

</td></tr><tr><td>

Text align\[align\]

</td><td>

Alignment of the text within the input field.

</td></tr></tbody>
</table><table id="table_byz_rvb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Text in the label.

</td></tr><tr><td>

Wrap label\[wrapLabel\]

</td><td>

If the label doesn't fit on one line, wraps the label.

</td></tr><tr><td>

Required\[required\]

</td><td>

Indicates that the user must enter a value in the input field before submitting the form.

</td></tr><tr><td>

Hide required indicator\[hideRequiredIndicator\]

</td><td>

Hides the required field indicator. Use this for forms in which most fields are required, together with the **Optional** flag for any fields that aren't required.

</td></tr><tr><td>

Optional\[optional\]

</td><td>

Adds a visual indicator marking a field that the user doesn't have to complete before submitting the form.

</td></tr><tr><td>

Helper content\[helperContent\]

</td><td>

Displays an iconic button with a popover next to the field label that displays additional hint text to the user. An example is URL requirements or other instructions for completing the field.

</td></tr></tbody>
</table><table id="table_vd3_cwb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

Visually marks a field containing an invalid value.

</td></tr><tr><td>

Manage invalid\[manageInvalid\]

</td><td>

If set to **true**, overrides automatic updates to the **Invalid** property. Use the **Input url invalid set** event to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Validation pattern\[pattern\]

</td><td>

​Provides a regular expression for evaluating user input.

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
</table><table id="table_yhj_jwb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ARIA properties\[configAria\]

</td><td>

A JSON field for configuring ARIA properties, such as **aria-braillelabel**.

</td></tr></tbody>
</table>## Input URL component events

Select event handlers to configure the actions \(events\) provided with the Input URL component.

The Events tab shows the events used by the Input URL component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Input URL events to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_br2_yfl_qnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input url invalid set

</td><td>

Dispatched when the user moves focus away from the field and the URL is invalidPayload:

-   `name`: String. Value of the **name** property.
-   `value`: Boolean. Value of the **invalid** property, which is based on the values of the **required** and **pattern** properties.
-   `fieldValue`: String. Value entered in the field.

</td></tr><tr><td>

Input url value set

</td><td>

Dispatched when the user moves focus away from the field and the URL is validPayload:

-   `name`: String. Value of the **name** property.
-   `value`: String. Value entered in the field.

</td></tr><tr><td>

Input url input

</td><td>

Dispatched when the user enters data in the field by typing or pasting text. The system does not validate the value or update the **value** property.Payload:

-   `name`: String. Value of the **name** property.
-   `data`: String. Value entered in the field that caused the event to fire.
-   `fieldValue`: String. Current value of the field when the event fired.

</td></tr></tbody>
</table>