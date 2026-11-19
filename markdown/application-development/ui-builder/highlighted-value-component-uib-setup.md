---
title: Highlighted Value component setup
description: The Highlighted Value component is a styled label with an optional icon.Define the highlighted text, background color, and the icon of the Highlighted Value component with these properties.The Highlighted Value component has no configurable actions \(events\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/highlighted-value-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Highlighted Value component setup

The Highlighted Value component is a styled label with an optional icon.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Highlighted Value component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "highlighted-value-content-tree.png"\] Alt text: Image showing Highlighted Value content tree

2.  Select the Highlighted Value component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Highlighted Value label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Highlighted Value component properties

Define the highlighted text, background color, and the icon of the Highlighted Value component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_pzs_wyg_14b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Text displayed in the highlighted value.

</td></tr><tr><td>

Will wrap\[willWrap\]

</td><td>

Wraps the text if it doesn't fit on one line.

</td></tr><tr><td>

Variant\[variant\]

</td><td>

Shade of the highlighted value background and the color of the text and/or icon.Default: **Tertiary**

</td></tr><tr><td>

Size\[size\]

</td><td>

Size of the highlighted value: **small** or **medium**.Default: **Small**

</td></tr><tr><td>

Tooltip label\[tooltipContent\]

</td><td>

Text string displayed in the tooltip.

</td></tr><tr><td>

Helper content\[helperContent\]

</td><td>

Additional text displayed in a popover when the highlighted value is selected. Use plain text to enable translation. If you don't want to add helper content, leave this property empty.

</td></tr><tr><td>

Color\[color\]

</td><td>

Background color of the highlighted value. Choices include:-   **AI**
-   **Critical**
-   **High**
-   **Warning**
-   **Moderate**
-   **Positive**
-   **Info**
-   **Low**
-   **Magenta**
-   **Pink**
-   **Orange**
-   **Yellow**
-   **Brown**
-   **Green**
-   **Green-yellow**
-   **Blue**
-   **Gray**
-   **Teal**
-   **Purple**

Default: **Low**

</td></tr><tr><td>

Icon\[icon\]

</td><td>

Optional icon to display in the highlighted value.

</td></tr></tbody>
</table>## Highlighted Value component events

The Highlighted Value component has no configurable actions \(events\).

