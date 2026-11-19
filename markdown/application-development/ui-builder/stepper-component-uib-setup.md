---
title: Stepper component setup
description: The Stepper is a tabular navigation that enables users to progress through a process, view their current location, and move to other steps.Configure the items that appear in the Stepper with these properties.Select event handlers to configure the actions \(events\) provided with the Stepper component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/stepper-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Stepper component setup

The Stepper is a tabular navigation that enables users to progress through a process, view their current location, and move to other steps.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Stepper that differentiates it from other components in the [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "stepper-content-tree.png"\] Alt text: Stepper component with label displayed in the content tree.

2.  Select the Stepper component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Stepper label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Stepper component properties

Configure the items that appear in the Stepper with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_xnm_jrl_znb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Items\[items\]

</td><td>

Array of objects describing the steps in the stepper.```
{
  "label": {
    "type": "string",
    "translatable": true
  },
  "id": {
    "type": [
      "string",
      "number"
    ]
  },
  "icon": {
    "type": "string"
  },
  "sublabel": {
    "type": "string",
    "translatable": true
  },
  "progress": {
    "type": "string",
    "enum": [
      "none",
      "partial",
      "done"
    ]
  },
  "disabled": {
    "type": "boolean"
  }
}
```

</td></tr><tr><td>

Selected item\[selectedItem\]

</td><td>

ID of the current step.

</td></tr><tr><td>

Manage selected item\[manageSelectedItem\]

</td><td>

Overrides automatic updates to the selected item property. Use the **Selected item set** event to intercept the requested change and handle it manually.

</td></tr><tr><td>

Hide numbers\[hideNumbers\]

</td><td>

Hides the numbers on each step in the stepper.

</td></tr><tr><td>

Show completed count\[showCompletedCount\]

</td><td>

Displays a count under the stepper that shows the number of completed steps and the number of total steps.

</td></tr><tr><td>

Read only\[readonly\]

</td><td>

Renders stepper in a presentation mode, removing all interactivity except for pagination.

</td></tr><tr><td>

Page to selected item\[pageToSelectedItem\]

</td><td>

Navigates to the page assigned to **selectedItem**.

</td></tr><tr><td>

Size\[size\]

</td><td>

Sets the stepper size. Options are **small** or **medium**.

</td></tr><tr><td>

Label position\[labelPosition\]

</td><td>

Position of the stepper label. Options are **top**, **bottom**, or **right**.

</td></tr></tbody>
</table>## Stepper component events

Select event handlers to configure the actions \(events\) provided with the Stepper component.

The Events tab shows the events used by the Stepper component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Stepper actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Stepper selected item set|Dispatched when a step is selected.|
|Stepper next page button clicked|Dispatched when the stepper is paginated and the user clicks the "next page" button to see additional steps that are not visible in the current view.|
|Stepper previous page button clicked|Dispatched when the stepper is paginated and the user clicks the "previous page" button to see previous steps that are not visible in the current view.|

