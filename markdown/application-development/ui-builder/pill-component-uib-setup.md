---
title: Pill component setup
description: The Pill component is used to indicate selected values in multi-select fields. It can contain information such as inputs, actions or attributes.Configure the appearance and features of the Pill component.Select event handlers to configure the actions \(events\) provided with the Pill component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/pill-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Pill component setup

The Pill component is used to indicate selected values in multi-select fields. It can contain information such as inputs, actions or attributes.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Pill that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "pill-content-tree.png"\] Alt text: Pill content tree.

2.  Select the Pill component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Pill label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Pill component properties

Configure the appearance and features of the Pill component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_umb_rcs_b4b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Text displayed inside the pill to identify the function of the pill.Default: "**Issue 42**"

</td></tr><tr><td>

Size\[size\]

</td><td>

Sets the size of the pill. Choices are: **extra small**, **small**, or **medium**.Default: **medium**.

</td></tr><tr><td>

Interaction\[interaction\]

</td><td>

Sets whether the pill can be selected. Choices are: **none** or **select**.Default: **select**.

</td></tr><tr><td>

Icon\[icon\]

</td><td>

Optional icon that is displayed at the start of the pill.

</td></tr><tr><td>

Selected\[selected\]

</td><td>

Indicates the selected state. If true, when the page is first opened, the user sees the toggle as `selected` or "on."

</td></tr><tr><td>

Manage selected \[manageSelected\]

</td><td>

If set to **true**, overrides automatic updates to the **Selected** property. Use the **Pill selected set** event to intercept the requested change and handle it manually.Default: **false**.

</td></tr><tr><td>

Tooltip label for dismiss button \[tooltipContent\]

</td><td>

Optional text to display in a tooltip describing the pill's dismiss button.

</td></tr><tr><td>

Dismissible\[canDismiss\]

</td><td>

Displays a button at the end of the pill, which is used to dispatch an action. For example, an \(X\) button can be provided so the user can select the button to remove the pill.

</td></tr><tr><td>

Disabled \[disabled\]

</td><td>

If set to **true**, the pill color is muted and select interactions are disabled.Default: **false**.

</td></tr><tr><td>

Avatar properties \[avatarProps\]

</td><td>

Displays username, image source, or presence for pill avatar. userName is a string, imageSrc is a string, and presence is **available**, **away**, **busy**, or **offline**. Default: **null**.

</td></tr><tr><td>

ARIA properties

</td><td>

An object whose keys reference a specific HTML element \(**button** or **icon**\) within the Pill. The value of each key is an object that contains an ARIA property and corresponding value. An ARIA property is set on the specified element. If the pill doesn't have a label, or if the label doesn't describe the pill's function, you can configure the icon with an `aria-label` property that provides alt text to describe what the pill does.

 Available ARIA properties for button and icon are:

 -   aria-braillelabel
-   aria-brailleroledescription
-   aria-colindextext
-   aria-description
-   aria-label
-   aria-placeholder
-   aria-roledescription
-   aria-rowindextext
-   aria-valuetext

</td></tr></tbody>
</table>## Pill component events

Select event handlers to configure the actions \(events\) provided with the Pill component.

The Events tab shows the events used by the Pill component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Pill actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Pill selected set|Dispatched when the user toggles the selected status of the Pill. Set the `manage-selected` property to override the default behavior and handle this action manually.|
|Pill dismissed|Dispatched when the user selects the pill dismiss button. The Pill component doesn't handle this action; its parent must handle it and remove the pill from its state so it's no longer rendered.|

