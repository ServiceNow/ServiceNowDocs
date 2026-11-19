---
title: Animation component setup
description: The animation component provides the ability to place Lottie animations in Next Experience pages or components.Configure the appearance and features of the Animation component.Select event handlers to configure the actions \(events\) provided with the Animation component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/animation-component-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Animation component setup

The animation component provides the ability to place Lottie animations in Next Experience pages or components.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Animation that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Animation component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Animation properties

Configure the appearance and features of the Animation component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Animation source path \[src\]

</td><td>

Source \(path\) to where the animation resides.

</td></tr><tr><td>

Token id \[tokenId\]

</td><td>

A unique key suffix to add to “now-animation-custom” to create a style design token that contains the animation JSON. The **Token ID** always takes precedence over the **animation source path**.

</td></tr><tr><td>

Autoplay \[autoplay\]

</td><td>

If set to **true**, the animation starts automatically playing when it's loaded.Default: **false**

</td></tr><tr><td>

Loop \[loop\]

</td><td>

If set to **true**, the animation plays continuously.Default: **false**

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

A JSON field for configuring ARIA properties, such as **aria-braillelabel**. Currently, aria-label is only supported.

</td></tr></tbody>
</table>## Animation component events

Select event handlers to configure the actions \(events\) provided with the Animation component.

The Events tab shows the events used by the Animation component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Animation actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Animation clicked|Dispatched when the animation is clicked. The payload includes Animation source path and Token ID.|
|Animation mouseenter|Dispatched when the mouse cursor enters the animation. The payload includes Animation source path and Token ID.|
|Animation mouseleave|Dispatched when the mouse cursor leaves the animation. The payload includes Animation source path and Token ID.|
|Animation content visible|Dispatched when the Lottie animation is rendered on the page. The payload includes Animation source path and Token ID.|

