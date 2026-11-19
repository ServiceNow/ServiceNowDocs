---
title: Color selector component setup
description: Color selector is a color library that can be used to search for, select, and save colors.Configure the tabs, buttons, borders, and color options for Color selector with these properties.Select event handlers to configure the actions \(events\) provided with the Color selector component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/color-selector-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Color selector component setup

Color selector is a color library that can be used to search for, select, and save colors.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Color selector that differentiates it from other components in the content tree.

    A label makes finding the Color selector easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "color-selector-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Color selector component, using one of these methods:

    -   Hexcodes, RGB, and HSL values are accepted, and custom colors can be used.

        Click anywhere within the component.

    -   Select the Color selector label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Color selector component properties

Configure the tabs, buttons, borders, and color options for Color selector with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_akw_x5g_f4b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger type\[triggerType\]

</td><td>

Type of trigger for the color selector. **Button trigger** and **Select trigger** are supported.

</td></tr><tr><td>

Show label\[showLabel\]

</td><td>

Displays label below the color picker swatch.

</td></tr><tr><td>

Include tabs\[selectors\]

</td><td>

Array of tab names. Tabs display in the order they are declared inside the array.```
[
  {
    "name": "type",
    "label": "Type",
    "fieldType": "choice",
    "mandatory": true,
    "typeMetadata": {
      "choices": [
        {
          "label": "Picker",
          "value": "picker"
        },
        {
          "label": "Palette",
          "value": "palette"
        }
      ]
    }
  },
  {
    "name": "label",
    "label": "Label",
    "fieldType": "string",
    "mandatory": false
  }
]
```

</td></tr><tr><td>

Initial color\[initialColor\]

</td><td>

Type and value of the selected color. HEX, RGB, HSL and ID are supported.

</td></tr><tr><td>

Include buttons\[footerActions\]

</td><td>

Array of objects that defines the buttons in the color selector panel footer.

</td></tr><tr><td>

Color name\[colorName\]

</td><td>

String to define color names.

</td></tr><tr><td>

Color name editable\[colorNameEditable\]

</td><td>

Enables users to edit color names.

</td></tr><tr><td>

Helper content\[helperContent\]

</td><td>

Iconic button next to the color name label. When selected, it opens a popover to display additional information about the color name.

</td></tr><tr><td>

Panel fit props\[panelFitProps\]

</td><td>

Position of the color selector panel.

</td></tr><tr><td>

Color groups\[colorGroups\]

</td><td>

Array of color objects to show in the **My Colors** tab.

</td></tr><tr><td>

Show accessible color selector\[showAccessibleColorSelector\]

</td><td>

Enables accessibility options for the color selector.

</td></tr><tr><td>

Contrast check type\[contrastCheckType\]

</td><td>

Enables accessible contrast options.

</td></tr><tr><td>

Comparison color\[comparisonColor\]

</td><td>

Displays comparison colors.

</td></tr></tbody>
</table>## Color selector component events

Select event handlers to configure the actions \(events\) provided with the Color selector component.

The Events tab shows the events used by the Color selector component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Color selector actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_xrp_z5g_f4b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Color selector color name set\[NOW\_COLOR\_SELECTOR\#COLOR\_NAME\_SET\]

</td><td>

Dispatched when the user edits the color name.

</td></tr><tr><td>

Color selector footer action clicked\[NOW\_COLOR\_SELECTOR\#FOOTER\_ACTION\_CLICKED\]

</td><td>

Dispatches when the user selects any footer action. Payload contains the footer action, selected color string in HEX format, and the color name.

</td></tr></tbody>
</table>