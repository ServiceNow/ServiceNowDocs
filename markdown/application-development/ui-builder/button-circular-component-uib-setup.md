---
title: Button circular component setup
description: A circular button is an actionable icon in a circular format, used to provide a high-visibility, top-level action on a page. This button acts as a trigger for a modal, modeless-dialog, or popover.Configure the appearance and tooltip text for your Button circular.Select event handlers to configure the actions \(events\) provided with the Button circular component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/button-circular-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Button circular component setup

A circular button is an actionable icon in a circular format, used to provide a high-visibility, top-level action on a page. This button acts as a trigger for a modal, modeless-dialog, or popover.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Button circular that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "button-circular-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Button circular component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the button circular label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Button Circular component properties

Configure the appearance and tooltip text for your Button circular.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_n23_dnf_dgc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Icon\[icon\]

</td><td>

Icon to display inside the button.

</td></tr><tr><td>

Variant\[variant\]

</td><td>

Color and behavior of the button.

</td></tr><tr><td>

Bare\[bare\]

</td><td>

Removes the border and sets the default background to be transparent.

</td></tr><tr><td>

Size\[size\]

</td><td>

Size of the button.Default: **medium**

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Option to disable the component. When this property is set to true, the button color is muted and user interaction is unavailable.Default: **false**

</td></tr><tr><td>

Animated icon\[animatedIcon\]

</td><td>

Animated icon to display inside the button.

</td></tr><tr><td>

Tooltip text\[tooltipContent\]

</td><td>

Text that is displayed when hovering either of the buttons.

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

An object whose keys reference a specific HTML element within the dropdown. The value of each key is an object that contains an ARIA property and corresponding value. These ARIA properties are set on the specified element.

</td></tr></tbody>
</table>## Button Circular component events

Select event handlers to configure the actions \(events\) provided with the Button circular component.

The Events tab shows the events used by the Button circular component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Button circular actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Button circular clicked|User clicks the Button circular component.|

