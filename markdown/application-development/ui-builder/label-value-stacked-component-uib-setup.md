---
title: Label value stacked component setup
description: Use the Label value stacked component to display label-value pairs vertically where column or horizontal space is limited.Configure the appearance and features of the Label value stacked component.The Label value stacked component has no configurable actions \(events\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/label-value-stacked-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Label value stacked component setup

Use the Label value stacked component to display label-value pairs vertically where column or horizontal space is limited.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Label value stacked that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "label-value-stacked-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Label value stacked component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Label value stacked label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Label value stacked component properties

Configure the appearance and features of the Label value stacked component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_jkh_ydf_14b"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Items

</td><td>

items

</td><td>

Array of label-value items that describe each item. A label item can have one or more value items. Value items can be rendered as a string, a text link, a highlighted value, or raw HTML content. Avoid raw HTML content since it cannot be translated by the component platform.

</td></tr><tr><td>

Alignment

</td><td>

align

</td><td>

Position of label-value items in relation to each other. Choose from the following options.-   **Vertical** - Display label-value pairs on top of each other
-   **Horizontal** - Display label-value pairs side-by-side
-   **Horizontal-equal** - Display label-value pairs side-by-side expanding each item to equally fill its parent container

</td></tr><tr><td>

Size

</td><td>

size

</td><td>

Size of label-value item.

</td></tr><tr><td>

Truncated

</td><td>

truncated

</td><td>

Option to truncate labels and values that do not fit on a single line within its parent container.

</td></tr><tr><td>

Wrap text

</td><td>

wrapped

</td><td>

Option to wrap label and values that do not fit on a single line to multiple horizontal rows.

</td></tr><tr><td>

Item min width

</td><td>

itemMinWidth

</td><td>

Minimum width of an individual label-value pair. The default value is 50px. The specified value must list a valid style sheet unit of measurement such as **px** for pixels.

</td></tr><tr><td>

Delimiter

</td><td>

delimiter

</td><td>

Character to display between multiple values of a label.

</td></tr></tbody>
</table>## Label value stacked component events

The Label value stacked component has no configurable actions \(events\).

