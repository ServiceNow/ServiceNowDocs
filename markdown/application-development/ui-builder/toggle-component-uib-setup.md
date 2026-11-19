---
title: Toggle component setup
description: The Toggle component turns a setting on and off.Configure the appearance and features of the Toggle component.Select event handlers to configure the actions \(events\) provided with the Toggle component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/toggle-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Toggle component setup

The Toggle component turns a setting on and off.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Toggle component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "toggle-content-tree.png"\] Alt text: Toggle content tree.

2.  Select the Toggle component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the toggle label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

    \[Omitted image "toggle-config-panel.png"\] Alt text: Shows the properties for the toggle component in config tab


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Toggle component properties

Configure the appearance and features of the Toggle component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_izp_x2h_f4b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Size of the toggle. The possible choices are:-   Small
-   Medium \(default\)

</td></tr><tr><td>

Checked\[checked\]

</td><td>

Indicates the checked state **on default**. If true, when the page is first opened, the user sees the toggle as `checked` or "on."Default: **false**

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Option to disable the toggle. Selecting this option grays out the toggle and prevents users from interacting with it.Default: **false**

</td></tr><tr><td>

Label\[label\]

</td><td>

Label to display for the toggle component.

</td></tr><tr><td>

Label position\[labelPosition\]

</td><td>

Location of the label relative to the toggle. The possible choices are:-   Start \(default\)
-   End
-   Top
-   Bottom

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Indicates whether the layout will be vertical \(stacked view\) or horizontal \(inline view\). In a horizontal layout, a typical component has three containers: **label**, **formfield**, and **slottted** content. If the layout is horizontal, the component uses the columns array to set the width of the grid template columns for these containers.Default: **\{"layout":"vertical"\}**

</td></tr><tr><td>

ARIA properties\[configAria

</td><td>

An object whose keys reference a specific HTML element within the component. The value of each key is an object that contains ARIA properties and corresponding values.

</td></tr></tbody>
</table>## Toggle component events

Select event handlers to configure the actions \(events\) provided with the Toggle component.

The Events tab shows the events used by the Toggle component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

\[Omitted image "toggle-events.png"\] Alt text: Shows the available events for the toggle component

### Event handlers

Event handlers work with data resources to link the Toggle actions to the data you want to display to your users. Expand the event in the list and add one or more event handlers. For information about event handlers, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md)

### Event descriptions

|Event|Description|
|-----|-----------|
|Toggle checked set|Dispatched when the checked state of the toggle changes. The payload contains the value **true** when the toggle is selected and **false** when it's unselected.|

