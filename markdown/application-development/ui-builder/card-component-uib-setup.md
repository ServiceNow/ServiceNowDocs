---
title: Card Base Container component setup
description: A Card Base Container component organizes specific information in a simple, easily scannable format. Use a Card Base Container to help the user make a decision or quickly view information. The component provides a border, card-level interactivity, and a default slot for holding card subcomponents.Configure the appearance and interactions of your Card Base Container with these properties.Select event handlers to configure the actions \(events\) provided with the Card Base Container component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/card-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Card Base Container component setup

A Card Base Container component organizes specific information in a simple, easily scannable format. Use a Card Base Container to help the user make a decision or quickly view information. The component provides a border, card-level interactivity, and a default slot for holding card subcomponents.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Card Base Container that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [UI Builder tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-tutorial.md).

    \[Omitted image "card-content-tree.png"\] Alt text: Page content tree containing a Card Base Container and showing its default slot.

2.  Select the Card Base Container component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Card Base Container label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

3.  Enter either static or dynamic input in the input fields.

    -   Enter static values by typing in the content or selecting it from a drop-down list.
    -   Enter dynamic input by selecting the appropriate button:
        -   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
        -   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Card Base Container component properties

Configure the appearance and interactions of your Card Base Container with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

**Note:** \(Optional\) Add any of the following subcomponents in the default slot:

-   Card Base Header
-   Card Base Actions
-   Card Base Divider

<table id="table_g4t_nzn_14b"><thead><tr><th>

Label\[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Defines the card's size. -   Large \(`"lg"`\)
-   Medium \(`"md"`\)
-   Small \(`"sm"`\)

 Default: Large \(`"lg"`\)

</td></tr><tr><td>

Interaction\[interaction\]

</td><td>

Sets whether the card can be clicked or selected.-   None: Card can be neither clicked nor selected.
-   Click: Card can be clicked.
-   Select: Card can be selected.

 Default: None

</td></tr><tr><td>

Selected\[selected\]

</td><td>

Indicates that the card is selected. Use only when **Interaction** is Select.Default: False

</td></tr><tr><td>

Sidebar\[sidebar\]

</td><td>

Specifies the color of the sidebar that appears along the side of the card. The value is an object with values for `color` and `variant`.Type: `{color: ("ai" |"critical" | "high" | "warning" | "moderate" | "positive" | "info" | "low" | "magenta" | "pink" | "orange" | "yellow" | "brown" | "green" | "green-yellow" | "blue" | "gray" | "teal" | "purple"), variant: ("primary" | "secondary" | "tertiary")}`

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

An object whose keys reference a specific HTML element within the Card Base Container. The available ARIA properties are as follows:-   aria-braillelabel
-   aria-brailleroledescription
-   aria-colindextext
-   aria-description
-   aria-label
-   aria-placeholder
-   aria-roledescription
-   aria-rowindextext
-   aria-valuetext

If the card is configured to be clickable, then the following attributes must be assigned to the card: **role="group"** and **aria-label=""**. This tells screen reader users that all the content in the card is one grouped element.

</td></tr></tbody>
</table>## Card Base Container component events

Select event handlers to configure the actions \(events\) provided with the Card Base Container component.

The Events tab shows the events used by the Card Base Container component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

The Events tab shows the events used by the Card Base Container component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

|Event|Description|
|-----|-----------|
|Card clicked|Dispatched when the card is clicked. Requires the **Interaction** property to be Click. No set payload. Handler and payload depend on what you want to happen when the card is clicked, which in turn depends on what component the card displays.|
|Card selected set|Dispatched when the user toggles the selected status of the card. Requires the **Interaction** property to be Select. The payload is a boolean value indicating the selected status of the card.|

