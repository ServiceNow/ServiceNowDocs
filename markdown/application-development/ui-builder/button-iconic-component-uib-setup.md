---
title: Button iconic component setup
description: The Button iconic component is a button represented by an actionable icon. The iconic button can't display other elements, such as labels.Configure the appearance, functionality, and tooltip text of Button iconic.Select event handlers to configure the actions \(events\) provided with the Button iconic component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/button-iconic-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Button iconic component setup

The Button iconic component is a button represented by an actionable icon. The iconic button can't display other elements, such as labels.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

This component contains preset configuration values that are intended for use with the Record List component bundle only. Some preset values for Button iconic won’t function as expected if used with the standalone component. When using this component outside of the Record List bundle, configure it manually.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Button iconic that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "button-iconic-content-tree.png"\] Alt text: Component content tree with the button iconic component.

2.  Select the Button iconic component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Button iconic label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

3.  If using Button iconic as a standalone component \(not in a bundle\), select **None** in the Config panel to remove preset values.

    \[Omitted image "button-iconic-preset-panel.png"\] Alt text: Shows the preset selection panel for button iconic and the None selection for manual configuration


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Button iconic component properties

Configure the appearance, functionality, and tooltip text of Button iconic.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_pdd_krq_wnb"><thead><tr><th>

Label \[Property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Icon\[icon\]

</td><td>

Type of icon used for the button.

</td></tr><tr><td>

Variant\[variant\]

</td><td>

Color and behavior of the icon.

</td></tr><tr><td>

Bare\[bare\]

</td><td>

Removes the border on the button and makes the background transparent.

</td></tr><tr><td>

Size\[size\]

</td><td>

Size of the button.

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Disables the button by muting the colors of the button and preventing clicking interactions.

</td></tr><tr><td>

Animated icon\[animatedIcon\]

</td><td>

Animated icon to display inside the button.

</td></tr><tr><td>

Tooltip text\[tooltipContent\]

</td><td>

Text to display in the button's tooltip.

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

An object whose keys reference a specific HTML element within the dropdown. The value of each key is an object that contains an ARIA property and corresponding value. These ARIA properties are set on the specified element.

</td></tr><tr><td>

Landmark\[landmark\]

</td><td>

Enable the Landmark Focus keyboard shortcut to focus on this split button.

</td></tr></tbody>
</table>## Button iconic component events

Select event handlers to configure the actions \(events\) provided with the Button iconic component.

The Events tab shows the events used by the Button iconic component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Button iconic actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Button iconic clicked|User selects the button iconic.|

