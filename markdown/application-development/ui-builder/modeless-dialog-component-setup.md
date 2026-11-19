---
title: Modeless dialog component setup
description: The Modeless dialog component is a window,  when triggered by a user, appears as an overlay. It enables users to interact with both the main content and window content.The Modeless dialog component is a window that appears as an overlay when triggered by a user. It enables users to interact with both the main content and  window content.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/modeless-dialog-component-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Modeless dialog component setup

The Modeless dialog component is a window,  when triggered by a user, appears as an overlay. It enables users to interact with both the main content and window content.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Modeless dialog that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Modeless dialog component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Modeless dialog component properties

The Modeless dialog component is a window that appears as an overlay when triggered by a user. It enables users to interact with both the main content and  window content.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variant \[variant\]

</td><td>

Sets the header content styles. Choices are:

-   **initial**
-   **primary**
-   **secondary**

Default: **initial**.

</td></tr><tr><td>

Size \[size\]

</td><td>

Sets the header content size. Choices are:

-   **small**
-   **medium**

Default: **medium**.

</td></tr><tr><td>

Width \[width\]

</td><td>

Initial width of the dialog in pixels. Default: **380**.

</td></tr><tr><td>

Height \[height\]

</td><td>

Initial height of the dialog in pixels. Default: **600**.

</td></tr><tr><td>

Position \[position\]

</td><td>

The position of the dialog, on the page, when triggered. Choices available are:

-   **unset**
-   **top-left**
-   **top-right**
-   **centered**
-   **bottom-right**
-   **bottom-left**

Default: **unset**, the dialog goes back to center position with respect to the page.

</td></tr><tr><td>

Offset \[offset\]

</td><td>

Number of pixels to shift the dialog toward the center of the screen. The first value is the horizontal offset. The second value is the vertical offset. Each value must be zero \(0\) or above. You can use this property when the **Position** property is set to **top-left**, **top-right**, **bottom-left**, or **bottom-right**.Default: **\[0,0\]**.

</td></tr><tr><td>

Opened \[opened\]

</td><td>

Determines whether the dialog is open by default. To have the dialog open, set to **true**.Default: **false**.

</td></tr><tr><td>

Fit content \[fitContent\]

</td><td>

To have the size of the dialog automatically adjust based on its content, set to **true**.Default: **false**.

</td></tr><tr><td>

Enable drag\[enableDrag\]

</td><td>

To enable the user to drag the dialog, set to **true**. User can drag the dialog by grabbing the header or footer area \(if available\). Default: **false**.

</td></tr><tr><td>

Show close \[canClose\]

</td><td>

To enable the close button, set to **true**. Default: **false**.

</td></tr><tr><td>

Show minimize\[canMinimize\]

</td><td>

To enable the minimize button, set to **true**. Default: **false**.

</td></tr><tr><td>

Show maximize \[canMaximize\]

</td><td>

To enable the maximize button, set to **true**. Default: **false**.

</td></tr><tr><td>

Heading \[headingLabel\]

</td><td>

Heading label \(title\) for the dialog. Overwrites the default heading slot.

</td></tr><tr><td>

Heading icon \[headingIcon\]

</td><td>

Icon that appears next to the dialog Heading label.

</td></tr><tr><td>

Resizable config\[resizableConfig\]

</td><td>

Whether the modeless dialog dynamically resizes as a user types beyond the size of the dialog, along with the ability to set the resizable minimum and maximum heights. When set to **false**, the modeless dialog doesn't dynamically resize.Default: **true**.

</td></tr></tbody>
</table>## Modeless dialog component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Modeless dialog component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**. If the component has only one event and that event doesn't have a preset, the event is displayed and is ready for configuration.

### Event handlers

Event handlers work with data resources to link the Modeless dialog actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

\[Omitted image "modeless-dialog-presets.png"\] Alt text: Modeless dialog default events tab showing preset events

### Preset events

-   **__Modeless dialog__**

    This preset provides data handlers for these events:

    -   Modeless dialog close
    -   Modeless dialog minimize

### Event descriptions

|Event|Description|
|-----|-----------|
|Modeless dialog opened set|When **Opened \[opened\]** property is set to **true**, triggered when the modeless dialog is opened.|
|Modeless dialog mousedown|Triggers when user selects header or footer \(if shown\).|
|Modeless dialog close|When close button is enabled \(**Show close \[canClose\]** property is set to **true**\) and user selects it, the dialog closes. Also, sets the **Opened \[opened\]** property to **false**.|
|Modeless dialog minimize|Triggers when the minimized button is enabled \(**Show minimize \[canMinimize\]** property is set to **true**\) and user selects it.|
|Modeless dialog maximize|Triggers when maximize button is enabled **Show maximize \[canMaximize\]** and user clicks it, makes the dialog height and width 100% – relative to the container.|
|Modeless dialog mouseup|Triggered when header or footer are shown and user releases mouse pointer from dragging while drag is enabled.|
|Modeless dialog content visible|Triggers when modeless dialog opens and renders the content.|

