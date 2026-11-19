---
title: Custom illustration component setup
description: Places theme-able inline Scalable Vector Graphics \(SVG\)s in Next Experience pages or components created in UI Builder.Configure the appearance and features of the Custom illustration component.The Custom illustration component has no configurable actions \(events\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/custom-illustration-component-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Custom illustration component setup

Places theme-able inline Scalable Vector Graphics \(SVG\)s in Next Experience pages or components created in UI Builder.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for custom illustration that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the custom illustration component using one of these methods:

    -   Select anywhere within the component on the page.
    -   Select the label that you created for your component in the content tree.
    The configuration options appear in the panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Custom illustration properties

Configure the appearance and features of the Custom illustration component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SVG image source \[src\]

</td><td>

URL of the SVG image.

</td></tr><tr><td>

Token ID \[tokenId\]

</td><td>

The unique key suffix to add to '-now-illustration-custom-' that contains the SVG image URL. It enables the creation of the style design token.

 The **Token ID** always takes precedence over the **SVG image source**.

</td></tr><tr><td>

Alt text \[alt\]

</td><td>

Alternative text to use on the &lt;img&gt; tag of the illustration. By default, there's no alternative text.

</td></tr><tr><td>

Width\[width\]

</td><td>

Width of your inline SVG image in pixels or a percentage of the container.Default: **100%**.

</td></tr><tr><td>

Height \[height\]

</td><td>

Height of your inline SVG image in pixels or a percentage of the container.Default: **100%**.

</td></tr></tbody>
</table>## Custom illustration events

The Custom illustration component has no configurable actions \(events\).

