---
title: Radio buttons component setup
description: The Radio buttons component is a selectable input that lets the user choose a single option in a predefined set of mutually exclusive options.Configure the appearance and features of the Radio buttons component.Select event handlers to configure the actions \(events\) provided with the Radio buttons component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/radio-buttons-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Radio buttons component setup

The Radio buttons component is a selectable input that lets the user choose a single option in a predefined set of mutually exclusive options.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your radio button that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "radio-buttons-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Radio buttons component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Radio buttons label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Radio buttons component properties

Configure the appearance and features of the Radio buttons component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_njc_j3c_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Button size. Either **small** or **medium**.Default: **Medium**

</td></tr><tr><td>

Layout\[layout\]

</td><td>

Orientation of radio buttons options. Choices are **vertical** or **horizontal**.Default: **Vertical**

</td></tr><tr><td>

Options\[options\]

</td><td>

Array of objects that define the options displayed by the component.Default:

```

{
  "id": {
    "type": [
      "string",
      "number"
    ]
  },
  "label": {
    "type": "string",
    "translatable": true
  },
  "checked": {
    "type": "boolean"
  },
  "readonly": {
    "type": "boolean"
  },
  "disabled": {
    "type": "boolean"
  }
}

```

</td></tr><tr><td>

Selected option\[value\]

</td><td>

The ID of the option selected by the user, or the first option passed in that has **checked** set to **true**.Default: **one**

</td></tr><tr><td>

Manage value\[manageValue\]

</td><td>

If set to **true**, overrides automatic updates to the **Value** property. Use the **Radio buttons value set** to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Identifier\[identifier\]

</td><td>

Name of the component control. Dispatched along with the value on user interaction.Default: **radio**

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Option to mute the button color and prevent user interactions.

</td></tr><tr><td>

Read-only\[readonly\]

</td><td>

Option to prevent users from modifying the component value.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **"layout":"horizontal"**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **"layout":"vertical"** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr></tbody>
</table><table id="table_gdd_tjc_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Text describing the purpose of the radio button options to the user. The text displays above the radio button options.

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

</td></tr></tbody>
</table><table id="table_rb2_hkc_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

Option to visually indicate that the component is in an incorrect state. Use this for forms that validate input to guide users to correct invalid component values.

</td></tr><tr><td>

Manage invalid\[manageInvalid\]

</td><td>

If set to **true**, overrides automatic updates to the **Invalid** property. Use the **Radio buttons invalid set** to intercept the requested change and handle it manually.Default: **false**

</td></tr><tr><td>

Alert messages\[messages\]

</td><td>

Array of inline alert messages that display below the component. The following list describes each object's properties:-   `content`: The text of the alert message.
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
</table>## Radio buttons component events

Select event handlers to configure the actions \(events\) provided with the Radio buttons component.

The Events tab shows the events used by the Radio buttons component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Radio buttons actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Radio buttons value set|Dispatched when the user interacts with a radio button in the group.|
|Radio buttons invalid set|Dispatched when the **Invalid** property should be updated.|

