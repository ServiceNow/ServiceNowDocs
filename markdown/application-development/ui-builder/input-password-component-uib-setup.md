---
title: Input Password component setup
description: Use the Input Password component to give users a way to create accounts or log in when authentication is required.Define the value, text, and alert messages of your Input Password component with these properties.Select event handlers to configure the actions \(events\) provided with the Input Password component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/input-password-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Input Password component setup

Use the Input Password component to give users a way to create accounts or log in when authentication is required.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Input Password that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "input-password-content-tree.png"\] Alt text: Image showing Input Password content tree

2.  Select the Input Password component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Input Password label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Input Password component properties

Define the value, text, and alert messages of your Input Password component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_vjc_3yd_qnb"><thead><tr><th>

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

When enabled, user cannot interact with the field and cannot change its value. The field appears grayed out when disabled.

</td></tr><tr><td>

Read-only\[readonly\]

</td><td>

When enabled, user cannot modify the value of the input field. The input field is not disabled in this setting.

</td></tr><tr><td>

Auto focus\[autofocus\]

</td><td>

Indicate that focus is automatically placed inside the input field when the page loads.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **"layout":"horizontal"**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **"layout":"vertical"** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr></tbody>
</table><table id="table_wcx_dqb_4fc"><thead><tr><th>

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

If set to **true**, overrides automatic updates to the **Value** property. Use the **Input password value set** event to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Identifier\[name\]

</td><td>

Reference name for the input field dispatched with the field value when the user interacts with the field.

</td></tr><tr><td>

Placeholder text\[placeholder\]

</td><td>

Hint text displayed in the input field before the user has entered a value.

</td></tr><tr><td>

Disable show password option\[disableUnmask\]

</td><td>

Disable the user's ability to view the password value in plain text using a **Mask/Unmask** button.

</td></tr><tr><td>

Text align\[align\]

</td><td>

Alignment of the text within the input field.

</td></tr></tbody>
</table><table id="table_hhl_lqb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requirements\[requirements\]

</td><td>

Array of requirements for the user-entered password. Each requirement contains a label describing the requirement and the RegEx pattern against which the password must validate.Default:

```

{
    "name": "label",
    "label": "Label",
    "fieldType": "string",
    "translatable": true
},
{
    "name": "pattern",
    "label": "Pattern",
    "fieldType": "string"
}

```

</td></tr><tr><td>

Place password requirements in icon\[compact\]

</td><td>

Displays password requirements in the input field popover instead of below the input field. Validation errors for passwords that fail to meet requirements appear below the input field.

</td></tr></tbody>
</table><table id="table_kbb_rqb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Text of the label.

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

</td></tr></tbody>
</table><table id="table_ld5_vqb_4fc"><thead><tr><th>

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

If set to **true**, overrides automatic updates to the **Invalid** property. Use the **Input password invalid set** event to intercept the requested change and handle it manually.Default: **false**

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
</table><table id="table_nyj_qrb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ARIA properties\[configAria\]

</td><td>

A JSON field for configuring ARIA properties, such as **aria-braillelabel**.

</td></tr></tbody>
</table>## Input Password component events

Select event handlers to configure the actions \(events\) provided with the Input Password component.

The Events tab shows the events used by the Input Password component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Input Password actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_vpr_jyd_qnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input password invalid set

</td><td>

Dispatched when the user moves focus away from the field and the value is invalid.Payload:

-   `name`: String. Value of the **name** property.
-   `value`: Boolean. Value of the **invalid** property, which is based on the values of the **required** and **pattern** properties.
-   `fieldValue`: String. Value entered in the field.

</td></tr><tr><td>

Input password value set

</td><td>

Dispatched when the user moves focus away from the field and the value is valid.Payload:

-   `name`: String. Value of the **name** property.
-   `value`: String. Value entered in the field.

</td></tr><tr><td>

Input password input

</td><td>

Dispatched when the user enters data in the field by typing or pasting text. The system does not validate the value or update the **value** property.Payload:

-   `name`: String. Value of the **name** property.
-   `data`: String. Value entered in the field that caused the event to fire.
-   `fieldValue`: String. Current value of the field when the event fired.

</td></tr></tbody>
</table>