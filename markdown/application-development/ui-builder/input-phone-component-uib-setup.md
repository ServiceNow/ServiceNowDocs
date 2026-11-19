---
title: Input Phone component setup
description: The Input Phone component is a form element input for telephone numbers with country code and computer telephony integration \(CTI\).Display a phone number that the user can call by selecting the iconic button​. You can also display a drop-down list of country codes to select, and a blank field allowing the user to input a phone number.Select event handlers to configure the actions \(events\) provided with the Input Phone component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/input-phone-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Input Phone component setup

The Input Phone component is a form element input for telephone numbers with country code and computer telephony integration \(CTI\).

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Input Phone that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "input-phone-content-tree.png"\] Alt text: Input phone content tree

2.  Select the Input Phone component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Input Phone label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

3.  Enter either static or dynamic input in the input fields.

    -   Enter static values by typing in the content or selecting it from a drop-down list.
    -   Enter dynamic input by selecting the appropriate button:
        -   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
        -   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).
4.  Select the **Events** tab in the setup panel on the right and configure event handlers for the actions provided for the Input Phone component.

    For more information about event handlers, see [event handlers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Input phone component properties

Display a phone number that the user can call by selecting the iconic button​. You can also display a drop-down list of country codes to select, and a blank field allowing the user to input a phone number.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_tsf_g3n_ynb"><thead><tr><th>

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

When enabled, the user cannot modify the value of the input field. However, the input field is not in a disabled state when this field evaluates to **True**.

</td></tr><tr><td>

Auto focus\[autofocus\]

</td><td>

Indicates that focus is automatically placed inside the input field when the page loads.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **"layout":"horizontal"**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **"layout":"vertical"** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr></tbody>
</table><table id="table_kyj_ztb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value\[value\]

</td><td>

Sets a value for the input field, including the country code and the numeric string. Unless the input field has pre-populated data, this property should be left empty.

</td></tr><tr><td>

Manage value\[manageValue\]

</td><td>

If set to **true**, overrides automatic updates to the **Value** property. Use the **Input phone value set** event to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Number\[number\]

</td><td>

Phone number \(excluding the country code\) in the main input area of the phone input field.

</td></tr><tr><td>

Identifier\[name\]

</td><td>

Reference name for the input field dispatched with the field value when the user interacts with the field.

</td></tr><tr><td>

Placeholder text\[placeholder\]

</td><td>

Hint text displayed in the input field before the user has entered a value. Text should hint to the user what input is expected.

</td></tr><tr><td>

Min characters\[minlength\]

</td><td>

​Sets a minimum number of characters required for the input field.

</td></tr><tr><td>

Max characters\[maxlength\]

</td><td>

​Sets a maximum number of characters required for the input field.

</td></tr><tr><td>

Text align\[align\]

</td><td>

Alignment of the text within the input field.

</td></tr></tbody>
</table><table id="table_ht1_35b_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Country codes\[countryCodes\]

 ​

</td><td>

Array of country codes to display in the drop-down list inside the field.

</td></tr><tr><td>

Selected country code\[selectedCountryCode\]

</td><td>

​"Code" value matching an object from the **countryCodes** array that is selected in the country code drop-down menu.

</td></tr></tbody>
</table><table id="table_xxt_k5b_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Label that tells users the value that should be entered in the input field.

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

When true, the required indicator is visually hidden. Use for forms where most fields are required, along with the "optional" flag for any fields that are not required

</td></tr><tr><td>

Optional\[optional\]

</td><td>

Indicates that the user doesn't have to enter a value in the input field before proceeding.

</td></tr><tr><td>

Helper text\[helperContent\]

</td><td>

Defines the hover text that displays additional help for a field. When this value is specified, ​an iconic button appears next to the field label for displaying hints for the user, such as password requirements or other instructions for completing the field. Use plain text to allow the text to be translatable. If you don't want to add helper content, leave this property empty.

</td></tr></tbody>
</table><table id="table_vmp_q5b_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

When enabled, the field appears as visually invalid, indicating incorrect input.

</td></tr><tr><td>

Manage invalid\[manageInvalid\]

</td><td>

If set to **true**, overrides automatic updates to the **Invalid** property. Use the **Input phone invalid set** event to intercept the requested change and handle it manually.Default: **false**

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
</table><table id="table_zdx_w5b_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ARIA properties\[configAria\]

</td><td>

A JSON field for configuring ARIA properties, such as **aria-braillelabel**.

</td></tr></tbody>
</table>## Input phone component events

Select event handlers to configure the actions \(events\) provided with the Input Phone component.

The Events tab shows the events used by the Input Phone component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Input Phone events to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_gn4_mg4_ynb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input phone invalid set

</td><td>

The user moves focus away from the input field.Payload contains:

-   **name**: Value of the `name` property
-   **value**: Value of the `invalid` property, which is based on the values of the `required` and `pattern` properties
-   **fieldValue**: Value entered in the input field

</td></tr><tr><td>

Input phone value set

</td><td>

The user selects a country code from the dropdown or updates the main phone number input value. You can set the `manage-value` property to override the default behavior and handle this action manually. The payload contains the concatenation of the country code and the phone number.

</td></tr><tr><td>

Input phone input

</td><td>

The user enters data in the field by typing or pasting text. The system does not validate the value or update the `value` property.Payload contains:

-   **name**: Value of the `name` property
-   **data**: Value entered in the field that caused the event to fire
-   **fieldValue**: Current value of the field when the event fired

</td></tr><tr><td>

Input phone button clicked

</td><td>

The user clicks the CTI \(phone\) button.

</td></tr><tr><td>

Input phone country code set

</td><td>

The user selects a country code from the dropdown. The payload contains the `code` value from the corresponding configuration object in the `countryCodes` array.

</td></tr></tbody>
</table>