---
title: Simple timer component setup
description: The Simple timer component displays elapsed time with an optional leading icon and configurable start and end times.Configure the properties for Simple timer.Select event handlers to configure the events provided with the Simple timer component. Event handlers work with data resources to link the Simple timer actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/simple-timer-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Simple timer component setup

The Simple timer component displays elapsed time with an optional leading icon and configurable start and end times.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Simple timer that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "simple-timer-content-tree.png"\] Alt text: Simple timer component in the UI Builder content tree.

2.  Select the Simple timer component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "simple-timer-config.png"\] Alt text: Simple timer component in the UI Builder configuration panel.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Simple timer component properties

Configure the properties for Simple timer.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start time\[startTime\]

</td><td>

Sets the exact date and time when the timer begins. Include both the date and time in the value. You don't need to add a comma or specify the weekday, but you can if you prefer.Example: `November 18 2025 10:00 AM` or `Tuesday, November 18, 2025 10:00 AM`

</td></tr><tr><td>

End time\[endTime\]

</td><td>

Sets the exact date and time when the timer ends. Include both the date and time in the value. You don't need to add a comma or specify the weekday, but you can if you prefer.Example: `November 18 2025 10:00 AM` or `Tuesday, November 18, 2025 10:00 AM`

</td></tr><tr><td>

Minimum resolution\[minResolution\]

</td><td>

Sets the timer's smallest counting unit in either seconds or minutes.Default: **Seconds**

</td></tr><tr><td>

Timer size\[size\]

</td><td>

Defines the timer's display size in either small \(sm\) or medium \(md\).Default: **sm**

</td></tr><tr><td>

Timer icon\[icon\]

</td><td>

Displays an icon to the left of the timer text.

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

Configures ARIA properties.

</td></tr></tbody>
</table>## Simple timer component events

Select event handlers to configure the events provided with the Simple timer component. Event handlers work with data resources to link the Simple timer actions to the data you want to display to your users.

The Events tab shows the events used by the Simple timer component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Simple timer actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Timer ended\[SN\_TIMER\#TIMER\_ENDED\]

</td><td>

Action that is dispatched when the timer stops counting.Payload:

```
{
              "name": "value",
              "label": "Value",
              "fieldType": "string",
              "typeMetadata": {
                "schema": {
                  "type": "string"
                }
              }
            }
```

</td></tr></tbody>
</table>