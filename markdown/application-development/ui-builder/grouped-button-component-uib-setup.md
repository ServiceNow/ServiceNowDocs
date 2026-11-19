---
title: Grouped button component setup
description: Configure the properties for the grouped button component.Select event handlers to configure the events provided with the Grouped button component. Event handlers work with data resources to link the Grouped button actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/grouped-button-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Grouped button component setup

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Grouped button that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Grouped button component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "grouped-button-content-tree.png"\] Alt text: Grouped button in the content tree


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Grouped button component properties

Configure the properties for the grouped button component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_grouped_button_props"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select\[select\]

</td><td>

Determines the selection mode. Options are **Single** \(default\) or **Multi**.

</td></tr><tr><td>

Button options\[items\]

</td><td>

An array of objects, each defining the configuration for a button.```
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
  "icon": {
    "type": "string"
  },
  "disabled": {
    "type": "boolean"
  },
  "tooltipContent": {
    "type": "string"
  }
}
```

</td></tr><tr><td>

Variant\[variant\]

</td><td>

Sets the color and style of the buttons. Options include:-   **Primary**
-   **Secondary** \(default\)
-   **Tertiary**
-   **Primary \(selection\)**
-   **Secondary \(selection\)**
-   **Tertiary \(selection\)**

</td></tr><tr><td>

Size\[size\]

</td><td>

Sets the size of the buttons. Options include:-   **Small**
-   **Medium** \(default\)
-   **Large**

</td></tr><tr><td>

Hide button labels\[hideButtonLabel\]

</td><td>

When true, hides labels for buttons that have an icon.Default: **False**

</td></tr><tr><td>

Hide container\[bare\]

</td><td>

When true, removes the border around the button group container.Default: **False**

</td></tr><tr><td>

Button fixed width\[fixedWidth\]

</td><td>

When true, all buttons share the same width based on the longest button label.Default: **True**

</td></tr><tr><td>

Selected buttons\[selectedItems\]

</td><td>

An array of IDs representing the currently selected buttons.

</td></tr><tr><td>

Manage selected items\[manageSelectedItems\]

</td><td>

Overrides automatic updates to the **Selected buttons** property. Use the **Selected items changed** event to intercept the requested change and handle it manually.

</td></tr><tr><td>

Button min width\[minWidth\]

</td><td>

Sets a custom minimum width for each button. Value must include units. When this property is empty, the component applies a default minimum width.

</td></tr><tr><td>

Group label\[label\]

</td><td>

Sets the label text for the button group.

</td></tr><tr><td>

Label position\[labelPosition\]

</td><td>

Sets the position of the label relative to the button group. Options are **Top** \(default\) or **Start**.

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

Configures ARIA attributes for the button group container.

</td></tr><tr><td>

High contrast\[highContrast\]

</td><td>

When true, increases contrast for buttons displayed on a colored background.

</td></tr></tbody>
</table>## Grouped button component events

Select event handlers to configure the events provided with the Grouped button component. Event handlers work with data resources to link the Grouped button actions to the data you want to display to your users.

The Events tab shows the events used by the Grouped button component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Grouped button actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_grouped_button_events"><thead><tr><th>

Label \[event\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Button clicked or selected\[NOW\_GROUPED\_BUTTON\#ITEM\_CLICKED\]

</td><td>

Dispatched when a button is clicked or selected.

</td></tr><tr><td>

Selected items changed\[NOW\_GROUPED\_BUTTON\#SELECTED\_ITEMS\_SET\]

</td><td>

Dispatched when the user changes the selected items.

</td></tr></tbody>
</table>