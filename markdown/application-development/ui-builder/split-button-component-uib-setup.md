---
title: Split Button component setup
description: The Split Button component has a separate variation with a primary action and a dropdown panel with related actions.Define the size, label, and other configurations of the Split Button component with these properties.Select event handlers to configure the actions \(events\) provided with the Split Button component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/split-button-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Split Button component setup

The Split Button component has a separate variation with a primary action and a dropdown panel with related actions.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Split Button that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "split-button-content-tree.png"\] Alt text: Image showing Split Button content tree

2.  Select the Split Button component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Split Button label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Split Button component properties

Define the size, label, and other configurations of the Split Button component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_fgz_ccn_14b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Text describing the purpose of the button to the user. The text displays inside the button.

</td></tr><tr><td>

Variant\[variant\]

</td><td>

Button style, including color and interaction behavior.

</td></tr><tr><td>

Size\[size\]

</td><td>

Size of the button.

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Option to disable the component. When this property is set to true, the button color is muted and user interaction is unavailable.Default: **false**

</td></tr><tr><td>

Opened\[opened\]

</td><td>

Property that is automatically updated when the user opens or closes the dropdown panel. Use this property to override the default behavior and handle the NOW\_SPLIT\_BUTTON\#OPENED\_SET event manually. For example, you can use this property in a client script to perform some action.**Note:** Setting this flag to **true** forces the dropdown panel to open when the page loads. Selecting an item from the list closes the panel.

Default: **false**

</td></tr><tr><td>

Manage opened\[manageOpened\]

</td><td>

Enable this property to override automatic updates to the opened property. Use the opened set event to intercept the requested change and handle it manually.

</td></tr><tr><td>

Icon\[icon\]

</td><td>

Icon to display inside the button.

</td></tr><tr><td>

Animated icon\[animatedIcon\]

</td><td>

Animated icon to display inside the button.

</td></tr><tr><td>

List items\[items\]

</td><td>

Objects that define related actions in the dropdown panel.

</td></tr><tr><td>

Tooltip label\[tooltipContent\]

</td><td>

Text that is displayed when hovering either of the buttons.

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

An object whose keys reference a specific HTML element within the split button. The value of each key is an object that contains an ARIA property and corresponding value. These ARIA properties are set on the specified element.

</td></tr><tr><td>

Landmark\[text\]

</td><td>

Enable the Landmark Focus keyboard shortcut to focus on this split button.

</td></tr></tbody>
</table>## Split Button component events

Select event handlers to configure the actions \(events\) provided with the Split Button component.

The Events tab shows the events used by the Split Button component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Split Button actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Split button opened set|Presents related actions|
|Split button item clicked|Prompts action to related set styles or related event|
|Split button action clicked|Actions performed on stage|

