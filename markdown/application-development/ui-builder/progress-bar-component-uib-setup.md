---
title: Progress Bar component setup
description: The Progress Bar displays the loading or completion progress of an ongoing, user-initiated process.Configure the appearance and values for the Progress Bar.The Progress Bar component has no configurable actions \(events\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/progress-bar-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Progress Bar component setup

The Progress Bar displays the loading or completion progress of an ongoing, user-initiated process.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Progress Bar that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "progress-bar-content-tree.png"\] Alt text: Content tree with the Progress Bar component.

2.  Select the Progress Bar component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Progress Bar label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Progress Bar component properties

Configure the appearance and values for the Progress Bar.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_kzb_krt_xnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Label for the progress bar that identifies the operation in progress.Default: none

</td></tr><tr><td>

Label position\[labelPosition\]

</td><td>

Position of the progress bar label with respect to the bar. The choices are: -   Top \(default\)
-   Bottom

</td></tr><tr><td>

Size\[size\]

</td><td>

Sets the size of the bar. The choices are:-   Extra small \(xs\)
-   Small \(sm\)
-   Medium \(md\)
-   Large \(lg\)

</td></tr><tr><td>

Style\[pathType\]

</td><td>

Sets the color of the bar. Match the color with the status you want to express for an operation. The choices are:-   Initial \[green\]
-   Positive \[blue\]
-   Alert \[brown\]
-   Error \[red\]
-   Inactive \[light gray\]
-   Pink
-   Green \[khaki\]
-   Orange
-   Gray

</td></tr><tr><td>

Max value\[max\]

</td><td>

Sets the value that the progress bar must reach to complete. The value must be greater than zero and be a valid floating point number. If you don't set a maximum value, the value defaults to 1.

</td></tr><tr><td>

Value\[value\]

</td><td>

Specifies how much of the process is completed. If you set a **Max value**, the value must be a valid floating point number from zero through the maximum. If you don't set a maximum value, the value must be from 0 through 1. If you provide a valid value, a determinate progress bar displays. If you don't provide a value or provide an invalid value, an indeterminate progress bar displays.

</td></tr><tr><td>

ARIA properties\[configAria\]

</td><td>

Configures the ARIA properties. Possible properties are:-   aria-braillelabel
-   aria-brailleroledescription
-   aria-colindextext
-   aria-description
-   aria-label \(Required to be accessible using a screen reader if no label is configured\)
-   aria-placeholder
-   aria-roledescription
-   aria-rowindextext
-   aria-valuetext

</td></tr></tbody>
</table>## Progress Bar component events

The Progress Bar component has no configurable actions \(events\).

