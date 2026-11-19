---
title: Label value tabbed component setup
description: Use the Label value tabbed component to display a label and value strings horizontally side-by-side. A tab character separates each label-value pair and ensures that multiple label-value pairs align horizontally.Configure the appearance and features of the Label value tabbed component.The Label value tabbed component has no configurable actions \(events\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/label-value-tabbed-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Label value tabbed component setup

Use the Label value tabbed component to display a label and value strings horizontally side-by-side. A tab character separates each label-value pair and ensures that multiple label-value pairs align horizontally.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Label value tabbed that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "label-value-tabbed-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Label value tabbed component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Label value tabbed label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Label value tabbed component properties

Configure the appearance and features of the Label value tabbed component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_i5v_dtv_nfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Items\[items\]

</td><td>

Array of label-value items that describe each item. A label item can have one or more value items. Value items can be rendered as a string, a text link, a highlighted value, or raw HTML content. Avoid raw HTML content since it cannot be translated by the component platform.

</td></tr><tr><td>

Size\[size\]

</td><td>

Size of the label-value item in either small or medium.Default: **Medium**

</td></tr><tr><td>

Delimiter\[delimiter\]

</td><td>

Character to display between multiple values of a label.

</td></tr><tr><td>

Label width\[labelWidth\]

</td><td>

Specify a fixed width for the item label. The value you enter must include a unit \(e.g. px, em, %, etc.\)

</td></tr><tr><td>

Wrap label\[wrapLabel\]

</td><td>

Wraps the label if it does not fit on one line. The label wraps after exceeding 50% of the max width if there is one label-value pair, or 30% if there are multiple label-value pairs. If you set a fixed width using the **labelWidth** property, the label wraps at the fixed width.Default: **false**

</td></tr></tbody>
</table>## Label value tabbed component events

The Label value tabbed component has no configurable actions \(events\).

