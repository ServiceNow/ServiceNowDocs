---
title: Button stateful component setup
description: The Button stateful component contains an actionable icon that can switch between ON and OFF states. This button can't display other elements, such as labels.Configure the appearance and features of the Button stateful component.Select event handlers to configure the actions \(events\) provided with the Button stateful component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/button-stateful-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Button stateful component setup

The Button stateful component contains an actionable icon that can switch between ON and OFF states. This button can't display other elements, such as labels.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Button stateful that differentiates it from other components in the content tree.

    For more information, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "button-stateful-config-content-tree.png"\] Alt text: Button stateful component in the content tree

2.  Select the Button stateful component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Button stateful label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Button stateful component properties

Configure the appearance and features of the Button stateful component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Icon|icon|Icon to display inside the button.|
|Selected|selected|Selection state of the button.|
|Variant|variant|Button style, including color and interaction behavior.|
|Size|size|Button size.|
|Config role|configRole|Type of stateful element to display such as button, radio, or tab.|
|Disabled|disabled|Option to mute the button color and prevent user interactions.|
|Padding|hidePadding|Option to show or hide button padding. Hiding padding reduces the button height so that the button only takes up the height required by its label and icons.|
|High contrast|highContrast|Option to display variant colors that have higher contrast. Use this property when displaying components on darker backgrounds.|
|Tooltip text|tooltipContent|Text displayed in a tooltip when the user hovers over the button.|
|ARIA properties|configAria|Object to set the ARIA properties for the specified HTML element within the button. The value of each key is an object that contains an ARIA property \(or properties\) and corresponding values. These ARIA properties are set on a specified element.|

## Button stateful component events

Select event handlers to configure the actions \(events\) provided with the Button stateful component.

The Events tab shows the events used by the Button stateful component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Button stateful actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Button stateful selected set|Dispatched when the user toggles the selected status of the button.|

