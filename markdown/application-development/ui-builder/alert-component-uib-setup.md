---
title: Alert component setup
description: The Alert component provides a message to the user as helpful information or a warning.Configure the Alert component with a message, actions to take, and any color to indicate the alert's priority.Select event handlers to configure the actions \(events\) provided with the Alert component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/alert-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Alert component setup

The Alert component provides a message to the user as helpful information or a warning.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Alert component that differentiates it from other components in the [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "alert-content-tree.png"\] Alt text: Alert component with label displayed in the content tree.

2.  Select the Alert component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the alert label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Alert component properties

Configure the Alert component with a message, actions to take, and any color to indicate the alert's priority.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_tcc_czl_qnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type\[status\]

</td><td>

Color indicating the priority of the alert.Default: **Info**

</td></tr><tr><td>

Icon\[icon\]

</td><td>

Icon displayed at the start of the alert.

</td></tr><tr><td>

Header\[header\]

</td><td>

Title for the alert.

</td></tr><tr><td>

Message\[content\]

</td><td>

Message for the alert.

</td></tr><tr><td>

Link\[textLinkProps\]

</td><td>

Object that defines an optional link in the alert. The link opens in a new window when the user clicks it.

</td></tr><tr><td>

Action\[action\]

</td><td>

Action to take in the alert message. For example, to open it or dismiss it.

</td></tr><tr><td>

Max height\[maxHeight\]

</td><td>

Maximum height \(in pixels\) for the content area of an expanded alert. If the content exceeds the provided height, a scrollbar displays inside the alert.

</td></tr><tr><td>

Expanded\[expanded\]

</td><td>

Option to expand the alert beyond the default alert size to show additional content.

</td></tr></tbody>
</table>## Alert component events

Select event handlers to configure the actions \(events\) provided with the Alert component.

The Events tab shows the events used by the Alert component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Alert actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Alert expanded set|Dispatched when an alert whose content overflows the default container size is expanded or collapsed to show/hide the additional content.|
|Alert action selected|Dispatched when the user selects the action on the alert.|
|Alert text link clicked|Dispatched when the user clicks on the text link.|

