---
title: Color picker component setup
description: Color picker allows users to select desired color. It comes with the swatches, list, and palette views.Configure the tabs, buttons, borders, and color options for Color picker with these properties.Select event handlers to configure the actions \(events\) provided with the Color picker component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/color-picker-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Color picker component setup

Color picker allows users to select desired color. It comes with the swatches, list, and palette views.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Color picker that differentiates it from other components in the content tree.

    A label makes finding the Color picker easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "color-picker-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Color picker component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Color picker label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Color picker component properties

Configure the tabs, buttons, borders, and color options for Color picker with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Include Tabs|includeTabs|List of tab names displayed in the order they are declared inside the array.|
|Include Buttons|includeButtons|List of buttons to be displayed. The **Cancel** button always appears before the **Save** button.|
|Default Colors|palette|List of color objects to be displayed in the swatches and list views.|
|Selected Color|selectedColor|The hexadecimal value of the selected color. Eight-digit hexadecimal color codes are supported.|
|Show Borders|showBorders|Indicates whether the color picker appears with borders on all sides or not.|
|Show Custom Colors|showCustomColors|Indicates whether custom colors functionality is enabled or not.|
|Custom Colors|customColors|List of color objects to be displayed in the custom colors section.|

## Color picker component events

Select event handlers to configure the actions \(events\) provided with the Color picker component.

The Events tab shows the events used by the Color picker component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Color picker actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Color Selected|Dispatched when a new selection is made in any of the color picker views. Payload contains selected color string in HEX format, such as: \#278EFC00.|
|Save Clicked|Dispatched when Save button is clicked. Payload contains selected color string is in HEX format.|
|Cancel Clicked|Dispatched when Cancel button is clicked. Payload contains initial color string in HEX format.|
|Custom Color Added|Dispatched when a new custom color is added.|
|Custom Color Deleted|Dispatched when a custom color is deleted.|

